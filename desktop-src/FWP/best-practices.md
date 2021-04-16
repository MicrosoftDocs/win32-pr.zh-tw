---
title: " (Windows 篩選平台) 的最佳作法"
description: 下列清單包含使用 Windows 篩選平台 (WFP) API 來開發應用程式的最佳做法。
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508248"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="f9443-103"> (Windows 篩選平台) 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="f9443-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="f9443-104">下列清單包含使用 Windows 篩選平台 (WFP) API 來開發應用程式的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="f9443-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="f9443-105">使用動態會話。</span><span class="sxs-lookup"><span data-stu-id="f9443-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="f9443-106">許多應用程式會在一開始就新增篩選原則物件，然後在停止時刪除這些物件。</span><span class="sxs-lookup"><span data-stu-id="f9443-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="f9443-107">藉由使用動態會話，您保證即使應用程式當機，也會刪除這些物件。</span><span class="sxs-lookup"><span data-stu-id="f9443-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="f9443-108">此外，只要在停止時關閉引擎控制碼，會比進行個別呼叫來刪除每個物件更有效率。</span><span class="sxs-lookup"><span data-stu-id="f9443-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="f9443-109">請正常處理交易超時，或將會話 **txnWaitTimeoutInMSec** 設為無限以防止超時。</span><span class="sxs-lookup"><span data-stu-id="f9443-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="f9443-110">即使您未使用明確交易，大部分的呼叫仍會在隱含交易下執行，因此可能會超時。</span><span class="sxs-lookup"><span data-stu-id="f9443-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="f9443-111">使用明確交易，將相關的「新增」或「刪除」作業合併為單一交易。</span><span class="sxs-lookup"><span data-stu-id="f9443-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="f9443-112">這會更有效率，並可讓您輕鬆地在錯誤路徑中清除部分結果。</span><span class="sxs-lookup"><span data-stu-id="f9443-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="f9443-113">使用符合 MUI 規範的字串。</span><span class="sxs-lookup"><span data-stu-id="f9443-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="f9443-114">所有可當地語系化的字串都會儲存在 common data 結構中： [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)。</span><span class="sxs-lookup"><span data-stu-id="f9443-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="f9443-115">此結構內的字串可以是 [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)所支援型別的間接字串。</span><span class="sxs-lookup"><span data-stu-id="f9443-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="f9443-116">在任何函式傳回 **FWPM \_ 顯示 \_ DATA0** 結構之前，會使用呼叫端的地區設定，將間接字串解析為指定的字串資源。</span><span class="sxs-lookup"><span data-stu-id="f9443-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="f9443-117">將所有物件與提供者產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f9443-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="f9443-118">當系統上安裝了多個提供者時，診斷工具可以更輕鬆地判斷加入的物件。</span><span class="sxs-lookup"><span data-stu-id="f9443-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="f9443-119">將篩選準則新增至您自己的子層。</span><span class="sxs-lookup"><span data-stu-id="f9443-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="f9443-120">一旦達到子層中的終止篩選器，就不會評估該子層中的任何篩選。</span><span class="sxs-lookup"><span data-stu-id="f9443-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="f9443-121">因此，如果您將篩選新增至與另一個提供者相同的子層，您可能會防止叫用彼此的篩選，而導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="f9443-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="f9443-122">使用應用層強制 (ALE) ，而不是封包導向的篩選。</span><span class="sxs-lookup"><span data-stu-id="f9443-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="f9443-123">封包層的篩選速度很慢。</span><span class="sxs-lookup"><span data-stu-id="f9443-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="f9443-124">在產生 ICMP 錯誤和 RST 事件之前，先進行篩選。</span><span class="sxs-lookup"><span data-stu-id="f9443-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="f9443-125">這樣會更有效率地在產生這些事件之後篩選這些事件。</span><span class="sxs-lookup"><span data-stu-id="f9443-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="f9443-126">在 Stream/資料包資料層執行封包檢查，而不是在傳輸層。</span><span class="sxs-lookup"><span data-stu-id="f9443-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="f9443-127">這適用于開發標注。</span><span class="sxs-lookup"><span data-stu-id="f9443-127">This applies to developing callouts.</span></span> <span data-ttu-id="f9443-128">如需詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 的注標 [驅動程式設計考慮](/windows-hardware/drivers/network/callout-driver-programming-considerations) 。</span><span class="sxs-lookup"><span data-stu-id="f9443-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="f9443-129">使用複雜的篩選器時，請考慮效能的影響。</span><span class="sxs-lookup"><span data-stu-id="f9443-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="f9443-130">從 Windows 7 和 Windows Server 2008 R2 開始，可以使用多個使用相同欄位索引鍵的條件來建立篩選。</span><span class="sxs-lookup"><span data-stu-id="f9443-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="f9443-131">這可讓您以較少的篩選準則建立複雜的原則。</span><span class="sxs-lookup"><span data-stu-id="f9443-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="f9443-132">不過，這類複雜的篩選器可能會產生較慢的效能，讓 WFP 篩選引擎進行分類。</span><span class="sxs-lookup"><span data-stu-id="f9443-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="f9443-133">您應該進行評估，以判斷使用這類篩選是否會造成對您解決方案的整體效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="f9443-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
