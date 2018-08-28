---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Insert Remarketing List
  version: 1.0.0
  description: Inserts a new remarketing list.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /userprofiles/{profileId}/remarketingListShares:
    patch:
      summary: Update Remarketing List Shares
      description: Updates an existing remarketing list share. This method supports
        patch semantics.
      operationId: dfareporting.remarketingListShares.patch
      x-api-path-slug: userprofilesprofileidremarketinglistshares-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      - in: query
        name: remarketingListId
        description: Remarketing list ID
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
    put:
      summary: Update Remarketing List Shares
      description: Updates an existing remarketing list share.
      operationId: dfareporting.remarketingListShares.update
      x-api-path-slug: userprofilesprofileidremarketinglistshares-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
  /userprofiles/{profileId}/remarketingListShares/{remarketingListId}:
    get:
      summary: Get Remarketing List Shares
      description: Gets one remarketing list share by remarketing list ID.
      operationId: dfareporting.remarketingListShares.get
      x-api-path-slug: userprofilesprofileidremarketinglistsharesremarketinglistid-get
      parameters:
      - in: path
        name: profileId
        description: User profile ID associated with this request
      - in: path
        name: remarketingListId
        description: Remarketing list ID
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
  /userprofiles/{profileId}/remarketingLists:
    get:
      summary: Get Remarketing Lists
      description: Retrieves a list of remarketing lists, possibly filtered. This
        method supports paging.
      operationId: dfareporting.remarketingLists.list
      x-api-path-slug: userprofilesprofileidremarketinglists-get
      parameters:
      - in: query
        name: active
        description: Select only active or only inactive remarketing lists
      - in: query
        name: advertiserId
        description: Select only remarketing lists owned by this advertiser
      - in: query
        name: floodlightActivityId
        description: Select only remarketing lists that have this floodlight activity
          ID
      - in: query
        name: maxResults
        description: Maximum number of results to return
      - in: query
        name: name
        description: Allows searching for objects by name or ID
      - in: query
        name: pageToken
        description: Value of the nextPageToken from the previous result page
      - in: path
        name: profileId
        description: User profile ID associated with this request
      - in: query
        name: sortField
        description: Field by which to sort the list
      - in: query
        name: sortOrder
        description: Order of sorted results, default is ASCENDING
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
    patch:
      summary: Update Remarketing List
      description: Updates an existing remarketing list. This method supports patch
        semantics.
      operationId: dfareporting.remarketingLists.patch
      x-api-path-slug: userprofilesprofileidremarketinglists-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: id
        description: Remarketing list ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
    post:
      summary: Insert Remarketing List
      description: Inserts a new remarketing list.
      operationId: dfareporting.remarketingLists.insert
      x-api-path-slug: userprofilesprofileidremarketinglists-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Remarketing List
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---