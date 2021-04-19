---
description: 呼叫 IAzClientCoNtext：： AccessCheck 方法，以檢查用戶端是否可以存取一或多個作業。
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: 在腳本中驗證用戶端對要求的資源的存取
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980363"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="05c1f-103">在腳本中驗證用戶端對要求的資源的存取</span><span class="sxs-lookup"><span data-stu-id="05c1f-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="05c1f-104">呼叫 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck)方法，以檢查用戶端是否可以存取一或多個作業。</span><span class="sxs-lookup"><span data-stu-id="05c1f-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="05c1f-105">如需建立 **IAzClientCoNtext** 物件的詳細資訊，請參閱 [在腳本中建立用戶端內容](establishing-a-client-context-in-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05c1f-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="05c1f-106">用戶端可能會有多個角色的成員資格，而且可能會將一項作業指派給一個以上的工作，讓授權管理員檢查所有角色和工作。</span><span class="sxs-lookup"><span data-stu-id="05c1f-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="05c1f-107">如果用戶端所隸屬的任何角色包含任何包含作業的工作，就會授與該作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="05c1f-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="05c1f-108">若只要檢查用戶端所屬單一角色的存取權，請設定 [**IAzClientCoNtext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)物件的 [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck)屬性。</span><span class="sxs-lookup"><span data-stu-id="05c1f-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="05c1f-109">將授權原則存放區初始化以進行存取檢查時，您必須將零傳遞為 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore)物件之 [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize)方法的 *lFlags* 參數值。</span><span class="sxs-lookup"><span data-stu-id="05c1f-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="05c1f-110">您也可以在執行時間套用商務邏輯，以限定存取權。</span><span class="sxs-lookup"><span data-stu-id="05c1f-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="05c1f-111">如需使用商務邏輯來限定存取權的相關資訊，請參閱 [在腳本中使用商務邏輯限定存取權](qualifying-access-with-business-logic-in-script.md)。</span><span class="sxs-lookup"><span data-stu-id="05c1f-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="05c1f-112">下列範例顯示如何檢查用戶端對作業的存取。</span><span class="sxs-lookup"><span data-stu-id="05c1f-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="05c1f-113">此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區，而且此存放區包含名為 Expense 的應用程式和名為 UseFormControl 的作業。</span><span class="sxs-lookup"><span data-stu-id="05c1f-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


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

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



