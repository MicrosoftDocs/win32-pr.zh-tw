---
description: 使用多個區域時，請按下連絡人的畫面位置，然後判斷連絡人叫用的位置，以 testingdetermines) 會受到使用者輸入影響的 (的區。
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: 在 DirectManipulation 中使用多個區
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104558089"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a><span data-ttu-id="66216-103">在 DirectManipulation 中使用多個區</span><span class="sxs-lookup"><span data-stu-id="66216-103">Using multiple viewports in DirectManipulation</span></span>

<span data-ttu-id="66216-104">使用多個區域時， *點擊測試* 會藉由取得連絡人的畫面位置，並判斷連絡人所叫用的位置，來決定哪些 (的) 會受到使用者輸入影響。</span><span class="sxs-lookup"><span data-stu-id="66216-104">When using multiple viewports, *Hit testing* determines which viewport(s) are affected by user input by taking the screen location of a contact and determining which viewport rectangle the contact hits.</span></span>

<span data-ttu-id="66216-105">[直接操作](direct-manipulation-portal.md)的常見案例是將一個區放在另一個（也稱為「*嵌套*」的區）。</span><span class="sxs-lookup"><span data-stu-id="66216-105">A common scenario in [Direct Manipulation](direct-manipulation-portal.md) is to place one viewport inside another, also known as *nesting viewports*.</span></span> <span data-ttu-id="66216-106">如果連絡人叫用一個以上的區，則由視窗的 [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))呼叫的 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)順序，會決定嵌套的方程式之父子式關聯性。</span><span class="sxs-lookup"><span data-stu-id="66216-106">If the contact hits more than one viewport, the order of  [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) calls by the window's [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) determines the parent-child relationship of the nested viewports.</span></span>

<span data-ttu-id="66216-107">規則：子項目應該在呼叫父系之前呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)。</span><span class="sxs-lookup"><span data-stu-id="66216-107">Rule: The child element should call [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)before calling the parent.</span></span>

![顯示點擊測試階層的圖表](images/dm-art-8.png)

<span data-ttu-id="66216-109">連絡人會在一個區中關閉。</span><span class="sxs-lookup"><span data-stu-id="66216-109">A contact comes down in a viewport.</span></span> <span data-ttu-id="66216-110">[**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 應該先在橙色 (子) 區上呼叫，然後再以綠色 (父) 區來建立正確的階層。</span><span class="sxs-lookup"><span data-stu-id="66216-110">[**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) should first be called on the orange (child) viewport and then the green (parent) viewport to establish the correct hierarchy.</span></span>

## <a name="targeting-the-correct-viewport"></a><span data-ttu-id="66216-111">以正確的視口為目標</span><span class="sxs-lookup"><span data-stu-id="66216-111">Targeting the correct viewport</span></span>

<span data-ttu-id="66216-112">連絡人可以與任意數目的區數相關聯，而且每個連絡人都可以指派給不同的一組區。</span><span class="sxs-lookup"><span data-stu-id="66216-112">A contact can be associated with any number of viewports and each contact can be assigned to a different set of viewports.</span></span>

<span data-ttu-id="66216-113">您可以視需要設定每個區，以支援特定的互動。</span><span class="sxs-lookup"><span data-stu-id="66216-113">Each viewport can be configured to support specific interactions, as required.</span></span>

<span data-ttu-id="66216-114">根據這些設定， [直接操作](direct-manipulation-portal.md) 會識別哪些區可處理輸入。</span><span class="sxs-lookup"><span data-stu-id="66216-114">Based on these settings, [Direct Manipulation](direct-manipulation-portal.md) identifies which viewport handles the input.</span></span> <span data-ttu-id="66216-115">點擊測試階層中的子系大部分的視口都有處理輸入的第一次機會。</span><span class="sxs-lookup"><span data-stu-id="66216-115">The child-most viewport in the hit testing hierarchy has the first chance to handle the input.</span></span> <span data-ttu-id="66216-116">不過，連結和父代升級都可以變更哪些區來處理輸入。</span><span class="sxs-lookup"><span data-stu-id="66216-116">However, both chaining and parent promotion can change which viewport handles the input.</span></span>

## <a name="chaining"></a><span data-ttu-id="66216-117">鏈結</span><span class="sxs-lookup"><span data-stu-id="66216-117">Chaining</span></span>

<span data-ttu-id="66216-118">在操作期間到達內容的結尾時， [直接操作](direct-manipulation-portal.md) 會套用界限效果，以表示內容無法再繼續。</span><span class="sxs-lookup"><span data-stu-id="66216-118">When the end of the content is reached during a manipulation, [Direct Manipulation](direct-manipulation-portal.md) applies a boundary effect to indicate that the content can go no further.</span></span> <span data-ttu-id="66216-119">但是，如果子區 *連結* 至父個區，則會隱藏此效果。</span><span class="sxs-lookup"><span data-stu-id="66216-119">However, if a child viewport is *chained* to a parent viewport, this effect is suppressed.</span></span> <span data-ttu-id="66216-120">相反地，點擊測試階層中最接近支援操作的上階區，會處理輸入。</span><span class="sxs-lookup"><span data-stu-id="66216-120">Instead, the closest ancestor viewport in the hit testing hierarchy that supports the manipulation, handles the input.</span></span> <span data-ttu-id="66216-121">如果操作方向反轉，使上階回到觸發連結的時間點，則操作 "unchains" 並將控制權轉移回子區。</span><span class="sxs-lookup"><span data-stu-id="66216-121">If the direction of the manipulation is reversed such that the ancestor returns to the point where chaining was triggered, the manipulation "unchains" and control transfers back to the child viewport.</span></span>

![顯示連鎖操作的圖表](images/dm-art-9.png)

<span data-ttu-id="66216-123">當使用者將子系視窗全部移動至內容的邊緣時，會將「鏈」操作系至父區，而使用者會開始改為移動父內容。</span><span class="sxs-lookup"><span data-stu-id="66216-123">When the user pans the child viewport all the way to the edge of the content, the manipulation "chains" to the parent viewport, and the user begins panning the parent content instead.</span></span>

> [!Note]  
> <span data-ttu-id="66216-124">X 和 Y 軸彼此獨立，因此如果對角平移觸及 y 界限之前的 x 界限，則操作會在 x 方向移動父系，同時繼續以 y 方向移動子系。</span><span class="sxs-lookup"><span data-stu-id="66216-124">The X and Y axes chain independently of one another, so if a diagonal pan hits the x boundary before the y boundary, the manipulation moves the parent in the x direction while continuing to move the child in the y direction.</span></span> <span data-ttu-id="66216-125">若要啟用或停用連結，請在子區上呼叫 [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) API。</span><span class="sxs-lookup"><span data-stu-id="66216-125">To enable or disable chaining, call the [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) API on the child viewport.</span></span>

### <a name="rails"></a><span data-ttu-id="66216-126">Rails</span><span class="sxs-lookup"><span data-stu-id="66216-126">Rails</span></span>

<span data-ttu-id="66216-127">在設定區的設定中指定滑軌，會影響從區連結輸入的方式。</span><span class="sxs-lookup"><span data-stu-id="66216-127">Specifying rails in a viewport’s configuration affects the way input is chained from the viewport.</span></span> <span data-ttu-id="66216-128">具體而言，輸入無法在滑軌的 "unrailed" 移動瀏覽模式中，從 railed 子區連結到其父系。</span><span class="sxs-lookup"><span data-stu-id="66216-128">Specifically, input cannot chain from a railed child viewport to its parent in the “unrailed” panning mode of rails.</span></span> <span data-ttu-id="66216-129">若要在設定滑軌時鏈出輸入，使用者必須以垂直或水準方式移動流覽並鎖定滑軌。</span><span class="sxs-lookup"><span data-stu-id="66216-129">To chain input when rails are set, the user must have panned vertically or horizontally and be locked to the rails.</span></span>

### <a name="zooming"></a><span data-ttu-id="66216-130">顯示比例</span><span class="sxs-lookup"><span data-stu-id="66216-130">Zooming</span></span>

<span data-ttu-id="66216-131">如果子區是在父代內進行嵌套，而且兩者都設定為縮放，則縮放操作可從子系連結到父系。</span><span class="sxs-lookup"><span data-stu-id="66216-131">If a child viewport is nested inside a parent, and both are configured for zoom, a zoom manipulation can chain from child to parent.</span></span> <span data-ttu-id="66216-132">但是，如果操作繼續進行，它只會在父系上運作，而且無法將其「unchain」至子系。</span><span class="sxs-lookup"><span data-stu-id="66216-132">However, if the manipulation continues, it works only on the parent and cannot “unchain” to the child.</span></span> <span data-ttu-id="66216-133">如果使用者將縮放從子系連結到父系，則 [直接操作](direct-manipulation-portal.md) 會暫停子系，直到與操作相關聯的所有連絡人都從螢幕中移除為止。</span><span class="sxs-lookup"><span data-stu-id="66216-133">If the user chains a zoom from child to parent, [Direct Manipulation](direct-manipulation-portal.md) suspends the child until all contacts associated with the manipulation are removed from the screen.</span></span> <span data-ttu-id="66216-134">此時，子系會從暫止中釋出，而使用者可以移動子系的子功能區。</span><span class="sxs-lookup"><span data-stu-id="66216-134">At this point, the child is released from suspension and the user can pan the child viewport.</span></span>

## <a name="gesture-targeting-parent-promotion"></a><span data-ttu-id="66216-135">手勢目標：上層升級</span><span class="sxs-lookup"><span data-stu-id="66216-135">Gesture targeting: Parent promotion</span></span>

<span data-ttu-id="66216-136">*手勢目標* 是 [直接操作](direct-manipulation-portal.md) 將連絡人群組在一起的程式，並決定哪些區會處理輸入。</span><span class="sxs-lookup"><span data-stu-id="66216-136">*Gesture targeting* is the process by which [Direct Manipulation](direct-manipulation-portal.md) groups contacts together and determines which viewport processes the input.</span></span> <span data-ttu-id="66216-137">「*父代升級*」是指將輸入從子系傳送到父系的情況。</span><span class="sxs-lookup"><span data-stu-id="66216-137">*Parent promotion* refers to cases where the input is transferred from the child to the parent.</span></span> <span data-ttu-id="66216-138">例如，當使用者在設定為僅供滾動的子區中，將兩個連絡人和 pinches 放在一起時，會將輸入升級為父代，以便進行縮放。</span><span class="sxs-lookup"><span data-stu-id="66216-138">For example, when a user puts down two contacts and pinches within a child viewport configured only for scrolling, the input is promoted to the parent so that zooming occurs.</span></span> <span data-ttu-id="66216-139">無論子系的子系是否啟用了連結，都會發生父代升級。</span><span class="sxs-lookup"><span data-stu-id="66216-139">Parent promotion occurs regardless of whether chaining is enabled on the child viewport.</span></span>

<span data-ttu-id="66216-140">與連結不同的是，不會反轉父項升級。</span><span class="sxs-lookup"><span data-stu-id="66216-140">Unlike chaining, parent promotion is not reversed.</span></span> <span data-ttu-id="66216-141">父元件會繼續處理互動輸入，直到所有的連絡人都 (子視窗區停止處理輸入) 為止。</span><span class="sxs-lookup"><span data-stu-id="66216-141">The parent viewport continues to process the interaction input until all contacts are lifted (child viewports stop processing the input).</span></span>
