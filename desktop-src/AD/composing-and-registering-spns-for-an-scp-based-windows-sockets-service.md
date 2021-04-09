---
title: 針對 SCP 型 Windows 通訊端服務撰寫和註冊 Spn
description: 下列程式碼範例示範如何撰寫和註冊服務的 Spn。 請在呼叫 CreateService 並建立服務的服務連接點 (SCP) 之後，從您的服務安裝程式呼叫此程式碼。
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- 服務主體名稱 AD、撰寫及註冊以 SCP 為基礎之 Windows sockets 服務的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681687"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="2a577-105">針對 SCP 型 Windows 通訊端服務撰寫和註冊 Spn</span><span class="sxs-lookup"><span data-stu-id="2a577-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="2a577-106">下列程式碼範例示範如何撰寫和註冊服務的 Spn。</span><span class="sxs-lookup"><span data-stu-id="2a577-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="2a577-107">請在呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 並建立服務的服務連接點 (SCP) 之後，從您的服務安裝程式呼叫此程式碼。</span><span class="sxs-lookup"><span data-stu-id="2a577-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="2a577-108">下列程式碼範例會呼叫撰寫和註冊 SPN 的 **SpnCompose** 和 **SpnRegister** 範例函式。</span><span class="sxs-lookup"><span data-stu-id="2a577-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="2a577-109">如需詳細資訊和 **SpnCompose** 原始程式碼，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。</span><span class="sxs-lookup"><span data-stu-id="2a577-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="2a577-110">如需詳細資訊和 **SpnRegister** 原始碼，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="2a577-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="2a577-111">此範例會使用服務類別名稱及其 SCP 的分辨名稱來建立其服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="2a577-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="2a577-112">如需詳細資訊和示範用戶端如何系結至服務 SCP 以取得這些名稱字串的程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="2a577-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="2a577-113">請注意，用來撰寫 SPN 的程式碼會根據服務的類型和用來發行服務的機制而有所不同。</span><span class="sxs-lookup"><span data-stu-id="2a577-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="2a577-114">服務會將其 SPN 儲存在目錄的服務帳戶物件的 **servicePrincipalName** 屬性中，以註冊其 SPN。</span><span class="sxs-lookup"><span data-stu-id="2a577-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="2a577-115">如果服務是在 LocalSystem 帳戶下執行，而不是在服務帳戶下執行，則會在目錄中的本機電腦帳戶物件下註冊其 SPN。</span><span class="sxs-lookup"><span data-stu-id="2a577-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



<span data-ttu-id="2a577-116">卸載您的服務時，您可以使用類似的程式碼取消註冊 Spn。</span><span class="sxs-lookup"><span data-stu-id="2a577-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="2a577-117">指定 **ds \_ spn \_ 刪除 \_ spn \_** 操作操作，而不是 **ds \_ spn \_ 新增 \_ spn \_** 作業。</span><span class="sxs-lookup"><span data-stu-id="2a577-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 