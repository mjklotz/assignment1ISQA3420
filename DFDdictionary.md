dictionary of DFD terms

Processes

Backend License: Developer tool used to authenticate user access and provide access to the license scanner and the License data store. Has read write access to License data store. Links to the NIST Vunerability database to send and receive the software package and Vunerability data. Also links to the Software package license scanner to send the software package and receive license information. Aggregates Vunerability and license data and writes the software package, Vunerability and license information to the License data store. Also allows the developer to look at all or select software packages, vunerabilities and license data.

Frontend License: Manager authentication and access to information stored in the License data store. Has read only access to the License data store. Used by the Manager to look at all or select software packages, vunerabilities and license data.

Software package license scanner: Opens the software package and searches for license information, returns the software package and the licenses foundxlist. If none are found then returns software package and none found message.

Frontend policy: Manager authentication and access to information stored in the Policy Documents Data Store. Has read write access. Allows Manager to add or modify policy documents to the Policy Documents data store. Also allows Manager to read policy documents stored on the data store. 

Backend policy: Developer authentication and access to information stored in the Policy Documents Data Store. Has read only access. Allows the Develore to read policy documents in the Policy Documents data store.

Databases

License Data Store: Stores Software package, Vunerability, and license data. 

NIST Vunerability DB: External database used by Backend License process to determine any Vunerabilities associated with software packages.

Policy Documents data store: Stores data from policy documents.

Data flows

Software package: Tool the company is interested in using or currently using.

Select package Vunerability and license req: Query License data store request for selected software package information. Used by developer and Manager.

Select package vulnerability and license res: Response from the License data store containing the software package and license information on selected software packages. Used by Developer and Manager.

All package Vunerability and license req: Request for all software packages with Vunerability and license information contained in the data store. Used by the Developer and Manager.

All package Vunerability and license res: Response from the data store containing all software packages with Vunerability and license information. Used by the Developer and Manager.

Software package vunerability search req: Sends the Software package to the NIST Vunerability DB. Used by the Developer.

Software package vunerability search res: Response from the NIST Vunerability DB. Used by the Developer.

Software package license res: Response from the Software package license scanner. Used by the Developer.

Software package, vunerability search results, license scan results: Agregated data containing the Software package, Software package vunerability res and the Software package license res to be written to the License data store. Used by the Developer.

Policy doc req: Query the Policy Documents data store. Used Manager, Developer, Backend policy and Frontend policy.

Policy doc res: Policy Documents data store response to policy doc req. Used by Manager, Developer, Backend policy and Frontend policy. 

Add policy documents: Sends new policy documents to the Frontend policy process to be written to the Policy Documents data store. Used by Manager 

Write policy documents: Writes new and modified Policy Doncuments to the Policy documents data store. Used by Frontend policy process.

Modify policy documents: Sends modified policy documents to the Frontent policy process to be written to the Policy Documents data store. Used by Manager.

Commit confirm: Confirms data has been written to the data store. Used by Policy Documents data store and License data store.


External entities

Developer: Accesses the Backend license process to check software packages for vulnerabilities and licenses and save the data to the License data store. Can also access all or select software package information. Has read write permission.
Also accesses the Backend policy process to read policy documents. Has read only permission.

Manager: Accesses the Frontend license process to look at all or select software package information. Has read only permission.
Also accesses the Frontend policy process to add and/or modify policy documents from the Policy Documents data store. Also able to read policy documents from the Policy Documents data store. Has read write permission.


