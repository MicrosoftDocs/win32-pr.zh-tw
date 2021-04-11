---
description: 您可以選擇 Microsoft Update 服務中的電腦，然後使用自動更新註冊該服務。
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In 至 Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112156"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="e5fac-103">Opt-In 至 Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="e5fac-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="e5fac-104">您可以選擇 Microsoft Update 服務中的電腦，然後使用自動更新註冊該服務。</span><span class="sxs-lookup"><span data-stu-id="e5fac-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="e5fac-105">本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 向自動更新註冊 Microsoft Update 服務。</span><span class="sxs-lookup"><span data-stu-id="e5fac-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="e5fac-106">或者，若要註冊服務，使用者可以造訪 Microsoft Update。</span><span class="sxs-lookup"><span data-stu-id="e5fac-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="e5fac-107">在您嘗試執行此範例之前，請確認電腦上安裝的 WUA 版本是7.0.6000 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e5fac-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="e5fac-108">如需如何判斷已安裝之 WUA 版本的詳細資訊，請參閱 [判斷 wua 的目前版本](determining-the-current-version-of-wua.md)。</span><span class="sxs-lookup"><span data-stu-id="e5fac-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="e5fac-109">範例</span><span class="sxs-lookup"><span data-stu-id="e5fac-109">Example</span></span>

<span data-ttu-id="e5fac-110">下列腳本範例說明如何使用 Windows Update Agent (WUA) 向自動更新註冊 Microsoft Update 服務。</span><span class="sxs-lookup"><span data-stu-id="e5fac-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="e5fac-111">此範例允許延遲或離線處理（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="e5fac-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5fac-112">此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。</span><span class="sxs-lookup"><span data-stu-id="e5fac-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="e5fac-113">此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。</span><span class="sxs-lookup"><span data-stu-id="e5fac-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="e5fac-114">在舊版 WUA (7.0.6000) 的最小 WUA 版本，您可以使用登錄設定來簡化加入宣告進程。</span><span class="sxs-lookup"><span data-stu-id="e5fac-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="e5fac-115">設定登錄機碼和值之後，下一次 WUA 執行搜尋時，就會發生 Microsoft Update 加入宣告進程。</span><span class="sxs-lookup"><span data-stu-id="e5fac-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="e5fac-116">加入宣告進程可能會由自動更新或由 API 呼叫者觸發。</span><span class="sxs-lookup"><span data-stu-id="e5fac-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="e5fac-117">例如，要為加入程式設定的登錄機碼和值的完整路徑如下所示：</span><span class="sxs-lookup"><span data-stu-id="e5fac-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="e5fac-118">**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**Windowsupdate.log** \\**PendingServiceRegistration** \\**7971f918-a847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="e5fac-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="e5fac-119">**ClientApplicationID** = 我的應用程式</span><span class="sxs-lookup"><span data-stu-id="e5fac-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="e5fac-120">**RegisterWithAU** = 1</span><span class="sxs-lookup"><span data-stu-id="e5fac-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="e5fac-121">只有當 WUA 從7.0.6000 版之前的版本更新為版本7.0.6000 或更新版本時，才會遵守登錄機碼一次。</span><span class="sxs-lookup"><span data-stu-id="e5fac-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="e5fac-122">覆寫現有的登錄值時，我們建議您自行決定，因為覆寫這些值可能會變更先前服務註冊要求的結果。</span><span class="sxs-lookup"><span data-stu-id="e5fac-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="e5fac-123">建立此登錄機碼需要系統管理認證。</span><span class="sxs-lookup"><span data-stu-id="e5fac-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="e5fac-124">若為 Windows Vista，呼叫端必須在提高許可權的進程中建立登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e5fac-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



