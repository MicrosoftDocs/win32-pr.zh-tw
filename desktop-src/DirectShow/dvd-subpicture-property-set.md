---
description: DVD 子圖片屬性控制子圖片顯示的色彩、對比和輸出。
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: 'DVD 子圖片屬性集 (Dvdmedia .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909086"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="44381-103">DVD 子圖片屬性集</span><span class="sxs-lookup"><span data-stu-id="44381-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="44381-104">DVD 子圖片屬性控制子圖片顯示的色彩、對比和輸出。</span><span class="sxs-lookup"><span data-stu-id="44381-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="44381-105">下列資訊提供在呼叫 [**IKsPropertySet**](ikspropertyset.md) 方法時，要用於此屬性集的必要常數和資料類型。</span><span class="sxs-lookup"><span data-stu-id="44381-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="44381-106">它會提供 **GUID** (*GuidPropSet*) 、屬性識別碼 (*dwPropID*) 和屬性資料類型的值， (*pPropData*) 參數。</span><span class="sxs-lookup"><span data-stu-id="44381-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="44381-107">標籤</span><span class="sxs-lookup"><span data-stu-id="44381-107">Label</span></span> | <span data-ttu-id="44381-108">值</span><span class="sxs-lookup"><span data-stu-id="44381-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="44381-109">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="44381-109">Property Set GUID</span></span> | <span data-ttu-id="44381-110">AM \_ KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="44381-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="44381-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="44381-111">Property ID</span></span>                           | <span data-ttu-id="44381-112">描述</span><span class="sxs-lookup"><span data-stu-id="44381-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44381-113">AM \_ 屬性 \_ DVDSUBPIC \_ 複合 \_ ON</span><span class="sxs-lookup"><span data-stu-id="44381-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="44381-114">啟用或停用子圖片顯示的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="44381-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="44381-115">DirectShow 定義此屬性的布林值資料類型 **上的 AM \_ 屬性 \_ 複合 \_** ，以及 \_ \_ \_ 作為此資料類型之指標的 PAM 屬性複合。</span><span class="sxs-lookup"><span data-stu-id="44381-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="44381-116">**TRUE** 表示顯示子圖片， **FALSE** 表示停用它。</span><span class="sxs-lookup"><span data-stu-id="44381-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="44381-117">如需詳細資訊，請參閱 Windows DDK 的 WDM 部分。</span><span class="sxs-lookup"><span data-stu-id="44381-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="44381-118">AM \_ 屬性 \_ DVDSUBPIC \_</span><span class="sxs-lookup"><span data-stu-id="44381-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="44381-119">僅限設定的屬性，指定將變更其色彩或對比度的子圖片或螢幕矩形。</span><span class="sxs-lookup"><span data-stu-id="44381-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="44381-120">資料類型為 [**AM \_ 屬性 \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli)。</span><span class="sxs-lookup"><span data-stu-id="44381-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="44381-121">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="44381-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="44381-122">AM \_ 屬性 \_ DVDSUBPIC \_ 調色板</span><span class="sxs-lookup"><span data-stu-id="44381-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="44381-123">設定子圖片的調色板。</span><span class="sxs-lookup"><span data-stu-id="44381-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="44381-124">資料類型為 [**AM \_ 屬性 \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)。</span><span class="sxs-lookup"><span data-stu-id="44381-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="44381-125">備註</span><span class="sxs-lookup"><span data-stu-id="44381-125">Remarks</span></span>

<span data-ttu-id="44381-126">**AM \_ 屬性 \_ DVDSUBPIC \_** 的 [AM] 屬性是 [僅設定]。</span><span class="sxs-lookup"><span data-stu-id="44381-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="44381-127">它會指定子圖片或螢幕的矩形，其色彩或對比度將會變更。</span><span class="sxs-lookup"><span data-stu-id="44381-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="44381-128">這與 DVD-Video 規格不同，因為 Microsoft DVD 導覽器會剖析所有按鈕和鍵盤資訊，並且在任何指定時間只將一個反白顯示的矩形傳遞到子圖片解碼器。</span><span class="sxs-lookup"><span data-stu-id="44381-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="44381-129">如此一來，反白顯示的資訊會比 DVD 串流中的資料更頻繁地傳送至該解碼器。</span><span class="sxs-lookup"><span data-stu-id="44381-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="44381-130">醒目提示資訊會以非同步方式到達資料流程。</span><span class="sxs-lookup"><span data-stu-id="44381-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="44381-131">此解碼器使用反白顯示開始和結束時間戳記，將醒目提示資訊與相關的子圖片資訊（如果有的話）相互關聯。</span><span class="sxs-lookup"><span data-stu-id="44381-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="44381-132">如果此解碼器未收到所要求之時間戳記的任何子圖片資料流程資訊，則此解碼器會假設醒目提示的資訊是獨立的，而且不會套用至子圖片。</span><span class="sxs-lookup"><span data-stu-id="44381-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="44381-133">在此情況下，解碼器會假設色彩和對比資訊都是相同的色彩。</span><span class="sxs-lookup"><span data-stu-id="44381-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="44381-134">資料不是完全採用 DVD 光碟格式。</span><span class="sxs-lookup"><span data-stu-id="44381-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="44381-135">Microsoft 提供另一個類型 [**AM \_ 屬性 \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) 的結構，此結構會以參數形式傳遞給這個屬性。</span><span class="sxs-lookup"><span data-stu-id="44381-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="44381-136">此結構描述 DVD 醒目提示資訊中目前選取的按鈕。</span><span class="sxs-lookup"><span data-stu-id="44381-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="44381-137">DVD 導覽器會處理所有擊鍵資訊，並在每次按鈕狀態變更時傳送新的醒目提示資訊。</span><span class="sxs-lookup"><span data-stu-id="44381-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="44381-138">這項資訊一次只會描述一個按鈕的模式。</span><span class="sxs-lookup"><span data-stu-id="44381-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="44381-139">它包含螢幕圖元座標的顯示矩形，或子圖片的顯示（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="44381-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="44381-140">此結構也包含色彩和對比資訊，但僅適用于目前選取之按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="44381-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="44381-141">格式是在 DVD 規格中定義。</span><span class="sxs-lookup"><span data-stu-id="44381-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="44381-142">醒目提示資訊包含開始和結束時間戳記。</span><span class="sxs-lookup"><span data-stu-id="44381-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="44381-143">這些與其他時間戳記的單位都相同，但有兩個例外：0xFFFFFFFF 的開始時間戳表示反白顯示內容在收到時有效，而0xFFFFFFFF 的結束時間戳記表示反白顯示內容在下一個反白顯示之前有效。</span><span class="sxs-lookup"><span data-stu-id="44381-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="44381-144">HLISS 欄位如 DVD 規格中所定義。</span><span class="sxs-lookup"><span data-stu-id="44381-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="44381-145">值為零表示所有醒目提示都是不正確，且解碼器應該停用所有的反白顯示。</span><span class="sxs-lookup"><span data-stu-id="44381-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="44381-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="44381-146">Requirements</span></span>



| <span data-ttu-id="44381-147">需求</span><span class="sxs-lookup"><span data-stu-id="44381-147">Requirement</span></span> | <span data-ttu-id="44381-148">值</span><span class="sxs-lookup"><span data-stu-id="44381-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44381-149">標頭</span><span class="sxs-lookup"><span data-stu-id="44381-149">Header</span></span><br/> | <dl> <span data-ttu-id="44381-150"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="44381-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44381-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44381-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44381-152">屬性集</span><span class="sxs-lookup"><span data-stu-id="44381-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




