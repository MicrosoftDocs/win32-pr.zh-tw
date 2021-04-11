---
description: 網路提供者是一種 DLL，可讓 Windows 作業系統支援特定的網路通訊協定。
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: 執行網路提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112192"
---
# <a name="implementing-a-network-provider"></a><span data-ttu-id="f8cd8-103">執行網路提供者</span><span class="sxs-lookup"><span data-stu-id="f8cd8-103">Implementing a Network Provider</span></span>

<span data-ttu-id="f8cd8-104">網路提供者是一種 DLL，可讓 Windows 作業系統支援特定的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-104">A network provider is a DLL that enables the Windows operating system to support a specific network protocol.</span></span> <span data-ttu-id="f8cd8-105">它是藉由執行網路提供者 API 來完成。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-105">It does this by implementing the Network Provider API.</span></span> <span data-ttu-id="f8cd8-106">此 API 是 [*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 呼叫以與網路通訊的一組功能。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-106">This API is a set of functions the [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls to communicate with the network.</span></span> <span data-ttu-id="f8cd8-107">網路提供者接著會將這些呼叫轉譯成網路特定 API 呼叫，以執行 MPR 所指定的動作。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-107">The network provider then translates these calls into network-specific API calls to perform the action specified by the MPR.</span></span> <span data-ttu-id="f8cd8-108">如此一來，Windows 作業系統就可以與新的網路通訊協定互動，而不需要瞭解其網路特定的 Api。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-108">In this way, the Windows operating system can interact with new network protocols without having to understand their network-specific APIs.</span></span>

<span data-ttu-id="f8cd8-109">若要建立網路提供者，請撰寫可匯出 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 函式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-109">To create a network provider, write a DLL that exports the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function.</span></span>

<span data-ttu-id="f8cd8-110">支援網路提供者 API 中的其他函式是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-110">Support of the other functions in the Network Provider API is optional.</span></span> <span data-ttu-id="f8cd8-111">如果您的網路提供者不需要函式，則您的 DLL 不需要加以執行，也不需要提供存根的實作為。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-111">If your network provider does not require a function, your DLL does not need to implement it or provide a stub implementation.</span></span> <span data-ttu-id="f8cd8-112">如需詳細資訊，請參閱 [網路提供者](authentication-functions.md)函式中的個別函數主題。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-112">For more information, see the individual function topics in [Network Provider Functions](authentication-functions.md).</span></span>

<span data-ttu-id="f8cd8-113">例外狀況是，如果您支援下列其中一個列舉函數，您也必須支援其他兩個函式： [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)、 [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)和 [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-113">The exception is that if you support one of the following enumeration functions, you must support the other two functions as well: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), and [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).</span></span>

<span data-ttu-id="f8cd8-114">下列指導方針說明如何撰寫可與 MPR 和 Windows 作業系統妥善互動的網路提供者。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-114">The following guidelines describe how to write a network provider that interacts well with the MPR and the Windows operating system.</span></span> <span data-ttu-id="f8cd8-115">可能的話，您的提供者應該遵循下列指導方針來進行速度、驗證和路由。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-115">Whenever possible, your provider should adhere to the following guidelines for speed, validation, and routing.</span></span>

## <a name="speed"></a><span data-ttu-id="f8cd8-116">速度</span><span class="sxs-lookup"><span data-stu-id="f8cd8-116">Speed</span></span>

<span data-ttu-id="f8cd8-117">網路提供者應該能夠快速判斷網路資源是否為自己的資源。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-117">A network provider should quickly determine whether a network resource is its own.</span></span> <span data-ttu-id="f8cd8-118">這是因為 MPR 可能必須迴圈許多提供者來尋找資源的擁有者。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-118">This is because the MPR may have to cycle through many providers to find the owner of a resource.</span></span>

<span data-ttu-id="f8cd8-119">如果網路提供者未擁有資源，它應該會立即傳回 WN 錯誤的網路服務（不 \_ 正確） \_ 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-119">If the network provider does not own the resource, it should immediately return the WN\_BAD\_NETNAME status code.</span></span>

<span data-ttu-id="f8cd8-120">支援 [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) 的提供者也很重要，因為它是在 WinFile 正在繪製目錄樹狀結構時呼叫。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-120">It is also important that providers that support [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) return results for this function quickly because it is called while WinFile is painting the directory tree.</span></span>

## <a name="validation"></a><span data-ttu-id="f8cd8-121">驗證</span><span class="sxs-lookup"><span data-stu-id="f8cd8-121">Validation</span></span>

<span data-ttu-id="f8cd8-122">驗證的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-122">The order of validation is important.</span></span> <span data-ttu-id="f8cd8-123">網路提供者應該先判斷其網路是否已啟動，然後判斷網路和網路提供者是否支援此作業。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-123">A network provider should first determine whether its network is started and then determine whether the network and network provider support the operation.</span></span> <span data-ttu-id="f8cd8-124">如果在這些檢查之後，網路提供者會收到任何網路資源，就應該判斷它是否擁有它們。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-124">If, after these checks, the network provider receives any network resources, it should determine whether it owns them.</span></span> <span data-ttu-id="f8cd8-125">最後，它應該驗證其他參數。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-125">Finally, it should validate other parameters.</span></span>

## <a name="routing"></a><span data-ttu-id="f8cd8-126">路由</span><span class="sxs-lookup"><span data-stu-id="f8cd8-126">Routing</span></span>

<span data-ttu-id="f8cd8-127">如果 MPR 必須迴圈處理網路提供者，它將會嘗試所有提供者，直到其中一個接受呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-127">If the MPR has to cycle through network providers, it will try all providers until one accepts the call.</span></span> <span data-ttu-id="f8cd8-128">換句話說，MPR 一律會繼續嘗試尋找網路提供者。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-128">In other words, the MPR always continues to try to find a network provider.</span></span>

<span data-ttu-id="f8cd8-129">但是，它會記下提供者所報告的第一個重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-129">It does, however, take note of the first significant error reported by a provider.</span></span> <span data-ttu-id="f8cd8-130">錯誤 \_ NETPATH 錯誤、錯誤 \_ \_ 網路名稱無效、錯誤不正確錯誤 \_ \_ \_ \_ \_ \_ 層級，因為它們只是表示提供者不管理資源。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-130">Errors such as ERROR\_BAD\_NETPATH, ERROR\_BAD\_NET\_NAME, ERROR\_INVALID\_PARAMETER, ERROR\_INVALID\_LEVEL are considered insignificant because they simply mean that the provider does not manage the resource.</span></span> <span data-ttu-id="f8cd8-131">但是，如果提供者失敗並出現錯誤的 \_ \_ 密碼無效或其他重大錯誤，MPR 會記錄此錯誤，並繼續進行網路提供者的迴圈。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-131">However, if the provider fails with the error ERROR\_INVALID\_PASSWORD or some other significant error, MPR records this error and continues cycling through the network providers.</span></span> <span data-ttu-id="f8cd8-132">一般來說，當路由傳送時，如果沒有任何提供者接受呼叫，MPR 就會報告在迴圈通過網路提供者時所遇到的第一個重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-132">In general, when routing, if no provider accepts the call, the MPR reports the first significant error it encounters while cycling through the network providers.</span></span>

<span data-ttu-id="f8cd8-133">當您決定要傳回的錯誤訊息時，您的網路提供者應該會將此 MPR 的行為納入考慮。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-133">Your network provider should take this behavior of the MPR into account when deciding what error message to return.</span></span>

## <a name="implementation-note"></a><span data-ttu-id="f8cd8-134">執行附注</span><span class="sxs-lookup"><span data-stu-id="f8cd8-134">Implementation note</span></span>

<span data-ttu-id="f8cd8-135">在執行網路提供者 DLL 時，提供者不能呼叫其他 [Windows 網路功能](../wnet/windows-networking-functions.md)、 [Shell api](../shell/samples-usingthumbnailproviders.md)，或其他以 UNC 路徑為基礎的查詢，這些查詢可能會導致 MPR 子系統的進入。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-135">When implementing Network Provider DLL’s, the provider must not call into other [Windows Networking Functions](../wnet/windows-networking-functions.md), [Shell APIs](../shell/samples-usingthumbnailproviders.md), or other UNC path-based queries that could cause reentry into the MPR subsystem.</span></span> <span data-ttu-id="f8cd8-136">如果您從網路提供者 DLL 進行這類呼叫，則應用程式或其他作業系統元件可能會遇到爭用、效能不佳或 MPR 子系統內的鎖死。</span><span class="sxs-lookup"><span data-stu-id="f8cd8-136">If you make such calls from a Network Provider DLL, the application, or other operating system components may experience contention, poor performance, or deadlocks inside the MPR subsystem.</span></span>

 

 
