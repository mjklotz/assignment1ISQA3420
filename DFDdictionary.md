dictionary of DFD terms

Backend Client: Developer tool used to authenticate user access and provide access to the license scanner and the License data store. Has                 read write access to License data store.

Frontend Client: "Storefront" for user authentication and access to information stored in the License data store. Has read only access to                   License data store.

license scanner: Opens the software package and searches for license information, returns the software package and the licenses found                     list. If none are found then returns software package and none found message.

License Data Store: Holds data for Software packages and returned license information from the license scanner.

Software package: Tool the company is interested in using or currently using.

package and license info: Return from license scanner process containing the software package and license information.

written to data store confirm: Verifies that the software package and license info was saved in the data store.

package license info req: User request for software package and license info from the License data store.

package license info res: License data store response to package license info req containing the software package and license info or a                            message containing not found.
