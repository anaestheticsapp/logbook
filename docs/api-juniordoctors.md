# API
* ```https://api.juniordoctors.co.uk/public/v1/```
  * POST ```/getreviews``` - get reviews
  * POST ```/departmentreview``` - post review

## Security
  * Authentication - users must have an AnaestheticsApp account
  * CORS Same-Origin Policy
  * CSRF Header
  * Transport Layer Security
  * Strict-Transport-Security
  * Content-Security-Policy

## Headers
* ```Content-Type: application/json```
* ```User-Agent: AnaestheticsApp/6.0```

# Types
```ts
type PrivateAPIKey = string;

type UUID = string;

/**
 * - T most recent (default)
 * - H highest rating first
 * - L lowest rating first
 */
type SortBy = 'T'|'H'|'L';

/**
 * - D Department
 * - P Training Programme
 */
type ReviewType = 'D'|'P';

/**
 * Supported training programmes in the AnaestheticsApp Logbook
 */
type TrainingProgramme = 'Core Anaesthetics'|'Anaesthetics ST4+'|'Foundation Programme';

/**
 * Supported specialities in the AnaestheticsApp Logbook
 */
type Speciality = 'Anaesthetics'|'Intensive Care Medicine';

export interface HospitalReview {
  review: string;
  rating: number;
  yearPosted: number;
  programme: string;
  site: string;
  department: string;
  workHereAgain: boolean;
  type: ReviewType;
  isTest?: boolean;
}
export interface WorkplaceReview {
  _hospital: Record<string, UUID>;
  _programme?: TrainingProgramme;
  averageRating: number;
  workHereAgain: number;
  totalReviewCount: number;
  reviews: HospitalReview[];
}

interface ErrorResponse {
  code: number;
  message: string;
}
/**
 * - ```sites``` - max 10
 * - ```specialities``` - max 2
 * - ```offset``` - default 0
 * - ```noOfReviews``` - default 20
 */
interface GetReviews {
  key: PrivateAPIKey;
  sites: UUID[];
  specialities: UUID[];
  sortBy: SortBy;
  offset?: number;
  noOfReviews?: number;
}

export interface GetReviewsResponse {
  ok?: true;
  data?: WorkplaceReview;
  error?: ErrorResponse;
}

/**
 * - ```review``` must be 40 characters and must not contain URLs
 * - ```rating``` 0-5
 */
 interface PostReview {
  key: PrivateAPIKey;
  site: UUID;
  speciality: UUID;
  programme: UUID;
  rating: number;
  review: string;
  workHereAgain: boolean;
  isTest: boolean;
}

export interface PostReviewResponse {
  ok?: true;
  data?: HospitalReview;
  error?: ErrorResponse;
}
```

# Logbook Integration
* Users must have a valid workplace
  * Country must be set to ```United Kingdom```
  * Region and hospital must match corresponding key in database
* API will be used in the ```<card-workplace></card-workplace>``` web component
	* **"Home" page**
		* Maximum of 5 reviews are shown in the "Workplace" card.
		* Link to ```juniordoctors.co.uk``` to view all reviews and facilities
		* Only _trainees_ will be able to review hospitals in the "Workplace" card.
		* Video: https://twitter.com/AnaestheticsApp/status/1557407510746873859?s=20&t=JP-PAYxSYyU_yEFyg2OHww
	* **"Account" page**
		* _Trainees_ will be able to review all previous placements/hospitals (max 20).
		* No reviews are shown.
		* Video: https://twitter.com/AnaestheticsApp/status/1557407541872713729?s=20&t=JP-PAYxSYyU_yEFyg2OHww

# Data Protection and Privacy
* No personal data will be submitted to the third-party provider (juniordoctors.co.uk)
* We record the following data for analytics:
	* User engagement
		* ```click/submit-button``` to monitor feature-uptake
	* Errors
		* ```api/offline``` to assess performance & user experience
		* ```api/bad-request``` for maintenance and to monitor for bugs
* No user data (ie user id, email, ip address, ...) is stored/associated with our analytics data
* We do not share any analytics data with third parties
