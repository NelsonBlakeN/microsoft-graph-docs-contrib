---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewThreatAssessmentRequest()
recipientEmail := "tifc@contoso.com"
requestBody.SetRecipientEmail(&recipientEmail)
expectedAssessment := graphmodels.BLOCK_THREATEXPECTEDASSESSMENT
requestBody.SetExpectedAssessment(&expectedAssessment)
category := graphmodels.MALWARE_THREATCATEGORY
requestBody.SetCategory(&category)
contentData := "UmVjZWl2ZWQ6IGZyb20gTVcyUFIwME1CMDMxNC5uYW1wcmQwMC....."
requestBody.SetContentData(&contentData)

threatAssessmentRequests, err := graphClient.InformationProtection().ThreatAssessmentRequests().Post(context.Background(), requestBody, nil)


```