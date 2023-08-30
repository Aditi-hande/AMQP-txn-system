## Proof of Concept: AMQP based Financial transaction service
1. Encryption and decryption of payload.
    - En-/De-cryption implemented according to Sarvatra standard algorithm
    - Module is complete and integrated after successful testing
2. Generation of payload.
    - Minimal wrapper over a HashMap for generating JSON payload procedurally.
    - Default values handled
    - TLV (Tag-Length-Value) format generation
    - Module is functional and has been integrated for creating payloads in the HTTP communication module
3. HTTP communication with the Sarvatra test server.
    - Using volley API
    - Login request is sent for beginning the session
    - Response from Login is parsed for session key and other session details
    - Transaction request for transactions along with the saved session key from Login is sent and the response is used to show success status of the txn
    - Module is functional and its implemented for cash withdrawal (Can be extended for other transactions)
4. RD Service API (fingerprint scanner)
    - Mantra RD service API is called for safely reading fingerprint data
    - Module was tested independently and has been integrated for using the returned encrypted data for HTTP requests
5. Creating a UI for Agent Login and transactions
    - Basic UI has been created for Login, Transaction and Success
    - The binding from UI inputs to final HTTP requests has been commented to avoid sending invalid data to Sarvatra test server during development

