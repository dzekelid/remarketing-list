---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Update Remarketing List Shares
  version: 1.0.0
  description: Updates an existing remarketing list share.
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