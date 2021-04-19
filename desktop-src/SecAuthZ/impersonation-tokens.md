---
description: 說明在存取控制中使用模擬權杖的方式。
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: 模擬權杖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000313"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="b8c11-103">模擬權杖</span><span class="sxs-lookup"><span data-stu-id="b8c11-103">Impersonation Tokens</span></span>

<span data-ttu-id="b8c11-104">模擬執行緒有兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)：</span><span class="sxs-lookup"><span data-stu-id="b8c11-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="b8c11-105">描述伺服器 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="b8c11-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="b8c11-106">若要取得此權杖的控制碼，請呼叫 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 函數。</span><span class="sxs-lookup"><span data-stu-id="b8c11-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="b8c11-107">模擬存取權杖，描述正在模擬之用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="b8c11-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="b8c11-108">若要取得此權杖的控制碼，請呼叫 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函數。</span><span class="sxs-lookup"><span data-stu-id="b8c11-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="b8c11-109">伺服器可以使用下列功能中的模擬 [*權杖*](/windows/desktop/SecGloss/i-gly) ：</span><span class="sxs-lookup"><span data-stu-id="b8c11-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="b8c11-110">在 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)、 [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)和 [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式中，判斷 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 是否允許用戶端有一組存取權限。</span><span class="sxs-lookup"><span data-stu-id="b8c11-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="b8c11-111">在 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數中，啟用或停用用戶端的許可權。</span><span class="sxs-lookup"><span data-stu-id="b8c11-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="b8c11-112">在 [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) 函式中，判斷是否已在用戶端的權杖中啟用一組許可權。</span><span class="sxs-lookup"><span data-stu-id="b8c11-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="b8c11-113">在安全性事件記錄檔中產生專案的函式，例如 [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) 或 [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)。</span><span class="sxs-lookup"><span data-stu-id="b8c11-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="b8c11-114">這些函式會使用模擬權杖來取得記錄專案之用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8c11-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
