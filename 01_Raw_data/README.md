# Raw Data

The Raw data in this repo is from the Pailla-Coreano behavioural neuroscience lab at the University fo Florida. They do most of their experiments on mice. This specific set of data is obtained through electrophysiology measurements of neural activity taht was recorded over a time while mice were allowed to socially interact with one another. 

The `phase2_collection.pkl` file isa pickle file of a Python class object. The `multirecording_spikeanalysis.py` script shows how this class was created.

All the data in this class object are under the `Class_object.collections` attribute as a python dictionary. The `.collections` dictionary contains data for a number of different recording sessions with the recording session name as a key (the second nested Python class variable can be accesses with `Class_object.collections["recording_session_name"]`) and another Python class varaible as a value. 

The second nested Python class variable has the following attributes that are all necessary for the analysis showcased in this repository:

- `Class_object.collections["recording_session_name"].subject` - Is a single **string** of which individual mouse this recording was done on.
- `.labels_dict` - Is a **dictionary** with the unit as a key and the type of unit as a value. (Unit in the case of this analysis could mean a neuron or a group of neurons that were recorded with the electrophysiology activity sensor.)
- `.timestamps_var` - This attribute is a **numpy array** that contains the index timestamp at which activity was recorded for during this session. The recording is a binary recording made at 20kHz so 20 000 times a second an observation is recorded. Each time activity is measured it is recoded as a 1 wit hthe  rest of the recording stream being filled with 0. This attribute array contains all the indexes of all the 1 values.
- `.unit_timestamps` - Is a **dictionary** with the unit as a key and the specific timestamps index **numpy array** as a value. This is similar to the `.timestamps_var` attribute, with the only difference being that the recordings have now been sorted according to each unit.
- `.event_dict` - Is a **dictionary** with the type of social behaviour as a key and a 2D **numpy array** as a value. Each row in the array contains a start timestamp index and a stop timestamp index during which times the behaviour was observed. These labels are done by hand by the scientists in the lab. Each event type can have multiple rows in the 2D array.