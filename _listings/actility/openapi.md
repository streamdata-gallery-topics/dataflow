swagger: "2.0"
x-collection-name: Actility
x-complete: 1
info:
  title: ThingPark DX Maker API
  description: api-providing-features-for-device-makers-such-as-preprovisioning-on-standalone-join-servers-
  version: 1.0.0
host: dx-api.thingpark.com
basePath: /maker/v011/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /bridgeDataflows:
    post:
      summary: Bridge dataflow creation
      description: Creates a new Bridge dataflow.
      operationId: creates-a-new-bridge-dataflow
      x-api-path-slug: bridgedataflows-post
      parameters:
      - in: body
        name: bridgeDataflow
        description: Contents of the Bridge dataflow to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bridge
      - Dataflow
      - Creation
  /bridgeDataflows/{bridgeDataflowRef}:
    get:
      summary: Bridge dataflow retrieval
      description: Retrieves the Bridge dataflow corresponding to the provided order
        ref, if that order is within authorized scopes.
      operationId: retrieves-the-bridge-dataflow-corresponding-to-the-provided-order-ref-if-that-order-is-within-author
      x-api-path-slug: bridgedataflowsbridgedataflowref-get
      parameters:
      - in: path
        name: bridgeDataflowRef
        description: Ref of the Bridge dataflow to retrieve
      responses:
        200:
          description: OK
      tags:
      - Bridge
      - Dataflow
      - Retrieval
    put:
      summary: Bridge dataflow update
      description: Updates the Bridge dataflow corresponding to the provided Bridge
        dataflow ref, if that dataflow is within authorized scopes. Note that when
        updating a dataflow, all existing attributs must be provided next to your
        changes.
      operationId: updates-the-bridge-dataflow-corresponding-to-the-provided-bridge-dataflow-ref-if-that-dataflow-is-wi
      x-api-path-slug: bridgedataflowsbridgedataflowref-put
      parameters:
      - in: body
        name: bridgeDataflow
        description: Contents of the Bridge dataflow to update
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: bridgeDataflowRef
        description: Ref of the Bridge dataflow to update
      responses:
        200:
          description: OK
      tags:
      - Bridge
      - Dataflow
      - Update
    delete:
      summary: Bridge dataflow deletion
      description: Deletes the Bridge dataflow corresponding to the provided Bridge
        dataflow ref, if that dataflow is within authorized scopes.
      operationId: deletes-the-bridge-dataflow-corresponding-to-the-provided-bridge-dataflow-ref-if-that-dataflow-is-wi
      x-api-path-slug: bridgedataflowsbridgedataflowref-delete
      parameters:
      - in: path
        name: bridgeDataflowRef
        description: Ref of the Bridge dataflow to delete
      responses:
        200:
          description: OK
      tags:
      - Bridge
      - Dataflow
      - Deletion
  /events:
    get:
      summary: Dataflow events retrieval
      description: Retrieves the list of events for all configured dataflows in scope.
      operationId: retrieves-the-list-of-events-for-all-configured-dataflows-in-scope
      x-api-path-slug: events-get
      parameters:
      - in: query
        name: dataflowRef
        description: Ref of the dataflow for which events should be retrieved
      responses:
        200:
          description: OK
      tags:
      - Dataflow
      - Events
      - Retrieval