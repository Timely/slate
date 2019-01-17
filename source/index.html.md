---
title: Timely Internal API doc
language_tabs:
  - json: JSON
  - shell: cURL
---

Use Timely API to integrate with your apps

Timely API helps you integrate your application with Timely. Following are the list of API’s available. For any help or support email support@timelyapp.com
# AppObjects



## create calendar


### Request

#### Endpoint

```plaintext
PUT /1.1/apps/6414/objects/6414
Accept: application/json
Content-Type: application/json
Authorization: Bearer d218d46d836917b8305185db316c287864adb51e37d0ef584e5da47962a6cf23
```

`PUT /1.1/apps/:app_id/objects/:id`

#### Parameters


```json
{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"true"},{"name":"anup@timelyapp.com","etag":"1457979055759000","object_id":"anup@timelyapp.com","project_id":"2","auto_import":"false"}]},"objects":{"object_id":70208242413960}}
```


| Name | Description |
|:-----|:------------|
| app_objects *required* | Object attributes |
| app_objects[objects] *required* | Calendar attributes |
| objects[name] *required* | Object name |
| objects[etag] *required* | Object etag |
| objects[object_id]  | Object id |
| objects[project_id]  | Object project id |
| objects[auto_import]  | Auto import hours |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","name":"Fixtures","etag":"\"1482740512308000\"","integrated":true,"updated_at":"2019-01-16T16:54:10+01:00","auto_import":true,"project_id":1},{"object_id":"anup@timelyapp.com","name":"anup@timelyapp.com","etag":"\"1457979055759000\"","integrated":true,"updated_at":"2019-01-16T16:54:10+01:00","auto_import":false,"project_id":2},{"object_id":"timelyapp.com_3qaj6ftsa591l17r3hgra4hn08@group.calendar.google.com","name":"Calendar Sync Test","etag":"\"1457979057839000\"","integrated":false},{"object_id":"timelyapp.com_5q9rqm0eqi68rb1r101o3bv1jo@group.calendar.google.com","name":"Timely Trials","etag":"\"1457979060008000\"","integrated":false},{"object_id":"timelyapp.com_uhbt0atpl6irjbcugvs1kee5j4@group.calendar.google.com","name":"Calendar Sync II","etag":"\"1457979061137000\"","integrated":false},{"object_id":"timelyapp.com_hhm9t83jh3rkdn6ni429g1tc4o@group.calendar.google.com","name":"Calendar integration","etag":"\"1469680526663000\"","integrated":false},{"object_id":"timelyapp.com_7veb7perd2p238atf210cps1n8@group.calendar.google.com","name":"Calendar Sync III","etag":"\"1457979056819000\"","integrated":false}]
```



```shell
curl "https://api.timelyapp.com/1.1/apps/6414/objects/6414" -d '{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"true"},{"name":"anup@timelyapp.com","etag":"1457979055759000","object_id":"anup@timelyapp.com","project_id":"2","auto_import":"false"}]},"objects":{"object_id":70208242413960}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer d218d46d836917b8305185db316c287864adb51e37d0ef584e5da47962a6cf23" \
	-H "Cookie: "
```
## delete calendar


### Request

#### Endpoint

```plaintext
PUT /1.1/apps/6416/objects/6416
Accept: application/json
Content-Type: application/json
Authorization: Bearer 189afc3b541bccbeb393a2e422117900bcc56ee83bdc9831409f83f9f1201638
```

`PUT /1.1/apps/:app_id/objects/:id`

#### Parameters


```json
{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"false"},{"name":"anup@timelyapp.com","etag":"1457979055759000","project_id":"2","auto_import":"false"}]},"objects":{"object_id":70208255496860}}
```


| Name | Description |
|:-----|:------------|
| app_objects *required* | Object attributes |
| app_objects[objects] *required* | Calendar attributes |
| objects[name] *required* | Object name |
| objects[etag] *required* | Object etag |
| objects[object_id]  | Object id |
| objects[project_id]  | Object project id |
| objects[auto_import]  | Auto import hours |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","name":"Fixtures","etag":"\"1482740512308000\"","integrated":true,"updated_at":"2019-01-16T16:54:10+01:00","auto_import":false,"project_id":1},{"object_id":"anup@timelyapp.com","name":"anup@timelyapp.com","etag":"\"1457979055759000\"","integrated":false},{"object_id":"timelyapp.com_3qaj6ftsa591l17r3hgra4hn08@group.calendar.google.com","name":"Calendar Sync Test","etag":"\"1457979057839000\"","integrated":false},{"object_id":"timelyapp.com_5q9rqm0eqi68rb1r101o3bv1jo@group.calendar.google.com","name":"Timely Trials","etag":"\"1457979060008000\"","integrated":false},{"object_id":"timelyapp.com_uhbt0atpl6irjbcugvs1kee5j4@group.calendar.google.com","name":"Calendar Sync II","etag":"\"1457979061137000\"","integrated":false},{"object_id":"timelyapp.com_hhm9t83jh3rkdn6ni429g1tc4o@group.calendar.google.com","name":"Calendar integration","etag":"\"1469680526663000\"","integrated":false},{"object_id":"timelyapp.com_7veb7perd2p238atf210cps1n8@group.calendar.google.com","name":"Calendar Sync III","etag":"\"1457979056819000\"","integrated":false}]
```



```shell
curl "https://api.timelyapp.com/1.1/apps/6416/objects/6416" -d '{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"false"},{"name":"anup@timelyapp.com","etag":"1457979055759000","project_id":"2","auto_import":"false"}]},"objects":{"object_id":70208255496860}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 189afc3b541bccbeb393a2e422117900bcc56ee83bdc9831409f83f9f1201638" \
	-H "Cookie: "
```
## list objects


### Request

#### Endpoint

```plaintext
GET /1.1/apps/6412/objects
Accept: application/json
Content-Type: application/json
Authorization: Bearer 0ed33d5b44af127addb8d08ccba15e1485dee7cd7c3f5dc10b7311392fdbe401
```

`GET /1.1/apps/:app_id/objects`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","name":"Fixtures","etag":"\"1482740512308000\"","integrated":false},{"object_id":"anup@timelyapp.com","name":"anup@timelyapp.com","etag":"\"1457979055759000\"","integrated":false},{"object_id":"timelyapp.com_3qaj6ftsa591l17r3hgra4hn08@group.calendar.google.com","name":"Calendar Sync Test","etag":"\"1457979057839000\"","integrated":false},{"object_id":"timelyapp.com_5q9rqm0eqi68rb1r101o3bv1jo@group.calendar.google.com","name":"Timely Trials","etag":"\"1457979060008000\"","integrated":false},{"object_id":"timelyapp.com_uhbt0atpl6irjbcugvs1kee5j4@group.calendar.google.com","name":"Calendar Sync II","etag":"\"1457979061137000\"","integrated":false},{"object_id":"timelyapp.com_hhm9t83jh3rkdn6ni429g1tc4o@group.calendar.google.com","name":"Calendar integration","etag":"\"1469680526663000\"","integrated":false},{"object_id":"timelyapp.com_7veb7perd2p238atf210cps1n8@group.calendar.google.com","name":"Calendar Sync III","etag":"\"1457979056819000\"","integrated":false}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/apps/6412/objects" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 0ed33d5b44af127addb8d08ccba15e1485dee7cd7c3f5dc10b7311392fdbe401" \
	-H "Cookie: "
```
## list objects


### Request

#### Endpoint

```plaintext
GET /1.1/apps/6413/objects
Accept: application/json
Content-Type: application/json
Authorization: Bearer bc718416eb672ee6bbbfdb551f283e194737e4eca60ae7edd4942a77963f1bdb
```

`GET /1.1/apps/:app_id/objects`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"object_id":"AQMkADAwATM0MDAAMS1mYWNmLTc0NTctMDACLTAwCgBGAAADRBR9GFAcnECww3HfNZ02uQcA5oz8Ye3dNUGORWPMT6HxsAAAAgEGAAAA5oz8Ye3dNUGORWPMT6HxsAAAAhT1AAAA","name":"Calendar","etag":"5oz8Ye3dNUGORWPMT6HxsAAAAAAV7g==","integrated":false},{"object_id":"AQMkADAwATM0MDAAMS1mYWNmLTc0NTctMDACLTAwCgBGAAADRBR9GFAcnECww3HfNZ02uQcA5oz8Ye3dNUGORWPMT6HxsAAAAgEGAAAA5oz8Ye3dNUGORWPMT6HxsAAAAhT2AAAA","name":"United States holidays","etag":"5oz8Ye3dNUGORWPMT6HxsAAAAAAV7w==","integrated":false},{"object_id":"AQMkADAwATM0MDAAMS1mYWNmLTc0NTctMDACLTAwCgBGAAADRBR9GFAcnECww3HfNZ02uQcA5oz8Ye3dNUGORWPMT6HxsAAAAgEGAAAA5oz8Ye3dNUGORWPMT6HxsAAAAhT4AAAA","name":"Birthdays","etag":"5oz8Ye3dNUGORWPMT6HxsAAAAAAV8Q==","integrated":false},{"object_id":"AQMkADAwATM0MDAAMS1mYWNmLTc0NTctMDACLTAwCgBGAAADRBR9GFAcnECww3HfNZ02uQcA5oz8Ye3dNUGORWPMT6HxsAAAAgEGAAAA5oz8Ye3dNUGORWPMT6HxsAAAABSmEdwAAAA=","name":"timely calendar","etag":"5oz8Ye3dNUGORWPMT6HxsAAAFKjA1Q==","integrated":false},{"object_id":"AQMkADAwATM0MDAAMS1mYWNmLTc0NTctMDACLTAwCgBGAAADRBR9GFAcnECww3HfNZ02uQcA5oz8Ye3dNUGORWPMT6HxsAAAAgEGAAAA5oz8Ye3dNUGORWPMT6HxsAAAABzE_nIAAAA=","name":"pravin cal","etag":"5oz8Ye3dNUGORWPMT6HxsAAAHMiPOg==","integrated":false}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/apps/6413/objects" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer bc718416eb672ee6bbbfdb551f283e194737e4eca60ae7edd4942a77963f1bdb" \
	-H "Cookie: "
```
## update calendar


### Request

#### Endpoint

```plaintext
PUT /1.1/apps/6415/objects/6415
Accept: application/json
Content-Type: application/json
Authorization: Bearer 9c127cef928ed19a7d52fcad4082b045656aa6a9dcfda1018b019d7ef3d8f478
```

`PUT /1.1/apps/:app_id/objects/:id`

#### Parameters


```json
{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"false"},{"name":"anup@timelyapp.com","etag":"1457979055759000","object_id":"anup@timelyapp.com","project_id":"2","auto_import":"true"}]},"objects":{"object_id":70208168076800}}
```


| Name | Description |
|:-----|:------------|
| app_objects *required* | Object attributes |
| app_objects[objects] *required* | Calendar attributes |
| objects[name] *required* | Object name |
| objects[etag] *required* | Object etag |
| objects[object_id]  | Object id |
| objects[project_id]  | Object project id |
| objects[auto_import]  | Auto import hours |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","name":"Fixtures","etag":"\"1482740512308000\"","integrated":true,"updated_at":"2019-01-16T16:54:10+01:00","auto_import":false,"project_id":1},{"object_id":"anup@timelyapp.com","name":"anup@timelyapp.com","etag":"\"1457979055759000\"","integrated":true,"updated_at":"2019-01-16T16:54:10+01:00","auto_import":true,"project_id":2},{"object_id":"timelyapp.com_3qaj6ftsa591l17r3hgra4hn08@group.calendar.google.com","name":"Calendar Sync Test","etag":"\"1457979057839000\"","integrated":false},{"object_id":"timelyapp.com_5q9rqm0eqi68rb1r101o3bv1jo@group.calendar.google.com","name":"Timely Trials","etag":"\"1457979060008000\"","integrated":false},{"object_id":"timelyapp.com_uhbt0atpl6irjbcugvs1kee5j4@group.calendar.google.com","name":"Calendar Sync II","etag":"\"1457979061137000\"","integrated":false},{"object_id":"timelyapp.com_hhm9t83jh3rkdn6ni429g1tc4o@group.calendar.google.com","name":"Calendar integration","etag":"\"1469680526663000\"","integrated":false},{"object_id":"timelyapp.com_7veb7perd2p238atf210cps1n8@group.calendar.google.com","name":"Calendar Sync III","etag":"\"1457979056819000\"","integrated":false}]
```



```shell
curl "https://api.timelyapp.com/1.1/apps/6415/objects/6415" -d '{"app_objects":{"objects":[{"name":"Fixtures","etag":"1482740512308000","object_id":"timelyapp.com_rfldr8c53ov8j3pvmgipg64008@group.calendar.google.com","project_id":"1","auto_import":"false"},{"name":"anup@timelyapp.com","etag":"1457979055759000","object_id":"anup@timelyapp.com","project_id":"2","auto_import":"true"}]},"objects":{"object_id":70208168076800}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 9c127cef928ed19a7d52fcad4082b045656aa6a9dcfda1018b019d7ef3d8f478" \
	-H "Cookie: "
```
# Apps



## delete connected app


### Request

#### Endpoint

```plaintext
DELETE /1.1/apps/10312/connected/6434
Accept: application/json
Content-Type: application/json
Authorization: Bearer 5881f1749125e0acae9bb16dc3d2470009c683d2673103fa53a73e6add069109
```

`DELETE /1.1/apps/:app_id/connected/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/apps/10312/connected/6434" -d '' -X DELETE \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 5881f1749125e0acae9bb16dc3d2470009c683d2673103fa53a73e6add069109" \
	-H "Cookie: "
```
## list apps


### Request

#### Endpoint

```plaintext
GET /1.1/apps
Accept: application/json
Content-Type: application/json
Authorization: Bearer c2aecf67a62d6c7ded99506e8f5a497e2f92377f7722e074462ffeb299f22700
```

`GET /1.1/apps`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"app_id":10298,"id":"google_calendar","display_name":"Display name","description":"Get all your calendar events imported directly into Timely as\n    planned time.","layout":"list","integrated":true,"disconnected_integrations_count":0,"connected_integrations_count":1,"first_created_at":"2019-01-16T16:54:11+01:00","last_imported_at":null,"platforms":["ios","android"],"summary":"Auto-import recurring, multi-day and full-day calendar events into Timely to avoid duplicating effort. We don’t send any data back, so edits you make in Timely won’t change your Google Calendar entries.","provider":"Google","provider_url":"https://calendar.google.com","screenshots":["screenshots/google_calendar/screenshot1.png"],"logo_path":"apps_logo/google_calendar.png","authorize_url":"/auth/google_calendar/authorize","connected_apps_url":"/apps/10298/connected"},{"app_id":10299,"id":"office365","display_name":"Display name","description":"Get all your calendar events imported directly into Timely as\n    planned time.","layout":"list","integrated":true,"disconnected_integrations_count":0,"connected_integrations_count":1,"first_created_at":"2019-01-16T16:54:11+01:00","last_imported_at":null,"platforms":["ios","android"],"summary":"Auto-import recurring, multi-day and full-day calendar events into Timely to avoid duplicating effort. We don’t send any data back, so edits you make in Timely won’t change your Office 365 entries.","provider":"Microsoft","provider_url":"https://products.office.com/en-us/business/explore-office-365-for-business","screenshots":["screenshots/office365/screenshot1.png"],"logo_path":"apps_logo/office365.png","authorize_url":"/auth/office365/authorize","connected_apps_url":"/apps/10299/connected"},{"app_id":10300,"id":"gmail","display_name":"Display name","description":"Get all your calendar events imported directly into Timely as\n    planned time.","layout":"list","integrated":true,"disconnected_integrations_count":0,"connected_integrations_count":1,"first_created_at":"2019-01-16T16:54:11+01:00","last_imported_at":null,"platforms":["ios","android"],"summary":"See exactly how much time you spend managing your Gmail each day. All the emails you send in a day will automatically appear in your private Memory timeline for easy reference.","provider":"Google","provider_url":"https://gmail.com/","screenshots":["screenshots/gmail/screenshot1.png"],"logo_path":"apps_logo/gmail.png","authorize_url":"/auth/gmail/authorize","connected_apps_url":"/apps/10300/connected"},{"app_id":10301,"id":"moves_app","display_name":"Display name","description":"Get all your calendar events imported directly into Timely as\n    planned time.","layout":"list","integrated":true,"disconnected_integrations_count":1,"connected_integrations_count":1,"first_created_at":"2019-01-14T16:54:11+01:00","last_imported_at":"2019-01-15T16:54:11+01:00","platforms":["ios","android"],"summary":"Track off-site meetings, travel for work and the time you spend in the office every day. Essential for on-the-go professionals who need to record where they’ve been and for how long.","provider":"Facebook","provider_url":"https://moves-app.com/","screenshots":["screenshots/moves_app/screenshot1.png","screenshots/moves_app/screenshot2.png"],"logo_path":"apps_logo/moves_app.png","authorize_url":"/auth/moves_app/authorize","connected_apps_url":"/apps/10301/connected"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/apps" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer c2aecf67a62d6c7ded99506e8f5a497e2f92377f7722e074462ffeb299f22700" \
	-H "Cookie: "
```
## list connected apps


### Request

#### Endpoint

```plaintext
GET /1.1/apps/10302/connected
Accept: application/json
Content-Type: application/json
Authorization: Bearer 4448f3a88f596549044b9722c50cfbdd3ac3498a6a0924d9fb0f11f65b478b4b
```

`GET /1.1/apps/:app_id/connected`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":6422,"name":"Tom Hardy","email":"tom@timelyapp.com","active":true,"created_at":"2019-01-16T16:54:11+01:00","updated_at":"2019-01-16T16:54:11+01:00","last_imported_at":null,"disconnected":false,"disconnected_reason":null,"objects":true,"objects_type":"calendars","objects_url":"/1.1/apps/6422/objects"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/apps/10302/connected" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 4448f3a88f596549044b9722c50cfbdd3ac3498a6a0924d9fb0f11f65b478b4b" \
	-H "Cookie: "
```
## list connected apps


### Request

#### Endpoint

```plaintext
GET /1.1/apps/10308/connected
Accept: application/json
Content-Type: application/json
Authorization: Bearer 2479646f5a075f3d41ca923f89ee78c7e1e583d3ff492b98a0bed0a4d545deb7
```

`GET /1.1/apps/:app_id/connected`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":6429,"name":"Tom Hardy","email":"tom@timelyapp.com","active":true,"created_at":"2019-01-16T16:54:11+01:00","updated_at":"2019-01-16T16:54:11+01:00","last_imported_at":null,"disconnected":false,"disconnected_reason":null,"objects":false}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/apps/10308/connected" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 2479646f5a075f3d41ca923f89ee78c7e1e583d3ff492b98a0bed0a4d545deb7" \
	-H "Cookie: "
```
# BudgetRecurrences



## month recurrence list


### Request

#### Endpoint

```plaintext
GET /1.1/22841/projects/22557/budget_recurrences
Accept: application/json
Content-Type: application/json
Authorization: Bearer c4a0af5a0b850215c505b41c7efe12454d21b5dbc8cb79c4a6c1f95eabc5048f
```

`GET /1.1/:account_id/projects/:project_id/budget_recurrences`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"recur":"August 2018","start_date":"2018-08-01","end_date":"2018-08-31","totals":{"duration":{"hours":4,"minutes":0,"seconds":0,"formatted":"04:00","total_hours":4.0,"total_seconds":14400,"total_minutes":240},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"cost":{"fractional":40000,"formatted":"$400.00","amount":400.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0}}},{"recur":"September 2018","start_date":"2018-09-01","end_date":"2018-09-30","totals":{"duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":50000,"formatted":"$500.00","amount":500.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"October 2018","start_date":"2018-10-01","end_date":"2018-10-31","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"November 2018","start_date":"2018-11-01","end_date":"2018-11-30","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22841/projects/22557/budget_recurrences" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer c4a0af5a0b850215c505b41c7efe12454d21b5dbc8cb79c4a6c1f95eabc5048f" \
	-H "Cookie: "
```
## month recurrence list


### Request

#### Endpoint

```plaintext
GET /1.1/22842/projects/22558/budget_recurrences
Accept: application/json
Content-Type: application/json
Authorization: Bearer 3e750218628582768293dadbfc5fea8fcb27382a28720e37f6e03fb9e5f1742d
```

`GET /1.1/:account_id/projects/:project_id/budget_recurrences`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"recur":"August 2018","start_date":"2018-08-01","end_date":"2018-08-31","totals":{"duration":{"hours":4,"minutes":0,"seconds":0,"formatted":"04:00","total_hours":4.0,"total_seconds":14400,"total_minutes":240},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"cost":{"fractional":40000,"formatted":"$400.00","amount":400.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0}}},{"recur":"September 2018","start_date":"2018-09-01","end_date":"2018-09-30","totals":{"duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":50000,"formatted":"$500.00","amount":500.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"October 2018","start_date":"2018-10-01","end_date":"2018-10-31","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"November 2018","start_date":"2018-11-01","end_date":"2018-11-30","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"September 2019","start_date":"2019-09-01","end_date":"2019-09-30","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":50000,"formatted":"$500.00","amount":500.0}}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22842/projects/22558/budget_recurrences" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 3e750218628582768293dadbfc5fea8fcb27382a28720e37f6e03fb9e5f1742d" \
	-H "Cookie: "
```
## week recurrence list


### Request

#### Endpoint

```plaintext
GET /1.1/22839/projects/22555/budget_recurrences
Accept: application/json
Content-Type: application/json
Authorization: Bearer 5e3b52c4e68de41b3988600131c6883aa66070729bdbc2527bc7e269ce74e6bf
```

`GET /1.1/:account_id/projects/:project_id/budget_recurrences`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"recur":"33 2018","start_date":"2018-08-13","end_date":"2018-08-19","totals":{"duration":{"hours":4,"minutes":0,"seconds":0,"formatted":"04:00","total_hours":4.0,"total_seconds":14400,"total_minutes":240},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"cost":{"fractional":40000,"formatted":"$400.00","amount":400.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0}}},{"recur":"35 2018","start_date":"2018-08-27","end_date":"2018-09-02","totals":{"duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":50000,"formatted":"$500.00","amount":500.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"40 2018","start_date":"2018-10-01","end_date":"2018-10-07","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"45 2018","start_date":"2018-11-05","end_date":"2018-11-11","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22839/projects/22555/budget_recurrences" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 5e3b52c4e68de41b3988600131c6883aa66070729bdbc2527bc7e269ce74e6bf" \
	-H "Cookie: "
```
## week recurrence list


### Request

#### Endpoint

```plaintext
GET /1.1/22840/projects/22556/budget_recurrences
Accept: application/json
Content-Type: application/json
Authorization: Bearer 18551f1133f0a432662fd455361a710b62a0e88efb34ad40b50fd100edb47f82
```

`GET /1.1/:account_id/projects/:project_id/budget_recurrences`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"recur":"33 2018","start_date":"2018-08-13","end_date":"2018-08-19","totals":{"duration":{"hours":4,"minutes":0,"seconds":0,"formatted":"04:00","total_hours":4.0,"total_seconds":14400,"total_minutes":240},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"cost":{"fractional":40000,"formatted":"$400.00","amount":400.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0}}},{"recur":"35 2018","start_date":"2018-08-27","end_date":"2018-09-02","totals":{"duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":50000,"formatted":"$500.00","amount":500.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"40 2018","start_date":"2018-10-01","end_date":"2018-10-07","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"45 2018","start_date":"2018-11-05","end_date":"2018-11-11","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":8,"minutes":0,"seconds":0,"formatted":"08:00","total_hours":8.0,"total_seconds":28800,"total_minutes":480},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":80000,"formatted":"$800.00","amount":800.0}}},{"recur":"37 2019","start_date":"2019-09-09","end_date":"2019-09-15","totals":{"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300},"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":50000,"formatted":"$500.00","amount":500.0}}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22840/projects/22556/budget_recurrences" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 18551f1133f0a432662fd455361a710b62a0e88efb34ad40b50fd100edb47f82" \
	-H "Cookie: "
```
# Discard Entries



## create


### Request

#### Endpoint

```plaintext
POST /1.1/22848/suggested_entries/discard
Accept: application/json
Content-Type: application/json
Authorization: Bearer 94b4f3392c0c59de095f814616af53c14cbcbcf2d5c4762a469be924b531ea84
```

`POST /1.1/:account_id/suggested_entries/discard`

#### Parameters


```json
{"discard_entries":{"entry_ids":[11675]}}
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22848/suggested_entries/discard" -d '{"discard_entries":{"entry_ids":[11675]}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 94b4f3392c0c59de095f814616af53c14cbcbcf2d5c4762a469be924b531ea84" \
	-H "Cookie: "
```
## index


### Request

#### Endpoint

```plaintext
GET /1.1/22847/suggested_entries/discarded
Accept: application/json
Content-Type: application/json
Authorization: Bearer 32d26a61e0eb701519e2fd69d60008ec83189877e4e69e3b08b316ecbfd15057
```

`GET /1.1/:account_id/suggested_entries/discarded`

#### Parameters


```json
{}: 
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":null,"to":null,"description":"hour.rb (~/code/github/timely/app/models) - VIM1","entry_ids":[11674],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","projects":[],"importance":0.8,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22847/suggested_entries/discarded" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 32d26a61e0eb701519e2fd69d60008ec83189877e4e69e3b08b316ecbfd15057" \
	-H "Cookie: "
```
## remove


### Request

#### Endpoint

```plaintext
DELETE /1.1/22849/suggested_entries/discard
Accept: application/json
Content-Type: application/json
Authorization: Bearer 98de40bc17bb02669a7c184181b1fc2998a70b481e93ccbac9e36ea990a3eb77
```

`DELETE /1.1/:account_id/suggested_entries/discard`

#### Parameters


```json
{"discard_entries":{"entry_ids":[11678]}}
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22849/suggested_entries/discard" -d '{"discard_entries":{"entry_ids":[11678]}}' -X DELETE \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 98de40bc17bb02669a7c184181b1fc2998a70b481e93ccbac9e36ea990a3eb77" \
	-H "Cookie: "
```
# Duration



## duration


### Request

#### Endpoint

```plaintext
GET /1.1/entries/durations?entry_ids=11679%2C11680
Accept: application/json
Content-Type: application/json
Authorization: Bearer 37adae96d59f634408f3add63c5fbd218d3c22a58903e4ae3e286e5963250fd0
```

`GET /1.1/entries/durations`

#### Parameters


```json
entry_ids: 11679,11680
```


| Name | Description |
|:-----|:------------|
| entry_ids  | Comma separated list of entry ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"hours":4,"minutes":30,"seconds":0,"formatted":"04:30","total_hours":4.5,"total_seconds":16200,"total_minutes":270}
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries/durations?entry_ids=11679%2C11680" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 37adae96d59f634408f3add63c5fbd218d3c22a58903e4ae3e286e5963250fd0" \
	-H "Cookie: "
```
## duration


### Request

#### Endpoint

```plaintext
GET /1.1/entries/durations?entry_ids=11681%2C11682
Accept: application/json
Content-Type: application/json
Authorization: Bearer af143ed06f72e3892a9d01f701dea270b15a9c10458ea62b921270233bda7df6
```

`GET /1.1/entries/durations`

#### Parameters


```json
entry_ids: 11681,11682
```


| Name | Description |
|:-----|:------------|
| entry_ids  | Comma separated list of entry ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210}
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries/durations?entry_ids=11681%2C11682" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer af143ed06f72e3892a9d01f701dea270b15a9c10458ea62b921270233bda7df6" \
	-H "Cookie: "
```
## duration


### Request

#### Endpoint

```plaintext
GET /1.1/entries/durations?entry_ids=11683%2C11684
Accept: application/json
Content-Type: application/json
Authorization: Bearer 54ee97f77ff0d498d02d0ba37467c084534f9a1e61474ea0a0a9d5a5f230828b
```

`GET /1.1/entries/durations`

#### Parameters


```json
entry_ids: 11683,11684
```


| Name | Description |
|:-----|:------------|
| entry_ids  | Comma separated list of entry ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"hours":5,"minutes":0,"seconds":0,"formatted":"05:00","total_hours":5.0,"total_seconds":18000,"total_minutes":300}
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries/durations?entry_ids=11683%2C11684" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 54ee97f77ff0d498d02d0ba37467c084534f9a1e61474ea0a0a9d5a5f230828b" \
	-H "Cookie: "
```
# Entries



## update deleted


### Request

#### Endpoint

```plaintext
DELETE /1.1/entries/11696
Accept: application/json
Content-Type: application/json
Authorization: Bearer ae82881c796402d5e3b4f0fe61f8de2d4842aaae8d20861aa77031ac4296ecfa
```

`DELETE /1.1/entries/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/entries/11696" -d '' -X DELETE \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer ae82881c796402d5e3b4f0fe61f8de2d4842aaae8d20861aa77031ac4296ecfa" \
	-H "Cookie: "
```
## with date


### Request

#### Endpoint

```plaintext
GET /1.1/entries?date=2019-01-18
Accept: application/json
Content-Type: application/json
Authorization: Bearer 17a08cb9005d0f62d4791a552fcc08dd44bfaf9475e92b9b717c5a712fd7312c
```

`GET /1.1/entries`

#### Parameters


```json
date: 2019-01-18
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 100) |
| date  | Date to retrieve records (Default current date) |
| order  | Order to retrieve records (Default updated_at DESC) |
| entry_ids  | Retrieve specific entry_ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":11690,"type":"google_calendar","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"Meeting","note":"Discuss about future","description":"16:54 - 20:24 • Discuss about future","date":"2019-01-18","from":"2019-01-16T16:54:18+01:00","to":"2019-01-16T20:24:18+01:00","entry_type":null,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"at":"2019-01-16T16:54:18+01:00","extra_attributes":[],"icon":"google_calendar.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","icon_fallback_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","url":null}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries?date=2019-01-18" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 17a08cb9005d0f62d4791a552fcc08dd44bfaf9475e92b9b717c5a712fd7312c" \
	-H "Cookie: "
```
## with default params


### Request

#### Endpoint

```plaintext
GET /1.1/entries
Accept: application/json
Content-Type: application/json
Authorization: Bearer c33b3b0f8de6f2da116365508e7c3eb6bf3dadf91c92975b3fcce25d772ed520
```

`GET /1.1/entries`

#### Parameters



| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 100) |
| date  | Date to retrieve records (Default current date) |
| order  | Order to retrieve records (Default updated_at DESC) |
| entry_ids  | Retrieve specific entry_ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":11685,"type":"macOS","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","description":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":"2019-01-16T16:54:18+01:00","to":"2019-01-16T20:24:18+01:00","entry_type":null,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"at":"2019-01-16T16:54:18+01:00","extra_attributes":[{"name":"application","value":"MacVim"},{"name":"detail","value":""}],"icon":"mac_vim.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","url":null},{"id":11686,"type":"google_calendar","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"Meeting","note":"Discuss about future","description":"16:54 - 20:24 • Discuss about future","date":"2019-01-16","from":"2019-01-16T16:54:18+01:00","to":"2019-01-16T20:24:18+01:00","entry_type":null,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"at":"2019-01-16T16:54:18+01:00","extra_attributes":[],"icon":"google_calendar.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","icon_fallback_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","url":null}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer c33b3b0f8de6f2da116365508e7c3eb6bf3dadf91c92975b3fcce25d772ed520" \
	-H "Cookie: "
```
## with entry_ids


### Request

#### Endpoint

```plaintext
GET /1.1/entries?entry_ids=11691%2C11693
Accept: application/json
Content-Type: application/json
Authorization: Bearer 2cfcdf22339b382b621562bb297bce2a414c126563009dc4a6fa287c5e6deacc
```

`GET /1.1/entries`

#### Parameters


```json
entry_ids: 11691,11693
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 100) |
| date  | Date to retrieve records (Default current date) |
| order  | Order to retrieve records (Default updated_at DESC) |
| entry_ids  | Retrieve specific entry_ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":11691,"type":"macOS","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","description":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":"2019-01-16T16:54:18+01:00","to":"2019-01-16T20:24:18+01:00","entry_type":null,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"at":"2019-01-16T16:54:18+01:00","extra_attributes":[{"name":"application","value":"MacVim"},{"name":"detail","value":""}],"icon":"mac_vim.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","url":null},{"id":11693,"type":"google_calendar","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"Meeting","note":"Discuss about future","description":"16:54 - 20:24 • Discuss about future","date":"2019-01-18","from":"2019-01-16T16:54:18+01:00","to":"2019-01-16T20:24:18+01:00","entry_type":null,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"at":"2019-01-16T16:54:18+01:00","extra_attributes":[],"icon":"google_calendar.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","icon_fallback_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","url":null}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/entries?entry_ids=11691%2C11693" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 2cfcdf22339b382b621562bb297bce2a414c126563009dc4a6fa287c5e6deacc" \
	-H "Cookie: "
```
# Events



## hour with id


### Request

#### Endpoint

```plaintext
GET /1.1/22870/events/15297
Accept: application/json
Content-Type: application/json
Authorization: Bearer 1224a83713f2b76dc6e338131762daeca15059ace7f006423fb6239aea92ff3f
```

`GET /1.1/:account_id/events/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":15297,"uid":"65f4abf5-80f3-49cf-a7b9-241bde0d5bbb","user":{"id":52841,"email":"quentin@timelyapp.com","name":"Quintin Duponde","active":false,"day_view_onboarded":true,"memory_onboarded":true,"created_at":1547654063,"updated_at":1547654063,"default_hour_rate":0.0,"last_received_memories_date":null,"sign_in_count":null,"external_id":null},"project":{"id":22576,"active":true,"account_id":22870,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17038,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654063,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":0,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"labels":[]},"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"estimated_duration":{"hours":4,"minutes":0,"seconds":0,"formatted":"04:00","total_hours":4.0,"total_seconds":14400,"total_minutes":240},"cost":{"fractional":17500,"formatted":"$175.00","amount":175.0},"estimated_cost":{"fractional":20000,"formatted":"$200.00","amount":200.0},"day":"2019-01-16","note":"Notes for testing with some random #hash in it.","sequence":1,"estimated":false,"timer_state":"default","timer_started_on":0,"timer_stopped_on":0,"label_ids":[],"user_ids":[],"updated_at":1547654063,"created_at":1547654063,"created_from":"Web","updated_from":"Web","billed":false,"to":"2019-01-16T20:24:23+01:00","from":"2019-01-16T16:54:23+01:00","deleted":false,"hour_rate":50.0,"hour_rate_in_cents":5000.0,"creator_id":null,"updater_id":null,"external_id":null,"entry_ids":[],"suggestion_id":null}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22870/events/15297" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 1224a83713f2b76dc6e338131762daeca15059ace7f006423fb6239aea92ff3f" \
	-H "Cookie: "
```
## not found


### Request

#### Endpoint

```plaintext
GET /1.1/22871/events/12345
Accept: application/json
Content-Type: application/json
Authorization: Bearer 8f33b799ecc0615304b6209c9f0e8d4dd8871064ca6382dc651facda55e42289
```

`GET /1.1/:account_id/events/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
404 Not Found
```


```json
{"errors":{"message":"Not found"}}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22871/events/12345" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 8f33b799ecc0615304b6209c9f0e8d4dd8871064ca6382dc651facda55e42289" \
	-H "Cookie: "
```
# Plans



## plans for appstore


### Request

#### Endpoint

```plaintext
GET /1.2/private/plans
Accept: application/json
Content-Type: application/json
Authorization: Bearer 8bf2793d762eff5b19be79d6b03bcae37a61c21d613e319823542d28210d9ca1
```

`GET /1.2/private/plans`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":28,"code":"essential","name":"Essential","users_limit":0,"projects_limit":0,"grace_period":950400,"trial":1209600,"price":15,"user_price":15,"default":false,"enabled":true,"version":4,"cycle":"M","term":2592000,"campaign":"default","appstore":true,"playstore":true,"features":[{"name":"memories","days":60},{"name":"billing","days":-1}]},{"id":34,"code":"solo_v1","name":"Solo","users_limit":1,"projects_limit":3,"grace_period":950400,"trial":1209600,"price":8,"user_price":8,"default":false,"enabled":true,"version":4,"cycle":"M","term":2592000,"campaign":"default","appstore":true,"playstore":true,"features":[{"name":"memories","days":30}]}]
```



```shell
curl -g "https://api.timelyapp.com/1.2/private/plans" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 8bf2793d762eff5b19be79d6b03bcae37a61c21d613e319823542d28210d9ca1" \
	-H "Cookie: "
```
## plans for playstore


### Request

#### Endpoint

```plaintext
GET /1.2/private/plans
Accept: application/json
Content-Type: application/json
Authorization: Bearer 1ddf10731f4a0617a557ac6ed9c4a8be5de474e38a0b6c71eba67c916b6cd121
```

`GET /1.2/private/plans`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":28,"code":"essential","name":"Essential","users_limit":0,"projects_limit":0,"grace_period":950400,"trial":1209600,"price":15,"user_price":15,"default":false,"enabled":true,"version":4,"cycle":"M","term":2592000,"campaign":"default","appstore":true,"playstore":true,"features":[{"name":"memories","days":60},{"name":"billing","days":-1}]},{"id":34,"code":"solo_v1","name":"Solo","users_limit":1,"projects_limit":3,"grace_period":950400,"trial":1209600,"price":8,"user_price":8,"default":false,"enabled":true,"version":4,"cycle":"M","term":2592000,"campaign":"default","appstore":true,"playstore":true,"features":[{"name":"memories","days":30}]}]
```



```shell
curl -g "https://api.timelyapp.com/1.2/private/plans" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 1ddf10731f4a0617a557ac6ed9c4a8be5de474e38a0b6c71eba67c916b6cd121" \
	-H "Cookie: "
```
# ProjectSubscriptions



## create project subscribers


### Request

#### Endpoint

```plaintext
POST /1.1/22881/projects/22587/subscribe
Accept: application/json
Content-Type: application/json
Authorization: Bearer ed4688de170f6277ff2dbcbef9ac2326f262a3b32c67a3dd7c3b251bece7c0c9
```

`POST /1.1/:account_id/projects/:project_id/subscribe`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22881/projects/22587/subscribe" -d '' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer ed4688de170f6277ff2dbcbef9ac2326f262a3b32c67a3dd7c3b251bece7c0c9" \
	-H "Cookie: "
```
## delete project subscribers


### Request

#### Endpoint

```plaintext
DELETE /1.1/22882/projects/22588/subscribe
Accept: application/json
Content-Type: application/json
Authorization: Bearer 80d7a37e3577d11ee706fc0c5c9686b1aef45fec6a0cdd516678e4b17de1dfe3
```

`DELETE /1.1/:account_id/projects/:project_id/subscribe`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22882/projects/22588/subscribe" -d '' -X DELETE \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 80d7a37e3577d11ee706fc0c5c9686b1aef45fec6a0cdd516678e4b17de1dfe3" \
	-H "Cookie: "
```
## list subscribed users


### Request

#### Endpoint

```plaintext
GET /1.1/22878/projects/22584/subscribers
Accept: application/json
Content-Type: application/json
Authorization: Bearer ade42ba05cca93d7d1a095c451a246cd53aa36e6d0c2283123f34aadc6f4e48b
```

`GET /1.1/:account_id/projects/:project_id/subscribers`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":52857,"email":"quentin@timelyapp.com","name":"Quintin Duponde","avatar":{"timeline":"https://www.gravatar.com/avatar/341d68b864aca41aadfc9d9ec221e0c1?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_timeline.jpg&s=","medium_retina":"https://www.gravatar.com/avatar/341d68b864aca41aadfc9d9ec221e0c1?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_medium_retina.jpg&s=50","medium":"https://www.gravatar.com/avatar/341d68b864aca41aadfc9d9ec221e0c1?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_medium.jpg&s="}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22878/projects/22584/subscribers" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer ade42ba05cca93d7d1a095c451a246cd53aa36e6d0c2283123f34aadc6f4e48b" \
	-H "Cookie: "
```
## show project subscription


### Request

#### Endpoint

```plaintext
GET /1.1/22879/projects/22585/subscription
Accept: application/json
Content-Type: application/json
Authorization: Bearer dffb510db36ddc0dc9f9aac91a986dfd16c0696dc867575afbf53d18a5af48f2
```

`GET /1.1/:account_id/projects/:project_id/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"project_budget_progress":true}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22879/projects/22585/subscription" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer dffb510db36ddc0dc9f9aac91a986dfd16c0696dc867575afbf53d18a5af48f2" \
	-H "Cookie: "
```
## show project subscription


### Request

#### Endpoint

```plaintext
GET /1.1/22880/projects/22586/subscription
Accept: application/json
Content-Type: application/json
Authorization: Bearer 076fc1694cdade5d10d4b41a609557360dfabda4d00a2a880f1aad8f47885319
```

`GET /1.1/:account_id/projects/:project_id/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"project_budget_progress":false}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22880/projects/22586/subscription" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 076fc1694cdade5d10d4b41a609557360dfabda4d00a2a880f1aad8f47885319" \
	-H "Cookie: "
```
# Projects



## Search all projects with query


### Request

#### Endpoint

```plaintext
GET /1.1/22894/projects/search?q=Jasper
Accept: application/json
Content-Type: application/json
Authorization: Bearer 2bb5953d5a578b9cb59d6d422408282344b1c4d839324a8341092682be2c82d8
```

`GET /1.1/:account_id/projects/search`

#### Parameters


```json
q: Jasper
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| q *required* | Search query (min 2 characters) |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":22607,"name":"Jasper","color":"67a3bc","active":true,"client":{"id":17062,"name":"Timely","active":true,"external_id":null}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22894/projects/search?q=Jasper" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 2bb5953d5a578b9cb59d6d422408282344b1c4d839324a8341092682be2c82d8" \
	-H "Cookie: "
```
## active


### Request

#### Endpoint

```plaintext
GET /1.1/22892/projects?filter=active
Accept: application/json
Content-Type: application/json
Authorization: Bearer aa877ca88fc6fa63adc2dcf83e1a70605fb7d4f8ee8f954b95e4b187add20306
```

`GET /1.1/:account_id/projects`

#### Parameters


```json
filter: active
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| order  | Reverses the sorting order |
| filter  | Specifies which records to retrieve, default is current users active projects |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":22602,"active":true,"account_id":22892,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17060,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654068,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52885,"hour_rate":100.0,"hour_rate_in_cents":10000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"labels":[]}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22892/projects?filter=active" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer aa877ca88fc6fa63adc2dcf83e1a70605fb7d4f8ee8f954b95e4b187add20306" \
	-H "Cookie: "
```
## all


### Request

#### Endpoint

```plaintext
GET /1.1/22891/projects?filter=all
Accept: application/json
Content-Type: application/json
Authorization: Bearer dfa8b347a3cfda19d36bf37b1e9452a198936b18995d62959eb9a25ee714bb10
```

`GET /1.1/:account_id/projects`

#### Parameters


```json
filter: all
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| order  | Reverses the sorting order |
| filter  | Specifies which records to retrieve, default is current users active projects |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":22600,"active":true,"account_id":22891,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17059,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654067,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52883,"hour_rate":100.0,"hour_rate_in_cents":10000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"labels":[]},{"id":22601,"active":false,"account_id":22891,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17059,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654067,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52883,"hour_rate":100.0,"hour_rate_in_cents":10000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"labels":[]}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22891/projects?filter=all" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer dfa8b347a3cfda19d36bf37b1e9452a198936b18995d62959eb9a25ee714bb10" \
	-H "Cookie: "
```
## archived


### Request

#### Endpoint

```plaintext
GET /1.1/22893/projects?filter=archived
Accept: application/json
Content-Type: application/json
Authorization: Bearer 4eb085b13eafaa4c1ecdbf708b3255d20d7015d777848023a111f735603c47ee
```

`GET /1.1/:account_id/projects`

#### Parameters


```json
filter: archived
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| order  | Reverses the sorting order |
| filter  | Specifies which records to retrieve, default is current users active projects |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":22605,"active":false,"account_id":22893,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17061,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654068,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52887,"hour_rate":100.0,"hour_rate_in_cents":10000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"labels":[]}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22893/projects?filter=archived" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 4eb085b13eafaa4c1ecdbf708b3255d20d7015d777848023a111f735603c47ee" \
	-H "Cookie: "
```
## create project


### Request

#### Endpoint

```plaintext
POST /1.1/22899/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer 9c40dffc186a67320d399de85c6e4ef9f290504241d3c59a8ddaaecb1e62314b
```

`POST /1.1/:account_id/projects`

#### Parameters


```json
{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17067,"budget_type":"M","budget":300,"users":[{"user_id":52899}],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"","recur_until":"archived"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |
| project[name] *required* | Project name |
| project[company_id] *required* | Company id |
| project[color] *required* | Project color |
| project[hour_rate]  | Project hour_rate |
| project[rate_type]  | Project rate_type |
| project[budget]  | Project budget |
| project[budget_type]  | Project budget type |
| project[billable]  | Project billable |
| project[active]  | Project active/archived |
| project[external_id]  | Project external_id |
| project[budget_scope]  | Project budget scope |
| project[users] *required* | Project users |
| project[labels]  | Project labels |
| project[budget_recurrence]  | Project budget recurrence rule |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
201 Created
```


```json
{"id":22629,"active":true,"account_id":22899,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17067,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654069,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52899,"hour_rate":50.0,"hour_rate_in_cents":5000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":null,"recur_until":"archived","days_count":0}}
```



```shell
curl "https://api.timelyapp.com/1.1/22899/projects" -d '{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17067,"budget_type":"M","budget":300,"users":[{"user_id":52899}],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"","recur_until":"archived"}}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 9c40dffc186a67320d399de85c6e4ef9f290504241d3c59a8ddaaecb1e62314b" \
	-H "Cookie: "
```
## create project


### Request

#### Endpoint

```plaintext
POST /1.1/22896/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer a5615ed572df67e4f251e93bb112ace5ca452d71bda3de68577f3a5226f2a375
```

`POST /1.1/:account_id/projects`

#### Parameters


```json
{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17064,"users":[{"user_id":52893}],"labels":[{"label_id":5238},{"label_id":5239,"budget":0,"required":false}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |
| project[name] *required* | Project name |
| project[company_id] *required* | Company id |
| project[color] *required* | Project color |
| project[hour_rate]  | Project hour_rate |
| project[rate_type]  | Project rate_type |
| project[budget]  | Project budget |
| project[budget_type]  | Project budget type |
| project[billable]  | Project billable |
| project[active]  | Project active/archived |
| project[external_id]  | Project external_id |
| project[budget_scope]  | Project budget scope |
| project[users] *required* | Project users |
| project[labels]  | Project labels |
| project[budget_recurrence]  | Project budget recurrence rule |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
201 Created
```


```json
{"id":22626,"active":true,"account_id":22896,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17064,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654069,"label_ids":[5238,5239],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":0,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52893,"hour_rate":50.0,"hour_rate_in_cents":5000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5238,"budget":null,"required":false},{"label_id":5239,"budget":0,"required":false}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22896/projects" -d '{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17064,"users":[{"user_id":52893}],"labels":[{"label_id":5238},{"label_id":5239,"budget":0,"required":false}]}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer a5615ed572df67e4f251e93bb112ace5ca452d71bda3de68577f3a5226f2a375" \
	-H "Cookie: "
```
## create project


### Request

#### Endpoint

```plaintext
POST /1.1/22897/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer add912fff4df8700e5db963efc2bec7922a1b0a0552d86d0a083e3f7f0b5608d
```

`POST /1.1/:account_id/projects`

#### Parameters


```json
{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17065,"budget_type":"M","budget_scope":"tag","budget":300,"users":[{"user_id":52895}],"labels":[{"label_id":5240,"budget":100,"required":false},{"label_id":5241,"budget":200,"required":true}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |
| project[name] *required* | Project name |
| project[company_id] *required* | Company id |
| project[color] *required* | Project color |
| project[hour_rate]  | Project hour_rate |
| project[rate_type]  | Project rate_type |
| project[budget]  | Project budget |
| project[budget_type]  | Project budget type |
| project[billable]  | Project billable |
| project[active]  | Project active/archived |
| project[external_id]  | Project external_id |
| project[budget_scope]  | Project budget scope |
| project[users] *required* | Project users |
| project[labels]  | Project labels |
| project[budget_recurrence]  | Project budget recurrence rule |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
201 Created
```


```json
{"id":22627,"active":true,"account_id":22897,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17065,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654069,"label_ids":[5240,5241],"required_label_ids":[5241],"team_ids":[],"external_id":null,"budget_scope":"tag","budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52895,"hour_rate":50.0,"hour_rate_in_cents":5000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5240,"budget":100,"required":false},{"label_id":5241,"budget":200,"required":true}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22897/projects" -d '{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17065,"budget_type":"M","budget_scope":"tag","budget":300,"users":[{"user_id":52895}],"labels":[{"label_id":5240,"budget":100,"required":false},{"label_id":5241,"budget":200,"required":true}]}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer add912fff4df8700e5db963efc2bec7922a1b0a0552d86d0a083e3f7f0b5608d" \
	-H "Cookie: "
```
## create project


### Request

#### Endpoint

```plaintext
POST /1.1/22898/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer 4ac0693c8b9ee58f8a11df0ca767c120bbebf37ff81d1657c2a19fe7931bab77
```

`POST /1.1/:account_id/projects`

#### Parameters


```json
{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17066,"budget_type":"M","budget":300,"users":[{"user_id":52897}],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |
| project[name] *required* | Project name |
| project[company_id] *required* | Company id |
| project[color] *required* | Project color |
| project[hour_rate]  | Project hour_rate |
| project[rate_type]  | Project rate_type |
| project[budget]  | Project budget |
| project[budget_type]  | Project budget type |
| project[billable]  | Project billable |
| project[active]  | Project active/archived |
| project[external_id]  | Project external_id |
| project[budget_scope]  | Project budget scope |
| project[users] *required* | Project users |
| project[labels]  | Project labels |
| project[budget_recurrence]  | Project budget recurrence rule |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
201 Created
```


```json
{"id":22628,"active":true,"account_id":22898,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17066,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654069,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52897,"hour_rate":50.0,"hour_rate_in_cents":5000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date","days_count":365}}
```



```shell
curl "https://api.timelyapp.com/1.1/22898/projects" -d '{"project":{"name":"Timely","rate_type":"project","hour_rate":50.0,"active":true,"deleted":false,"currency_code":"usd","color":"67a3bc","company_id":17066,"budget_type":"M","budget":300,"users":[{"user_id":52897}],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date"}}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 4ac0693c8b9ee58f8a11df0ca767c120bbebf37ff81d1657c2a19fe7931bab77" \
	-H "Cookie: "
```
## mine with projects


### Request

#### Endpoint

```plaintext
GET /1.1/22889/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer 722d5670bf1dcd8fc75dbbf47834f8cdb5830360a15f4551c9645da596475107
```

`GET /1.1/:account_id/projects`

#### Parameters



| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| order  | Reverses the sorting order |
| filter  | Specifies which records to retrieve, default is current users active projects |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":22596,"active":true,"account_id":22889,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17057,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654067,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[{"user_id":52879,"hour_rate":100.0,"hour_rate_in_cents":10000.0}],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"labels":[]}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22889/projects" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 722d5670bf1dcd8fc75dbbf47834f8cdb5830360a15f4551c9645da596475107" \
	-H "Cookie: "
```
## mine without projects


### Request

#### Endpoint

```plaintext
GET /1.1/22890/projects
Accept: application/json
Content-Type: application/json
Authorization: Bearer fff5950c42cf962b263d64fbf3178239d2984d68f4e8bbf1632eadc9cdab89a4
```

`GET /1.1/:account_id/projects`

#### Parameters



| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| order  | Reverses the sorting order |
| filter  | Specifies which records to retrieve, default is current users active projects |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22890/projects" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer fff5950c42cf962b263d64fbf3178239d2984d68f4e8bbf1632eadc9cdab89a4" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22909/projects/22639
Accept: application/json
Content-Type: application/json
Authorization: Bearer 78e7077f1207f12a69d4488a379f10c752ea6ad6dc84778bfb8b8c486f87a952
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":300}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22639,"active":true,"account_id":22909,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17077,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654072,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date","days_count":365}}
```



```shell
curl "https://api.timelyapp.com/1.1/22909/projects/22639" -d '{"project":{"budget_type":"M","budget":300}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 78e7077f1207f12a69d4488a379f10c752ea6ad6dc84778bfb8b8c486f87a952" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22900/projects/22630
Accept: application/json
Content-Type: application/json
Authorization: Bearer 43a6baeb68f57de0610a780e038c9f868017a7ddef355ea9fda82f650c0be611
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"labels":[{"label_id":5242},{"label_id":5243,"budget":0,"required":false}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22630,"active":true,"account_id":22900,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17068,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654070,"label_ids":[5242,5243],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5242,"budget":null,"required":false},{"label_id":5243,"budget":0,"required":false}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22900/projects/22630" -d '{"project":{"labels":[{"label_id":5242},{"label_id":5243,"budget":0,"required":false}]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 43a6baeb68f57de0610a780e038c9f868017a7ddef355ea9fda82f650c0be611" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22901/projects/22631
Accept: application/json
Content-Type: application/json
Authorization: Bearer 5904b1fa5dc6989b4548c3cc537f705dc442f10c14a8e1f4b492ab4d2143496a
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget_scope":"tag","budget":200,"labels":[{"label_id":5244,"budget":100,"required":true},{"label_id":5245,"budget":100,"required":true}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22631,"active":true,"account_id":22901,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17069,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654070,"label_ids":[5244,5245],"required_label_ids":[5244,5245],"team_ids":[],"external_id":null,"budget_scope":"tag","budget":200,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5244,"budget":100,"required":true},{"label_id":5245,"budget":100,"required":true}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22901/projects/22631" -d '{"project":{"budget_type":"M","budget_scope":"tag","budget":200,"labels":[{"label_id":5244,"budget":100,"required":true},{"label_id":5245,"budget":100,"required":true}]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 5904b1fa5dc6989b4548c3cc537f705dc442f10c14a8e1f4b492ab4d2143496a" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22902/projects/22632
Accept: application/json
Content-Type: application/json
Authorization: Bearer d3ce3667b45798d16306cfad99adeece89cac4ce2dd132181682498353eba207
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget_scope":"tag","budget":400,"labels":[{"label_id":5246,"budget":100,"required":true},{"label_id":5247,"budget":100,"required":true},{"label_id":5248,"budget":200,"required":true}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22632,"active":true,"account_id":22902,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17070,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654070,"label_ids":[5246,5247,5248],"required_label_ids":[5246,5247,5248],"team_ids":[],"external_id":null,"budget_scope":"tag","budget":400,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5246,"budget":100,"required":true},{"label_id":5247,"budget":100,"required":true},{"label_id":5248,"budget":200,"required":true}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22902/projects/22632" -d '{"project":{"budget_type":"M","budget_scope":"tag","budget":400,"labels":[{"label_id":5246,"budget":100,"required":true},{"label_id":5247,"budget":100,"required":true},{"label_id":5248,"budget":200,"required":true}]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer d3ce3667b45798d16306cfad99adeece89cac4ce2dd132181682498353eba207" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22903/projects/22633
Accept: application/json
Content-Type: application/json
Authorization: Bearer 7f02909d90ffb0cff938852dd2e72cab886bfac8bc4c9f36712f3df34eff3bf8
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget_scope":"tag","budget":400,"labels":[{"label_id":5251,"budget":400,"required":true}]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22633,"active":true,"account_id":22903,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17071,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654071,"label_ids":[5251],"required_label_ids":[5251],"team_ids":[],"external_id":null,"budget_scope":"tag","budget":400,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[{"label_id":5251,"budget":400,"required":true}]}
```



```shell
curl "https://api.timelyapp.com/1.1/22903/projects/22633" -d '{"project":{"budget_type":"M","budget_scope":"tag","budget":400,"labels":[{"label_id":5251,"budget":400,"required":true}]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 7f02909d90ffb0cff938852dd2e72cab886bfac8bc4c9f36712f3df34eff3bf8" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22904/projects/22634
Accept: application/json
Content-Type: application/json
Authorization: Bearer 008065443482405f90649b254e9df96d9613923f7d6f1eb0ca3c0bc62fa5beea
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":400,"labels":[]}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22634,"active":true,"account_id":22904,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17072,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654071,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":400,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[]}
```



```shell
curl "https://api.timelyapp.com/1.1/22904/projects/22634" -d '{"project":{"budget_type":"M","budget":400,"labels":[]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 008065443482405f90649b254e9df96d9613923f7d6f1eb0ca3c0bc62fa5beea" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22905/projects/22635
Accept: application/json
Content-Type: application/json
Authorization: Bearer 81e36d14937ff2d20ff82631af56832b3f6dc130c3946de8f7922d30c9bec91b
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22635,"active":true,"account_id":22905,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17073,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654071,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date","days_count":365}}
```



```shell
curl "https://api.timelyapp.com/1.1/22905/projects/22635" -d '{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":"2019-09-21","recur_until":"end_date"}}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 81e36d14937ff2d20ff82631af56832b3f6dc130c3946de8f7922d30c9bec91b" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22906/projects/22636
Accept: application/json
Content-Type: application/json
Authorization: Bearer b0090416651a054499804501aeadc5bbd2f74f212ab043b674214b7216fb834d
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"start_date":"2018-09-21","end_date":"","recur_until":"archived"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22636,"active":true,"account_id":22906,"name":"Timely","color":"67a3bc","rate_type":"project","client":{"id":17074,"name":"Timely","active":true,"external_id":null},"billable":true,"updated_at":1547654071,"label_ids":[],"required_label_ids":[],"team_ids":[],"external_id":null,"budget_scope":null,"budget":300,"budget_type":"M","hour_rate":50.0,"hour_rate_in_cents":5000.0,"users":[],"cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"estimated_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"estimated_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"billed_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"billed_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"unbilled_cost":{"fractional":0,"formatted":"$0.00","amount":0.0},"unbilled_duration":{"hours":0,"minutes":0,"seconds":0,"formatted":"00:00","total_hours":0.0,"total_seconds":0,"total_minutes":0},"first_logged_on":null,"last_logged_on":null,"labels":[],"budget_recurrence":{"recur":"week","start_date":"2018-09-21","end_date":null,"recur_until":"archived","days_count":0}}
```



```shell
curl "https://api.timelyapp.com/1.1/22906/projects/22636" -d '{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"start_date":"2018-09-21","end_date":"","recur_until":"archived"}}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer b0090416651a054499804501aeadc5bbd2f74f212ab043b674214b7216fb834d" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22907/projects/22637
Accept: application/json
Content-Type: application/json
Authorization: Bearer 78f775f0b6bb30da8af22cbfa45b4273a56a610d4b6039b664e628f4222b7994
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"recur":"month"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
422 Unprocessable Entity
```


```json
{"errors":{"budget_recurrence":[{"start_date":["invalid date"],"end_date":["invalid date","invalid date"],"recur":["cannot be updated"]}]}}
```



```shell
curl "https://api.timelyapp.com/1.1/22907/projects/22637" -d '{"project":{"budget_type":"M","budget":300,"budget_recurrence":{"recur":"month"}}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 78f775f0b6bb30da8af22cbfa45b4273a56a610d4b6039b664e628f4222b7994" \
	-H "Cookie: "
```
## update project


### Request

#### Endpoint

```plaintext
PUT /1.1/22908/projects/22638
Accept: application/json
Content-Type: application/json
Authorization: Bearer 7b269352dfac1817f5a2dea7efe707f48fdddbdd36a8b83e3a3943d72d2e5123
```

`PUT /1.1/:account_id/projects/:id`

#### Parameters


```json
{"project":{"budget_type":"M","budget":400,"budget_recurrence":{"recur":"week"}}}
```


| Name | Description |
|:-----|:------------|
| project *required* | Project attributes |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
422 Unprocessable Entity
```


```json
{"errors":{"budget_recurrence":[{"start_date":["invalid date"],"end_date":["invalid date","invalid date"]}],"budget":["cannot be changed"]}}
```



```shell
curl "https://api.timelyapp.com/1.1/22908/projects/22638" -d '{"project":{"budget_type":"M","budget":400,"budget_recurrence":{"recur":"week"}}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 7b269352dfac1817f5a2dea7efe707f48fdddbdd36a8b83e3a3943d72d2e5123" \
	-H "Cookie: "
```
# Projects

Project object contains all project details of a logged account. With this api you can retrieve a specific project or the list of all projects, update, create and delete a project.



## Invalid request


### Request

#### Endpoint

```plaintext
GET /1.1/22886/projects/111
Accept: application/json
Content-Type: application/json
Authorization: Bearer 5861e22e0ba880a26de949148c45f48fa8d353af7cc517e9d6bf03b0e439c37f
```

`GET /1.1/:account_id/projects/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| account_id  | Account id for which project to be retrieved |
| id  | The id of the project to be retrieved |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
404 Not Found
```


```json
{"errors":{"message":"Not found"}}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22886/projects/111" -X GET \
	-H "Host: api.timelyapp.com" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 5861e22e0ba880a26de949148c45f48fa8d353af7cc517e9d6bf03b0e439c37f" \
	-H "Cookie: "
```
# Suggested Entries



## index


### Request

#### Endpoint

```plaintext
GET /1.1/22911/suggested_entries?date=2019-01-16
Accept: application/json
Content-Type: application/json
Authorization: Bearer 67f0d84c3c8cd955a71aeae86613f53dcac626b2846d0c6df7e111c95be268e4
```

`GET /1.1/:account_id/suggested_entries`

#### Parameters


```json
date: 2019-01-16
```


| Name | Description |
|:-----|:------------|
| date  | Suggested entries for date (Default today) |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"title":"Meeting","note":"Discuss about future","date":"2019-01-16","from":null,"to":null,"description":"14:00 - 15:00 • Discuss about future","entry_ids":[11697],"icon_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","icon_fallback_url":"/assets/apps_logo/google_calendar-cf4817a3d9bb86a0f2371b67fc49106074b36e8ee05a1932c595181dbd9aecd0.png","projects":[],"importance":0,"duration":{"hours":1,"minutes":0,"seconds":0,"formatted":"01:00","total_hours":1.0,"total_seconds":3600,"total_minutes":60}},{"title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":null,"to":null,"description":"hour.rb (~/code/github/timely/app/models) - VIM1","entry_ids":[11698,11699],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","projects":[{"project_id":22641,"accuracy":0.8,"count":2}],"importance":0.8,"duration":{"hours":7,"minutes":0,"seconds":0,"formatted":"07:00","total_hours":7.0,"total_seconds":25200,"total_minutes":420}},{"title":"Congratulations on winning $100000","note":"You won $100000, share your netbanking details","date":"2019-01-16","from":null,"to":null,"description":" • You won $100000, share your netbanking details","entry_ids":[11700],"icon_url":"/assets/apps_logo/gmail-507255a1d62e38cfb7bcc5a531337868c05cd6924f1183cdd4f08b0cb4d7efdf.png","icon_fallback_url":"/assets/apps_logo/gmail-507255a1d62e38cfb7bcc5a531337868c05cd6924f1183cdd4f08b0cb4d7efdf.png","projects":[{"project_id":22641,"accuracy":0.8,"count":1}],"importance":0,"duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210}}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22911/suggested_entries?date=2019-01-16" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 67f0d84c3c8cd955a71aeae86613f53dcac626b2846d0c6df7e111c95be268e4" \
	-H "Cookie: "
```
## update


### Request

#### Endpoint

```plaintext
PUT /1.1/22912/suggested_entries
Accept: application/json
Content-Type: application/json
Authorization: Bearer 900b5b970c444a2f9ae031de50489baa095f5001a18c719e9b177ca16c0a9205
```

`PUT /1.1/:account_id/suggested_entries`

#### Parameters


```json
{"suggested_entries":{"entries":[{"entry_id":11702,"project_id":22643}]}}
```


| Name | Description |
|:-----|:------------|
| suggested_entries  | Suggested Entries to update |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22912/suggested_entries" -d '{"suggested_entries":{"entries":[{"entry_id":11702,"project_id":22643}]}}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 900b5b970c444a2f9ae031de50489baa095f5001a18c719e9b177ca16c0a9205" \
	-H "Cookie: "
```
# Suggested Hours



## default


### Request

#### Endpoint

```plaintext
GET /1.1/22913/suggested_hours?date=2019-01-16
Accept: application/json
Content-Type: application/json
Authorization: Bearer 85a309f54f01a4aafc1ac8482f55be09ca12e259ecbe87d8140fe2eaadc1ad07
```

`GET /1.1/:account_id/suggested_hours`

#### Parameters


```json
date: 2019-01-16
```


| Name | Description |
|:-----|:------------|
| date  | Suggested entries for date (Default today) |
| since  | Suggested entries form specific date to until |
| until  | Suggested entries until specific date from since |
| suggested_hour_ids  | Suggested hours for specific ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":2484,"owner":{"id":22028,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22644,"date":"2019-01-16","to":"2019-01-16T20:24:33+01:00","from":"2019-01-16T16:54:33+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:33+01:00","suggested_entry_ids":[11705,11706],"version":"0.2.0","updated_at":"2019-01-16T16:54:33+01:00"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22913/suggested_hours?date=2019-01-16" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 85a309f54f01a4aafc1ac8482f55be09ca12e259ecbe87d8140fe2eaadc1ad07" \
	-H "Cookie: "
```
## show


### Request

#### Endpoint

```plaintext
GET /1.1/22919/suggested_hours/2496
Accept: application/json
Content-Type: application/json
Authorization: Bearer 28fe63f7995628641b4d935490666a1d882321cc947ca3e376e11f6ee7cd882b
```

`GET /1.1/:account_id/suggested_hours/:suggested_hour_id`

#### Parameters


```json
{}: 
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":2496,"owner":{"id":22034,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22650,"date":"2019-01-16","to":"2019-01-16T20:24:35+01:00","from":"2019-01-16T16:54:35+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:35+01:00","suggested_entry_ids":[11729,11730],"version":"0.2.0","updated_at":"2019-01-16T16:54:35+01:00"}
```



```shell
curl -g "https://api.timelyapp.com/1.1/22919/suggested_hours/2496" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 28fe63f7995628641b4d935490666a1d882321cc947ca3e376e11f6ee7cd882b" \
	-H "Cookie: "
```
## since and until


### Request

#### Endpoint

```plaintext
GET /1.1/22915/suggested_hours?date=2019-01-16&amp;since=2019-01-14&amp;until=2019-01-16
Accept: application/json
Content-Type: application/json
Authorization: Bearer b1a5a38e97273176d87625f9372e906fb9c657149b75361d04e6436397da35af
```

`GET /1.1/:account_id/suggested_hours`

#### Parameters


```json
date: 2019-01-16
since: 2019-01-14
until: 2019-01-16
```


| Name | Description |
|:-----|:------------|
| date  | Suggested entries for date (Default today) |
| since  | Suggested entries form specific date to until |
| until  | Suggested entries until specific date from since |
| suggested_hour_ids  | Suggested hours for specific ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":2488,"owner":{"id":22030,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22646,"date":"2019-01-16","to":"2019-01-16T20:24:34+01:00","from":"2019-01-16T16:54:34+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:34+01:00","suggested_entry_ids":[11713,11714],"version":"0.2.0","updated_at":"2019-01-16T16:54:34+01:00"},{"id":2489,"owner":{"id":22030,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22646,"date":"2019-01-14","to":"2019-01-16T20:24:34+01:00","from":"2019-01-16T16:54:34+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:34+01:00","suggested_entry_ids":[11715],"version":"0.2.0","updated_at":"2019-01-16T16:54:34+01:00"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22915/suggested_hours?date=2019-01-16&since=2019-01-14&until=2019-01-16" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer b1a5a38e97273176d87625f9372e906fb9c657149b75361d04e6436397da35af" \
	-H "Cookie: "
```
## suggested hour ids


### Request

#### Endpoint

```plaintext
GET /1.1/22916/suggested_hours?date=2019-01-16&amp;suggested_hour_ids=2490
Accept: application/json
Content-Type: application/json
Authorization: Bearer 379e165718ae787aee179ba75d0f7987a207d0bea2e50ea9dbc33a6f0bbc9dc6
```

`GET /1.1/:account_id/suggested_hours`

#### Parameters


```json
date: 2019-01-16
suggested_hour_ids: 2490
```


| Name | Description |
|:-----|:------------|
| date  | Suggested entries for date (Default today) |
| since  | Suggested entries form specific date to until |
| until  | Suggested entries until specific date from since |
| suggested_hour_ids  | Suggested hours for specific ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":2490,"owner":{"id":22031,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22647,"date":"2019-01-16","to":"2019-01-16T20:24:34+01:00","from":"2019-01-16T16:54:34+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:34+01:00","suggested_entry_ids":[11717,11718],"version":"0.2.0","updated_at":"2019-01-16T16:54:34+01:00"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22916/suggested_hours?date=2019-01-16&suggested_hour_ids=2490" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 379e165718ae787aee179ba75d0f7987a207d0bea2e50ea9dbc33a6f0bbc9dc6" \
	-H "Cookie: "
```
## update


### Request

#### Endpoint

```plaintext
PUT /1.1/22917/suggested_hours/2492
Accept: application/json
Content-Type: application/json
Authorization: Bearer cedcd55b7511ca09770c677bfca1f1acf7b801741f73a0cf909ca064eab50cd0
```

`PUT /1.1/:account_id/suggested_hours/:suggested_hour_id`

#### Parameters


```json
{}
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":2492,"owner":{"id":22032,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22648,"date":"2019-01-16","to":"2019-01-16T20:24:34+01:00","from":"2019-01-16T16:54:34+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"dismissed","source":"prediction","created_at":"2019-01-16T16:54:34+01:00","suggested_entry_ids":[11721,11722],"version":"0.2.0","updated_at":"2019-01-16T16:54:34+01:00"}
```



```shell
curl "https://api.timelyapp.com/1.1/22917/suggested_hours/2492" -d '{}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer cedcd55b7511ca09770c677bfca1f1acf7b801741f73a0cf909ca064eab50cd0" \
	-H "Cookie: "
```
## update


### Request

#### Endpoint

```plaintext
PUT /1.1/22918/suggested_hours/decline
Accept: application/json
Content-Type: application/json
Authorization: Bearer a01d1dabab69383153ec7fef71280dbeab73eb3f538da0e02551c08b2bcbbfcb
```

`PUT /1.1/:account_id/suggested_hours/decline`

#### Parameters


```json
{"suggested_hour_ids":[2494]}
```


| Name | Description |
|:-----|:------------|
| suggested_hour_ids  | Suggested hour ids to decline |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22918/suggested_hours/decline" -d '{"suggested_hour_ids":[2494]}' -X PUT \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer a01d1dabab69383153ec7fef71280dbeab73eb3f538da0e02551c08b2bcbbfcb" \
	-H "Cookie: "
```
## with date


### Request

#### Endpoint

```plaintext
GET /1.1/22914/suggested_hours?date=2019-01-14
Accept: application/json
Content-Type: application/json
Authorization: Bearer c7b63f5dbc7721bc530065cd66abad8f3094bbd3049c2299d58b5e155063c86d
```

`GET /1.1/:account_id/suggested_hours`

#### Parameters


```json
date: 2019-01-14
```


| Name | Description |
|:-----|:------------|
| date  | Suggested entries for date (Default today) |
| since  | Suggested entries form specific date to until |
| until  | Suggested entries until specific date from since |
| suggested_hour_ids  | Suggested hours for specific ids |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":2487,"owner":{"id":22029,"email":"notifications@timelyapp.com","name":"Timely","avatar":{"timeline":"/assets/timely_user_avatar_timeline.png","medium_retina":"/assets/timely_user_avatar_medium_retina.png","medium":"/assets/timely_user_avatar_medium.png"}},"project_id":22645,"date":"2019-01-14","to":"2019-01-16T20:24:33+01:00","from":"2019-01-16T16:54:33+01:00","note":"Notes for testing with some random #hash in it.","duration":{"hours":3,"minutes":30,"seconds":0,"formatted":"03:30","total_hours":3.5,"total_seconds":12600,"total_minutes":210},"status":"pending","source":"prediction","created_at":"2019-01-16T16:54:33+01:00","suggested_entry_ids":[11711],"version":"0.2.0","updated_at":"2019-01-16T16:54:33+01:00"}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22914/suggested_hours?date=2019-01-14" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer c7b63f5dbc7721bc530065cd66abad8f3094bbd3049c2299d58b5e155063c86d" \
	-H "Cookie: "
```
# Training Entries



## create


### Request

#### Endpoint

```plaintext
POST /1.1/22926/training_entries
Accept: application/json
Content-Type: application/json
Authorization: Bearer 96f6f41d46f397ac85e9e04a1b30b1525460d5c76c435ce793f99887db8b7f9d
```

`POST /1.1/:account_id/training_entries`

#### Parameters


```json
{"training_entries":{"entries":[{"entry_id":11736,"project_id":22656}]}}
```


| Name | Description |
|:-----|:------------|
| training_entries  | Training Entries to create/update |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22926/training_entries" -d '{"training_entries":{"entries":[{"entry_id":11736,"project_id":22656}]}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 96f6f41d46f397ac85e9e04a1b30b1525460d5c76c435ce793f99887db8b7f9d" \
	-H "Cookie: "
```
## list


### Request

#### Endpoint

```plaintext
GET /1.1/22925/training_entries?date=2019-01-16
Accept: application/json
Content-Type: application/json
Authorization: Bearer b723765b366a289b8db26d9afdccc85f0229455339278bce70399554c57f0836
```

`GET /1.1/:account_id/training_entries`

#### Parameters


```json
date: 2019-01-16
```


| Name | Description |
|:-----|:------------|
| date  | Training entries for date (Default today) |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":11733,"type":"macOS","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","description":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":"2019-01-16T10:00:00+01:00","to":"2019-01-16T12:00:00+01:00","entry_type":null,"duration":{"hours":2,"minutes":0,"seconds":0,"formatted":"02:00","total_hours":2.0,"total_seconds":7200,"total_minutes":120},"at":"2019-01-16T10:00:00+01:00","extra_attributes":[{"name":"application","value":"MacVim"},{"name":"detail","value":""}],"icon":"mac_vim.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","url":null,"score":0.8},{"id":11734,"type":"macOS","uid":"3283efc2-e58a-43f7-8e43-9045e4c72b0c","title":"MacVim","note":"hour.rb (~/code/github/timely/app/models) - VIM1","description":"hour.rb (~/code/github/timely/app/models) - VIM1","date":"2019-01-16","from":"2019-01-16T14:00:00+01:00","to":"2019-01-16T15:00:00+01:00","entry_type":null,"duration":{"hours":1,"minutes":0,"seconds":0,"formatted":"01:00","total_hours":1.0,"total_seconds":3600,"total_minutes":60},"at":"2019-01-16T14:00:00+01:00","extra_attributes":[{"name":"application","value":"MacVim"},{"name":"detail","value":""}],"icon":"mac_vim.png","color":"rgba(86,210,255,0.30)","sub_entries":[],"icon_url":"/timeline_app_logos/macvim.png","icon_fallback_url":"/assets/timeline_app_logos/default-ec843823aa8fa1357fc233024c47d3f11adcd237244768bcc7bb9672b77bd8ac.png","url":null,"score":0.6}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22925/training_entries?date=2019-01-16" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer b723765b366a289b8db26d9afdccc85f0229455339278bce70399554c57f0836" \
	-H "Cookie: "
```
## update


### Request

#### Endpoint

```plaintext
POST /1.1/22927/training_entries
Accept: application/json
Content-Type: application/json
Authorization: Bearer b88ae402b5fe1b70006fd72f1a790714a1f7bb1717e3f5966feb85dba777fcbb
```

`POST /1.1/:account_id/training_entries`

#### Parameters


```json
{"training_entries":{"entries":[{"entry_id":11738,"project_id":22657},{"entry_id":11737,"project_id":22657}]}}
```


| Name | Description |
|:-----|:------------|
| training_entries  | Training Entries to create/update |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{}
```



```shell
curl "https://api.timelyapp.com/1.1/22927/training_entries" -d '{"training_entries":{"entries":[{"entry_id":11738,"project_id":22657},{"entry_id":11737,"project_id":22657}]}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer b88ae402b5fe1b70006fd72f1a790714a1f7bb1717e3f5966feb85dba777fcbb" \
	-H "Cookie: "
```
# Upgrade



## upgrade account plan from web account


### Request

#### Endpoint

```plaintext
POST /1.2/private/accounts/22938/upgrade
Accept: application/json
Content-Type: application/json
Authorization: Bearer bbb666be59d7552906ee589f4aee12ab7d6a5cafbdcc9a5c0cc133a5c0b6e954
```

`POST /1.2/private/accounts/:account_id/upgrade`

#### Parameters


```json
{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"essential"}}
```


| Name | Description |
|:-----|:------------|
| next_charge  | Next charge date |
| plan  | plan code |
| appstore_transaction_id  | Appstore original transaction id |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
422 Unprocessable Entity
```


```json
{"errors":{"message":"Upgrade via appstore failed."}}
```



```shell
curl "https://api.timelyapp.com/1.2/private/accounts/22938/upgrade" -d '{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"essential"}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer bbb666be59d7552906ee589f4aee12ab7d6a5cafbdcc9a5c0cc133a5c0b6e954" \
	-H "Cookie: "
```
## upgrade account plan from web account


### Request

#### Endpoint

```plaintext
POST /1.2/private/accounts/22940/upgrade
Accept: application/json
Content-Type: application/json
Authorization: Bearer 066bfcb7838d5b4ec9195fe3b5f1b0e68cd157f7a7da55ab40d1ea5deaf76786
```

`POST /1.2/private/accounts/:account_id/upgrade`

#### Parameters


```json
{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"solo_v1"}}
```


| Name | Description |
|:-----|:------------|
| next_charge  | Next charge date |
| plan  | plan code |
| appstore_transaction_id  | Appstore original transaction id |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
422 Unprocessable Entity
```


```json
{"errors":{"message":"Plan upgrade failed. You need to delete some projects,           Solo plan supports only  project."}}
```



```shell
curl "https://api.timelyapp.com/1.2/private/accounts/22940/upgrade" -d '{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"solo_v1"}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 066bfcb7838d5b4ec9195fe3b5f1b0e68cd157f7a7da55ab40d1ea5deaf76786" \
	-H "Cookie: "
```
## upgrade account plan to essential


### Request

#### Endpoint

```plaintext
POST /1.2/private/accounts/22937/upgrade
Accept: application/json
Content-Type: application/json
Authorization: Bearer 26f5391e9882e69620b584085fb8279a45f4ba0f56867b7622e5e6ada16d48e0
```

`POST /1.2/private/accounts/:account_id/upgrade`

#### Parameters


```json
{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"essential"}}
```


| Name | Description |
|:-----|:------------|
| next_charge  | Next charge date |
| plan  | plan code |
| appstore_transaction_id  | Appstore original transaction id |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22937,"name":"Timely","from":"Web","max_users":0,"max_projects":0,"num_users":2,"num_projects":0,"plan_id":28,"plan_name":"Essential","next_charge":"2019-02-16","currency":{"id":"usd","name":"United States Dollar","iso_code":"USD","symbol":"$","symbol_first":true},"start_of_week":0,"beta":false,"created_at":1547654080,"payment_mode":"appstore","paid":false,"company_size":"10-49","color":"44505e","logo":{"large_retina":"/assets/account_thumbs/account_large_retina.png","medium_retina":"/assets/account_thumbs/account_medium_retina.png","small_retina":"/assets/account_thumbs/account_small_retina.png"},"capacity":{"hours":40.0,"minutes":0.0,"seconds":0.0,"formatted":"40:00","total_hours":40.0,"total_seconds":144000.0,"total_minutes":2400.0},"plan_code":"essential","appstore_transaction_id":"some-appstore-id","expired":false,"trial":true,"days_to_end_trial":31,"features":[{"name":"control","days":-1},{"name":"memories","days":-1},{"name":"billing","days":-1},{"name":"project_labels","days":-1},{"name":"teams","days":-1},{"name":"recurring_budget","days":-1}],"firebase_url":"https://shining-fire-1562.firebaseio.com/","firebase_auth_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1NTAzMzI0ODAsInYiOjAsImlhdCI6MTU0NzY1NDA4MCwiZCI6eyJ1c2VyX2lkIjoiNTI5OTgiLCJhY2NvdW50X2lkIjoiMjI5MzciLCJ1c2VyX3R5cGUiOiJub3JtYWwiLCJ1aWQiOiJjMjE3NWU1MTA2NTYyODUxNTlmZDUzMjNlYjMzNzBlYyJ9fQ.LmjAsLgFcBwM005CpijZSTpPW3G_bHH0POvbAK-rLn8"}
```



```shell
curl "https://api.timelyapp.com/1.2/private/accounts/22937/upgrade" -d '{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"essential"}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 26f5391e9882e69620b584085fb8279a45f4ba0f56867b7622e5e6ada16d48e0" \
	-H "Cookie: "
```
## upgrade account plan to solo


### Request

#### Endpoint

```plaintext
POST /1.2/private/accounts/22936/upgrade
Accept: application/json
Content-Type: application/json
Authorization: Bearer e81c398ba4d66496decee2bef46512c0f368ec7bfff47422d1b984a90d48fccc
```

`POST /1.2/private/accounts/:account_id/upgrade`

#### Parameters


```json
{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"solo_v1"}}
```


| Name | Description |
|:-----|:------------|
| next_charge  | Next charge date |
| plan  | plan code |
| appstore_transaction_id  | Appstore original transaction id |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
{"id":22936,"name":"Timely","from":"Web","max_users":1,"max_projects":3,"num_users":2,"num_projects":0,"plan_id":34,"plan_name":"Solo","next_charge":"2019-02-16","currency":{"id":"usd","name":"United States Dollar","iso_code":"USD","symbol":"$","symbol_first":true},"start_of_week":0,"beta":false,"created_at":1547654080,"payment_mode":"appstore","paid":false,"company_size":"10-49","color":"44505e","logo":{"large_retina":"/assets/account_thumbs/account_large_retina.png","medium_retina":"/assets/account_thumbs/account_medium_retina.png","small_retina":"/assets/account_thumbs/account_small_retina.png"},"capacity":{"hours":40.0,"minutes":0.0,"seconds":0.0,"formatted":"40:00","total_hours":40.0,"total_seconds":144000.0,"total_minutes":2400.0},"plan_code":"solo_v1","appstore_transaction_id":"some-appstore-id","expired":false,"trial":true,"days_to_end_trial":31,"features":[{"name":"control","days":-1},{"name":"memories","days":-1},{"name":"billing","days":-1},{"name":"project_labels","days":-1},{"name":"teams","days":-1},{"name":"recurring_budget","days":-1}],"firebase_url":"https://shining-fire-1562.firebaseio.com/","firebase_auth_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1NTAzMzI0ODAsInYiOjAsImlhdCI6MTU0NzY1NDA4MCwiZCI6eyJ1c2VyX2lkIjoiNTI5OTYiLCJhY2NvdW50X2lkIjoiMjI5MzYiLCJ1c2VyX3R5cGUiOiJub3JtYWwiLCJ1aWQiOiJmOWMxNTBkODM4NDYxMDFlZmFkOTZjMzQ1OTNmMWUwMSJ9fQ.edVaGzHhAhiEgjqOfp8oW5frGqHZWaQP0QOAl0t-IiM"}
```



```shell
curl "https://api.timelyapp.com/1.2/private/accounts/22936/upgrade" -d '{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"some-appstore-id","plan":"solo_v1"}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer e81c398ba4d66496decee2bef46512c0f368ec7bfff47422d1b984a90d48fccc" \
	-H "Cookie: "
```
## upgrade for duplicate appstore_transaction_id


### Request

#### Endpoint

```plaintext
POST /1.2/private/accounts/22942/upgrade
Accept: application/json
Content-Type: application/json
Authorization: Bearer 86cb40faa4c869781e3d69cfed6dae0ed383c92369c0cf0bb231d926de0bb926
```

`POST /1.2/private/accounts/:account_id/upgrade`

#### Parameters


```json
{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"duplicate-transaction-id","plan":"solo_v1"}}
```


| Name | Description |
|:-----|:------------|
| next_charge  | Next charge date |
| plan  | plan code |
| appstore_transaction_id  | Appstore original transaction id |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
422 Unprocessable Entity
```


```json
{"errors":{"message":"Current Apple ID is used by another Timely account. Please login with original Timely account, or use another Apple ID if you want to subscribe."}}
```



```shell
curl "https://api.timelyapp.com/1.2/private/accounts/22942/upgrade" -d '{"account":{"next_charge":"2019-02-16","appstore_transaction_id":"duplicate-transaction-id","plan":"solo_v1"}}' -X POST \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 86cb40faa4c869781e3d69cfed6dae0ed383c92369c0cf0bb231d926de0bb926" \
	-H "Cookie: "
```
# User Onboarding



## create or update properties


### Request

#### Endpoint

```plaintext
PUT /user_onboarding
Accept: application/json
Content-Type: application/json
```

`PUT /user_onboarding`

#### Parameters


```json
{"user_onboarding":{"user_onboarding_properties":[{"property":"has_seen_calendar_day","value":"yes"},{"property":"has_seen_calendar_week","value":"no"}]}}
```


| Name | Description |
|:-----|:------------|
| user_onboarding *required* | User onboarding |
| user_onboarding[user_onboarding_properties] *required* | Array of multiple property and valyes |
| user_onboarding_properties[property] *required* | Onboarding property name |
| user_onboarding_properties[value] *required* | Onboarding property value |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"user_id":52749,"property":"has_seen_calendar_day","value":"yes","updated_at":"2019-01-16T16:54:08+01:00"},{"user_id":52749,"property":"has_seen_calendar_week","value":"no","updated_at":"2019-01-16T16:54:08+01:00"}]
```



```shell
curl "https://api.timelyapp.com/user_onboarding" -d '{"user_onboarding":{"user_onboarding_properties":[{"property":"has_seen_calendar_day","value":"yes"},{"property":"has_seen_calendar_week","value":"no"}]}}' -X PUT \
	-H "Host: app.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Cookie: "
```
## list properties


### Request

#### Endpoint

```plaintext
GET /user_onboarding
Accept: application/json
Content-Type: application/json
```

`GET /user_onboarding`

#### Parameters


```json
{}: 
```

None known.


### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"user_id":52748,"property":"has_seen_calendar_week","value":"yes","updated_at":"2019-01-16T16:54:08+01:00"}]
```



```shell
curl -g "https://api.timelyapp.com/user_onboarding" -X GET \
	-H "Host: app.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Cookie: "
```
# Users



## Search all users with query


### Request

#### Endpoint

```plaintext
GET /1.1/22934/users/search?q=Charleen+Jerde
Accept: application/json
Content-Type: application/json
Authorization: Bearer 089959af16824d8640ad8873594e01e8f48347c434c66b7419189276fa53e6d8
```

`GET /1.1/:account_id/users/search`

#### Parameters


```json
q: Charleen Jerde
```


| Name | Description |
|:-----|:------------|
| page  | Page number (Default 1) |
| per_page  | Records per page (Default 50) |
| q *required* | Search query (min 2 characters) |



### Response

```plaintext
Content-Type: application/json; charset=utf-8
200 OK
```


```json
[{"id":52980,"email":"jorge@hotmail.com","name":"Charleen Jerde","active":false,"external_id":null,"avatar":{"large":"https://www.gravatar.com/avatar/53307145cda468462255d45a544411d7?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_large_retina.jpg&s=200","medium":"https://www.gravatar.com/avatar/53307145cda468462255d45a544411d7?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_medium_retina.jpg&s=50","small":"https://www.gravatar.com/avatar/53307145cda468462255d45a544411d7?d=https%3A%2F%2Fapp.timelyapp.com%2Fassets%2Fthumbs%2Fuser_small_retina.jpg&s=25"},"updated_at":1547654079}]
```



```shell
curl -g "https://api.timelyapp.com/1.1/22934/users/search?q=Charleen+Jerde" -X GET \
	-H "Host: api.timelyapp.test" \
	-H "Accept: application/json" \
	-H "Content-Type: application/json" \
	-H "Authorization: Bearer 089959af16824d8640ad8873594e01e8f48347c434c66b7419189276fa53e6d8" \
	-H "Cookie: "
```
