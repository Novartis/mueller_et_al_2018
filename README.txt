Digit Biomark
Continuous monitoring of patient mobility for 18 months using inertial sensors
following traumatic knee injury: a case study
Mueller A., Hoefling H., Nuritdinow T., et al.
DOI: 10.1159/000490919

## Description of data files

## meta-data.txt

Experiment/subject meta-data.

path: the path to the belt file with raw acceleration data
belt.id: the internal ID of the device
start/end: time stamps when the device was switched on/off
ducation: the difference between end and start in seconds
stopcode: stop code this is the stopcode (as string) according to firmware specification 
uuid: a unique ID for device and period when it was worn. One device can generate several
raw data files, and each of tese files has the same uuid but differnet file names.
year_of_birth: of subject
gender: if subject
patient_time_zone: of subject (only one time zone is supported)


## gait_params.txt.gz

Compressed gait parameters derived from raw data.

time: time of heel-strike of the foot
running: TRUE if the foot/step was in a running mode (otherwise FALSE)
toeoff: time of toe-off of the foot
foot: left/right foot
speed: walking speed of this step
duration: adjusted duration of this step
distance: distance of this step
steptime: time of the step (heel strike - heel strike of the prev. foot)
stancetime: time for heel strike to toe-off of the same foot
swingtime: heel strike to prev. toe-off of the same foot
new_bout: TRUE if this step belongs to a new walking bout (>= 3 sec pause to prev. step)
bout_num: index of the bout
bout_len: number of steps in this bout
bout_type: short, medium, long walking bouts with 5-20, >20-100, >100-500 steps

## belt/

Directory with periods and belts.

x/y/z: acceleratino in g
KSS: 1 or 0 if the belt magnet (in the belt buckle) was closed or open

Note, the KSS can be used to determine whether a belt was open or closed.

Date is recorded at 100 Hz, the first record corresponds to the start time stamp in the
meta-data.txt file.

## diary.tsv

Diary with events manually annotated by the study participant. Includes key milestones (e.g. returning to work), physiotherapy sessions, falls and near falls, and other observations.

FreeText: Notes entered by the participant, free text.
Date: Date of event, in DDMMYYYY format.
StartTime: Begin time of event if applicable, in CET.	
EndTime: End time of event if applicable, in CET.	
Start: DateTime formatted beginning of event.
End: DateTime formatted end of event.
EventType: Grouping of events (Milestone for major events, Physio for physiotherapy sessions, Fall and Near Fall, otherwise NA.

