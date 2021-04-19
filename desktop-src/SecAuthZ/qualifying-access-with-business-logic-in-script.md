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
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974947"
---
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="96b98-103">使用腳本中的商務邏輯來限定存取權</span><span class="sxs-lookup"><span data-stu-id="96b98-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="96b98-104">使用商務規則腳本來提供用來檢查存取的執行時間邏輯。</span><span class="sxs-lookup"><span data-stu-id="96b98-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="96b98-105">如需商務規則的詳細資訊，請參閱 [商務規則](business-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="96b98-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="96b98-106">若要將商務規則指派給工作，請先設定代表工作之 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件的 [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage)屬性。</span><span class="sxs-lookup"><span data-stu-id="96b98-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="96b98-107">腳本必須使用 Visual Basic Scripting Edition (VBScript) 程式設計語言或 JScript 開發軟體來撰寫。</span><span class="sxs-lookup"><span data-stu-id="96b98-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="96b98-108">指定指令碼語言之後，請使用腳本的字串表示來設定 **IAzTask** 物件的 [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule)屬性。</span><span class="sxs-lookup"><span data-stu-id="96b98-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="96b98-109">當檢查具有相關聯之商務規則的工作所包含之作業的存取權時，應用程式必須建立兩個相同大小的陣列，以作為 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法的 *varParameterNames* 和 *varParameterValues* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="96b98-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="96b98-110">如需建立用戶端內容的詳細資訊，請參閱 [在腳本中建立用戶端內容](establishing-a-client-context-in-script.md)。</span><span class="sxs-lookup"><span data-stu-id="96b98-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="96b98-111">[**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法會建立傳遞給商務規則腳本的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext)物件。</span><span class="sxs-lookup"><span data-stu-id="96b98-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="96b98-112">腳本接著會設定 **azbizrulecoNtext.businessruleresult** 物件的 [**azbizrulecoNtext.businessruleresult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult)屬性。</span><span class="sxs-lookup"><span data-stu-id="96b98-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="96b98-113">值為 **True** 表示授與存取權，值為 **False** 表示拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="96b98-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="96b98-114">商務規則腳本無法指派給委派的 [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope)物件所包含的 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件。</span><span class="sxs-lookup"><span data-stu-id="96b98-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="96b98-115">下列範例顯示如何使用商務規則腳本來檢查用戶端對作業的存取。</span><span class="sxs-lookup"><span data-stu-id="96b98-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="96b98-116">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，而且此存放區包含名為 Expense 的應用程式、名為 Submit Expense 的工作，以及名為 UseFormControl 的作業。</span><span class="sxs-lookup"><span data-stu-id="96b98-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



