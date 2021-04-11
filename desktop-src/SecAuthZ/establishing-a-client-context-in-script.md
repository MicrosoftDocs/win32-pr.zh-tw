---
description: 若要在腳本中建立用戶端內容，應用程式可以使用權杖的控制碼、網域和使用者名稱，或用戶端安全識別碼的字串表示來建立用戶端內容。
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: 在腳本中建立用戶端內容
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851107"
---
# <a name="establishing-a-client-context-in-script"></a>在腳本中建立用戶端內容

在授權管理員中，應用程式會藉由呼叫 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法（代表用戶端內容），來判斷用戶端是否有權存取作業。

應用程式可以使用權杖的控制碼、網域和使用者名稱，或用戶端的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 的字串表示，來建立用戶端內容。

使用 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication)物件的 [**InitializeClientCoNtextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken)、 [**InitializeClientCoNtextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)和 [**InitializeClientCoNtextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid)方法來建立用戶端內容。

下列範例顯示如何從用戶端名稱建立 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) 物件。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，而且此存放區包含名為 Expense 的應用程式。


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

%>
```



 

 
