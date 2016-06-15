## API Fields

Serialized headers are main models (e.g. `Event`, `Session`, etc.). Others  are nested fields (e.g. `SessionSpeaker`, `TrackSession`, etc.).

Datatype, requirement and access-level has been defined for every model. Nested fields inherit the access-level defined for them in the model.

### 1. Event

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Required | Public |
|**description** | string | Optional | Public |
|**event_url** | string | Optional | Public |
|**color** | string | Optional | Public |
|**logo** | string | Optional | Public |
|**location_name** | string | Optional | Public |
|**start_time** | string | Required | Public |
|**end_time** | string | Required | Public |
|**latitude** | number | Optional | Public |
|**longitude** | number | Optional | Public |
|**background_url** | string | Optional | Public |
|**state** | string | Optional | Public |
|**email** | string | Optional | Public |
|**organizer_name** | string | Optional | Public |
|**organizer_description** | string | Optional | Public |
|**closing_datetime** | string | Optional | Public |

### 2. Format

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**label_en** | string | Optional | Public |
|**name** | string | Optional | Public |


### 3. Languages

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**label_de** | string | Optional | Public |
|**label_en** | string | Optional | Public |
|**name** | string | Optional | Public |


### 4. Level

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**label_en** | string | Optional | Public |
|**name** | string | Optional | Public |


### 5. Microlocation

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Optional | Public |
|**floor** | integer | Optional | Public |
|**latitude** | number | Optional | Public |
|**longitude** | number | Optional | Public |
|**room** | string | Optional | Public |


### 6. Session

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**title** | string | Optional | Public |
|**subtitle** | string | Optional | Public |
|**description** | string | Optional | Public |
|**abstract** | string | Optional | Public |
|**start_time** | string | Optional | Public |
|**end_time** | string | Optional | Public |
|**speakers** | Array[**SessionSpeaker**] | Optional | Public |
|**language** | **SessionLanguage** | Optional | Public |
|**format** | **SessionFormat** | Optional | Public |
|**track** | **SessionTrack** | Optional | Public |
|**microlocation** | **SessionMicrolocation** | Optional | Public |
|**level** | **SessionLevel** | Optional | Public |



#### SessionSpeaker

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**name** | string | Optional |


#### SessionLanguage

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**label_de** | string | Optional |
|**label_en** | string | Optional |


#### SessionFormat

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**name** | string | Optional |


#### SessionTrack

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**name** | string | Optional |


#### SessionMicrolocation

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**name** | string | Optional |


#### SessionLevel

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**label_de** | string | Optional |
|**label_en** | string | Optional |



### 7. Speaker

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Optional | Public |
|**email** | string | Optional | Public |
|**biography** | string | Optional | Public |
|**organisation** | string | Optional | Public |
|**country** | string | Optional | Public |
|**web** | string | Optional | Public |
|**github** | string | Optional | Public |
|**photo** | string | Optional | Public |
|**position** | string | Optional | Public |
|**facebook** | string | Optional | Public |
|**twitter** | string | Optional | Public |
|**linkedin** | string | Optional | Public |
|**sessions** | Array[**SpeakerSession**] | Optional | Public |





#### SpeakerSession

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Optional |
|**title** | string | Optional |


### 8. Sponsor

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Optional | Public |
|**description** | string | Optional | Public |
|**url** | string | Optional | Public |
|**logo** | string | Optional | Public |
|**sponsor_type_id** | integer | Optional | Public |



### 9. SponsorType

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Optional | Public |


### 10. Track

| Field | Datatype | Requirement | Access |
| --- | --- | --- | --- |
|**id** | integer | Required | Public |
|**name** | string | Optional | Public |
|**description** | string | Optional | Public |
|**color** | string | Optional | Public |
|**track_image_url** | string | Optional | Public |
|**location** | string | Optional | Public |
|**sessions** | Array[**TrackSession**] | Optional | Public |

#### TrackSession

| Field | Datatype | Requirement |
| --- | --- | --- |
|**id** | integer | Required |
|**title** | string | Optional |
