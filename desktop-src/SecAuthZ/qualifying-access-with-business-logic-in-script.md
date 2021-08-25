---
description: 在腳本中使用商務規則腳本，以提供用來檢查存取的執行時間邏輯。
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: 使用腳本中的商務邏輯來限定存取權
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b77ff1d6d520780d30efab5619c3e9bc3c896ad88315fba56e3a19e05d3ae97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907548"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>使用腳本中的商務邏輯來限定存取權

使用商務規則腳本來提供用來檢查存取的執行時間邏輯。 如需商務規則的詳細資訊，請參閱 [商務規則](business-rules.md)。

若要將商務規則指派給工作，請先設定代表工作之 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件的 [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage)屬性。 腳本必須使用 Visual Basic 腳本撰寫版 (VBScript) 程式設計語言或 JScript 開發軟體來撰寫。 指定指令碼語言之後，請使用腳本的字串表示來設定 **IAzTask** 物件的 [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule)屬性。

當檢查具有相關聯之商務規則的工作所包含之作業的存取權時，應用程式必須建立兩個相同大小的陣列，以作為 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法的 *varParameterNames* 和 *varParameterValues* 參數傳遞。 如需建立用戶端內容的詳細資訊，請參閱 [在腳本中建立用戶端內容](establishing-a-client-context-in-script.md)。

[**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法會建立傳遞給商務規則腳本的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext)物件。 腳本接著會設定 **azbizrulecoNtext.businessruleresult** 物件的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult)屬性。 值為 **True** 表示授與存取權，值為 **False** 表示拒絕存取。

商務規則腳本無法指派給委派的 [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope)物件所包含的 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件。

下列範例顯示如何使用商務規則腳本來檢查用戶端對作業的存取。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，而且此存放區包含名為 Expense 的應用程式、名為 Submit Expense 的工作，以及名為 UseFormControl 的作業。


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

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



