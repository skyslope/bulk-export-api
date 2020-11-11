# bulk-export-api-example

## 

1. Make sure node and your preferred package manager are installed on your machine
    - Instruction to install Yarn can be found here [ [Mac](https://classic.yarnpkg.com/en/docs/install#mac-stable), [Windows](https://classic.yarnpkg.com/en/docs/install#windows-stable) ]
    - Instructions to install Node.js and npm can be found [here](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
2. Clone the repo `git clone https://github.com/skyslope/bulk-export-api.git`
3. Replace the values in the .sampleENV file with your data and rename the file to `.env` from `.sampleENV`
4. Install the modules: dotenv, crypto, moment, and node-fetch: `yarn add dotenv crypto moment node-fetch`
5. Run the script: `yarn start`
6. A successful result will look like the following. **By default, the API returns files created with the last seven (7) days**, unless specified in the `Start_Date` in the .env file:
    - ```[
            { 
                objectType: 'sale',
                saleGuid: '5342bb92-4f6d-4df2-bb03-7be81e2336c7',
                listingGuid: null,
                agentGuid: '48433422-c9d7-4f5b-979c-b26a9fad130d',
                createdByGuid: '48433422-c9d7-4f5b-979c-b26a9fad130d',
                mlsNumber: '',
                escrowNumber: '',
                statusId: 59,
                status: 'Incomplete',
                officeId: null,
                officeGuid: null,
                checklistType: 'Other',
                escrowClosingDate: '2020-10-15T00:00:00',
                actualClosingDate: null,
                contractAcceptanceDate: '2020-10-13T00:00:00',
                modifiedOn: '2020-10-13T18:38:42.997',
                source: null,
                otherSource: null,
                dealType: 'Purchase / Tenant',
                listingPrice: 0,
                salePrice: 10,
                isOfficeLead: false,
                coBrokerCompany: null,
                email: 'GSt8112@skyslope.com',
                property: [Object],
                commission: null,
                sellers: [],
                buyers: [],
                titleContact: null,
                escrowContact: null,
                attorneyContact: [],
                lenderContact: null,
                otherSideAgentContact: null,
                homeWarrantyContact: null,
                miscContact: null,
                commercialLease: null,
                commissionBreakdowns: [],
                coAgentGuids: null,
                commissionSplits: [Array],
                stage: [Object],
                commissionReferral: null,
                agent: [Object],
                coAgents: null,
                earnestMoneyDeposit: null,
                customFields: [Object],
                createdOn: '2020-10-13T18:38:42.967' 
            },
            {   objectType: 'listing',
                listingGuid: '4b9624c6-effc-44cc-9f38-6cef37ee0aa3',
                agentGuid: '09c83abe-fcef-4746-a2bf-822917fa59a9',
                createdByGuid: '09c83abe-fcef-4746-a2bf-822917fa59a9',
                coListingAgentGuid: null,
                referringAgentGuid: null,
                mlsNumber: '',
                status: 'Incomplete',
                modifiedOn: '2020-10-13T18:39:21.14',
                officeId: 12421,
                officeGuid: 'd530742d-97e1-47fb-81a4-bb21c2cf1ab8',
                checklistType: 'New',
                type: 'New',
                listingDate: '2020-10-13T00:00:00',
                source: null,
                otherSource: null,
                fileId: '',
                commission: [Object],
                expirationDate: '2020-10-15T00:00:00',
                company: null,
                listingPrice: 10,
                email: 'JSt6021@skyslope.com',
                property: [Object],
                commercialLease: null,
                sellers: [],
                homeWarranty: null,
                miscContact: null,
                stage: [Object],
                coAgentGuids: null,
                agent: [Object],
                coAgents: null,
                customFields: [Object],
                createdOn: '2020-10-13T18:39:21.123' },
                { objectType: 'sale',
                saleGuid: 'e7eb561a-5d5f-402d-944e-4038242378cb',
                listingGuid: null,
                agentGuid: '09c83abe-fcef-4746-a2bf-822917fa59a9',
                createdByGuid: '09c83abe-fcef-4746-a2bf-822917fa59a9',
                mlsNumber: '',
                escrowNumber: '',
                statusId: 59,
                status: 'Incomplete',
                officeId: 12421,
                officeGuid: 'd530742d-97e1-47fb-81a4-bb21c2cf1ab8',
                checklistType: 'Other',
                escrowClosingDate: null,
                actualClosingDate: null,
                contractAcceptanceDate: '0001-01-01T00:00:00',
                modifiedOn: '2020-10-13T18:39:55.757',
                source: null,
                otherSource: null,
                dealType: 'Purchase / Tenant',
                listingPrice: 0,
                salePrice: 0,
                isOfficeLead: false,
                coBrokerCompany: null,
                email: 'WUWPNsstestQStHUXKK@skyslope.com',
                property: [Object],
                commission: null,
                sellers: [],
                buyers: [],
                titleContact: null,
                escrowContact: null,
                attorneyContact: [],
                lenderContact: null,
                otherSideAgentContact: null,
                homeWarrantyContact: null,
                miscContact: null,
                commercialLease: null,
                commissionBreakdowns: [],
                coAgentGuids: null,
                commissionSplits: [Array],
                stage: [Object],
                commissionReferral: null,
                agent: [Object],
                coAgents: null,
                earnestMoneyDeposit: null,
                customFields: [Object],
                createdOn: '2020-10-13T18:39:55.757' 
            } 
       ]```
7. A list of additional parameters to filter Bulk Export results can be found [here](https://api.skyslope.com/api/docs/openid/SkySlopeApi.html#_bulkexport_getmasterdatafeed)
