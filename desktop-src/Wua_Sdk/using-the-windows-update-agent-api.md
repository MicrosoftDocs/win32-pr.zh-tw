---
description: 若要使用 Windows Update 代理程式 (WUA) API，請先從適當的 coclass 建立物件，以建立其中一個介面的實例。
ms.assetid: b304971d-584a-4d0f-be5b-26f0ab315ec9
title: 使用 Windows Update 代理程式 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b5d155a2354b68135d0742f765dffb01e7235f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690711"
---
# <a name="using-the-windows-update-agent-api"></a><span data-ttu-id="44e9d-103">使用 Windows Update 代理程式 API</span><span class="sxs-lookup"><span data-stu-id="44e9d-103">Using the Windows Update Agent API</span></span>

<span data-ttu-id="44e9d-104">若要使用 Windows Update 代理程式 (WUA) API，請先從適當的 coclass 建立物件，以建立其中一個介面的實例。</span><span class="sxs-lookup"><span data-stu-id="44e9d-104">To use the Windows Update Agent (WUA) API, first create an instance of one of the interfaces by creating the object from the appropriate coclass.</span></span>

<span data-ttu-id="44e9d-105">下列主題會說明如何使用 WUA API：</span><span class="sxs-lookup"><span data-stu-id="44e9d-105">The following topics describe how you can use the WUA API:</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="44e9d-106">這些腳本的目的是要示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。</span><span class="sxs-lookup"><span data-stu-id="44e9d-106">These scripts are intended to demonstrate the use of the Windows Update Agent APIs, and provide examples of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="44e9d-107">這些腳本並不是用來做為實際執行程式碼，而 Microsoft (也不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。</span><span class="sxs-lookup"><span data-stu-id="44e9d-107">These scripts are not intended as production code, and the scripts themselves are not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 

-   [<span data-ttu-id="44e9d-108">Windows Update 代理程式物件模型</span><span class="sxs-lookup"><span data-stu-id="44e9d-108">Windows Update Agent Object Model</span></span>](windows-update-agent-object-model.md)
-   [<span data-ttu-id="44e9d-109">判斷 WUA 的目前版本</span><span class="sxs-lookup"><span data-stu-id="44e9d-109">Determining the Current Version of WUA</span></span>](determining-the-current-version-of-wua.md)
-   [<span data-ttu-id="44e9d-110">更新 Windows Update 代理程式</span><span class="sxs-lookup"><span data-stu-id="44e9d-110">Updating the Windows Update Agent</span></span>](updating-the-windows-update-agent.md)
-   [<span data-ttu-id="44e9d-111">更新 Windows Update 代理程式標頭檔</span><span class="sxs-lookup"><span data-stu-id="44e9d-111">Updating Windows Update Agent Header Files</span></span>](updating-windows-update-agent-header-files.md)
-   [<span data-ttu-id="44e9d-112">使用 WUA 離線掃描更新</span><span class="sxs-lookup"><span data-stu-id="44e9d-112">Using WUA to Scan for Updates Offline</span></span>](using-wua-to-scan-for-updates-offline.md)
-   [<span data-ttu-id="44e9d-113">WUA API 中安全的方法和屬性</span><span class="sxs-lookup"><span data-stu-id="44e9d-113">Secured Methods and Properties in the WUA API</span></span>](secured-methods-and-properties-in-the-wua-api.md)
-   [<span data-ttu-id="44e9d-114">搜尋、下載及安裝更新</span><span class="sxs-lookup"><span data-stu-id="44e9d-114">Searching, Downloading, and Installing Updates</span></span>](searching--downloading--and-installing-updates.md)
-   [<span data-ttu-id="44e9d-115">搜尋、下載及安裝特定更新</span><span class="sxs-lookup"><span data-stu-id="44e9d-115">Searching, Downloading, and Installing Specific Updates</span></span>](searching--downloading--and-installing-specific-updates.md)
-   [<span data-ttu-id="44e9d-116">從遠端電腦使用 WUA</span><span class="sxs-lookup"><span data-stu-id="44e9d-116">Using WUA From a Remote Computer</span></span>](using-wua-from-a-remote-computer.md)
-   [<span data-ttu-id="44e9d-117">非同步 WUA 作業的指導方針</span><span class="sxs-lookup"><span data-stu-id="44e9d-117">Guidelines for Asynchronous WUA Operations</span></span>](guidelines-for-asynchronous-wua-operations.md)
-   [<span data-ttu-id="44e9d-118">從次要登入使用 WUA (以) 進程的方式執行</span><span class="sxs-lookup"><span data-stu-id="44e9d-118">Using WUA from a Secondary Logon (Run As) Process</span></span>](using-wua-from-a-secondary-logon--run-as--process.md)
-   [<span data-ttu-id="44e9d-119">WUA 成功和錯誤碼</span><span class="sxs-lookup"><span data-stu-id="44e9d-119">WUA Success and Error Codes</span></span>](wua-success-and-error-codes-.md)
-   [<span data-ttu-id="44e9d-120">WUA 網路錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="44e9d-120">WUA Networking Error Codes</span></span>](wua-networking-error-codes-.md)

 

 



