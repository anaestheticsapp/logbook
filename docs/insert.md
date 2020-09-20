# Settings

You can access the settings tab by clicking on the settings icon. The settings tab contains three cards:

* **Custom items**. This will show all custom items that you have saved. You can create custom items for all form fields that have the keyboard icon. The settings page will allow you to delete your saved custom items.
* **Form Items**. The Form Items card will allow you to enable and disable specific form items.
  * Please note that the ```Supervision``` and ```Supervisor``` fields are required for your RCoA logbook summary and ARCP if you are a trainee. If you are a consultant, you can turn both fields off as they don't apply to you.
  * The ```Duration``` form field will be used to calculate your total anaesthetic time and will be shown in your logbook summary in a future update. We think this is a better marker of anaesthetic exposure than case numbers.
  * The ```Position``` and ```Analgesia``` form items are optional and disabled by default. Depending on popularity, these may be removed in future updates. We regularly test new form fields and analyse how useful they are based on user feedback.
* **Forms**. If you don't do intensive care or clinics, you can turn off these form fields here.

# Inserting a case
* ```Date```. The app will automatically select **Today** unless you have entered a case within the last 12 hours. In that case, the last date of the previous case will be automatically selected. This is helpful for users who enter cases on a weekly basis, as you don't have to change the date of your cases all the time. As you can see, there are only two options by default - today and yesterday. To select any date, just click on the calender icon.
* ```Session```
  * Morning 08:00 - 13:00
  * Afternoon 13:00 - 18:00
  * Evening 18:00 - 22:00
  * Night 22:00 - 08:00
* ```Speciality```
  * The form field will show you the most frequently used specialities in your current workplace. Most specialities won't be relevant to subspecialised consultants, for example in cardiac. Specialites not used commonly will be hidden by default to keep the list short. Click the arrow icon the to view all specialities.
* ```Operation```
  * Clicking on this form field will open the **operation picker**. It will show you the list of all operations for the speciality selected. Therefore, before using this form field, make sure zou have selected the correct speciality. Typing in the text field will filter all operations and shorten the list. For example, typing in "appendix" will show "Open appendicectomy", "Laparoscopic appendicectomy", "Laparotomy appendicectomy". If an operation is not listed, just click the "Enter" button. Once you have entered an operation twice, it will automatically appear in the list of operations.
  * Starred operations are operations that are commonly used in the app and by yourself.
  * You can also save operations to your favourites. Just click on the "heart" to mark an operation as "favourite". The next time you open the operation picker, you will see all your favourite operations at the top of the list and allows you to qucikly select them. To remove an item, just click on the red heart again. Favourites will be synchronised between your devices, although there will be a short time delay to avoid any performance issues.
  * Once you have selected an operation and the operation picker is closed, you can still click on the operation to edit it. This will bring up the on-screen keyboard on mobile devices. To open the operation picker instead, just click the "add to list" icon 
* ```Priority```
  * Immediate
    * Immediate life, limb or organ-saving intervention.
    * Resuscitation simultaneous with intervention.
    * Within minutes of decision to operate.
  * Urgent
    * Acute onset or clinical deterioration of potentially life-threatening conditions.
    * Fixation of fractures.
    * Normally within hours of decision to operate.
  * Expedited
    * Eearly treatment where the condition is not an immediate threat to life, limb or organ survival.
    * Normally within days of decision to operate.
  * Elective
    * Intervention planned or booked in advance of routine admission to hospital
    * Timing to suit patient, hospital and staff
  * When selecting "Obstetrics", you will also be able to chose from "Category 1" (Immediate threat to life of woman or fetus), "Category 2" (No immediate threat to life of woman or fetus), "Category 3" (Requires early delivery). Category 4 is elective and this should be selected instead.
* ```Destination```
  * POCU - Post-operative care unit
* ```Supervision```
  * This is who is supervising you. This field is not applicable to consultants. You can turn off this form field in the settings.
  * Immediate - supervisor is within the theatre complex.
  * Local - supervisor is outside the theatre complex.
  * Distant - supervisor is not in the hospital.
  * Solo - although trainees must always be supervised, we recommend to use this option if you are doing a solo list with a consultant supervising you from a distance (ie discuss the list with your consultant at the beginning of your list but consultant is not part of the team brief and not in theatre with you). If your consultant is present for induction and then leaves you to do the case, this is **local supervision**
* ```Supervisor```
  * Most people select the level of supervision but a lot of trainees also enter the name of the supervisor (click on the keyboard to create a custom item).
  * This field is not applicable to consultants and can be turned off in the settings.
* ```ASA```
  * 1 A normal healthy patient
  * 2 A patient with mild systemic disease (smoker, social alcohol drinker, obesity, pregnancy)
  * 3 A patient with severe systemic disease
  * 4 A patient with severe systemic disease that is a constant threat to life
  * 5 A moribund patient who is not expected to survive without the operation
  * 6 A declared brain-dead patient whose organs are being removed for donor purposes
* ```Anaesthesia```
  * This form field allows multiple selections. For example, if you are doing a case under sedation but sedation fails and you have to insert a supraglottic airway or endotracheal tube, select "Sedation" and "Volatile"/"TIVA" depending on what you use.
  * RSI Rapid sequence induction
* ```Airway```
  * This form field applies to general anaesthesia only - not sedation. Mask here means you are doing a general anaesthetic but only using an airway adjunct and bag mask ventilation for a short case (for example, MUA nose).
  * You can create your own custom items. Most people like to specify the type of LMA used (ie iGel, Proseal, Classic LMA) or the type of ETT used (ie RAE, Laser ETT, MLT)
* ```Regional```
  * Options shown here by default depend on what speciality you have selected. For example, if you enter a neuro case, you are unlikely to use any blocks, so only a "Scalp block" is shown by default. This is to keep the list short and to make entering cases quicker. To view all regional items, just click on the arrow.
  * Selecting an option will display another form field which will allow you to choose from "Landmark", "Ultrasound", "Nerve Stimulator", "Catheter", "Observed". Some people select catheter for epidural, although this is not required as a catheter is inserted by default and selecting epidural will automatically assume you have used a catheter.
* ```Procedures```
  * As with regional, options shown here are dependend on speciality selected. To view all items, click the arrow. You can also enter custom items.
* ```Incidents```
  * CICV Casn't intubate, can't ventilate
* ```Labels```
  * This allows you to label your case with a tag. **Do not use any labels that will allow patient identification**. This is more to help you keep track which parts of the curriculum you have covered. If you have discussed "Bone cement implantation syndrome" with your consultant, you can add this to your labels. It doesn't mean this event happened (if it did, use the incident box instead).
  * Consultants can use labels to keep track of private patients
* ```Hospital```
  * You can only select hospitals which you have listed in your workplace. When you create a workplace, you will be able to select up to four hospitals. Always put your primary/main hospital first. You cannot select between different workplaces.
  * When your workplace has expired, you will see an error message. Always make sure your workplace is up-to-date as editing cases later is time consuming.
* ```Reflection, draft, follow up```
  * If you have reflected about something in your notes, tick the "Reflection" box. This will help you to find those cases later on when you have to create your reflections for your ARCP. You can also use this if you have learned something and you want to remind yourself later on. For example, you have used an awake fibreoptic "recipe" that worked particularly well. If you have to do another one after 6-12 months, you are unlikely to remmeber what you have done. Instead, open your logbook, filter out your cases marked as reflection, and select the case where you have described your technique.
  * If you have started to enter case but want to add something later on, mark the case as a "Draft"
  * If you want to follow up a patient, use the "Follow up" check box. This is useful for regional technique where you want to see how well or how long your block lasted.
