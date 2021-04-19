---
description: Null 轉譯器篩選器會捨棄它收到的每個範例，而不顯示或轉譯範例資料。
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: 'Null 轉譯器篩選 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993203"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="0794f-103">Null 轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="0794f-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="0794f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0794f-104">\[Deprecated.</span></span> <span data-ttu-id="0794f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0794f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0794f-106">Null 轉譯器篩選器會捨棄它收到的每個範例，而不顯示或轉譯範例資料。</span><span class="sxs-lookup"><span data-stu-id="0794f-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0794f-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="0794f-107">Filter interfaces</span></span>                        | <span data-ttu-id="0794f-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="0794f-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="0794f-109">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="0794f-109">Input pin media types</span></span>                    | <span data-ttu-id="0794f-110">任何媒體類型</span><span class="sxs-lookup"><span data-stu-id="0794f-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="0794f-111">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="0794f-111">Input pin interfaces</span></span>                     | <span data-ttu-id="0794f-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0794f-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="0794f-113">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="0794f-113">Output pin media types</span></span>                   | <span data-ttu-id="0794f-114">不適用。</span><span class="sxs-lookup"><span data-stu-id="0794f-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="0794f-115">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="0794f-115">Output pin interfaces</span></span>                    | <span data-ttu-id="0794f-116">不適用。</span><span class="sxs-lookup"><span data-stu-id="0794f-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="0794f-117">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="0794f-117">Filter CLSID</span></span>                             | <span data-ttu-id="0794f-118">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="0794f-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="0794f-119">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="0794f-119">Property Page CLSID</span></span>                      | <span data-ttu-id="0794f-120">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="0794f-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="0794f-121">可執行檔</span><span class="sxs-lookup"><span data-stu-id="0794f-121">Executable</span></span>                               | <span data-ttu-id="0794f-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="0794f-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="0794f-123">優點</span><span class="sxs-lookup"><span data-stu-id="0794f-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="0794f-124">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="0794f-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="0794f-125">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="0794f-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0794f-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0794f-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0794f-127">備註</span><span class="sxs-lookup"><span data-stu-id="0794f-127">Remarks</span></span>

<span data-ttu-id="0794f-128">當圖形中的輸出釘選需要下游連接，但您不想從該 pin 轉譯資料時，請使用此篩選器。</span><span class="sxs-lookup"><span data-stu-id="0794f-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="0794f-129">藉由將輸出連接連接到 Null 轉譯器，您就可以完成連接，而不會轉譯資料。</span><span class="sxs-lookup"><span data-stu-id="0794f-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="0794f-130">雖然此篩選不會轉譯任何範例，但它會在捨棄範例之前等候每個樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="0794f-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="0794f-131">因此，圖形會以一般費率執行。</span><span class="sxs-lookup"><span data-stu-id="0794f-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="0794f-132">如果您想要儘快執行圖形，請將參考時鐘設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0794f-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="0794f-133">如需詳細資訊，請參閱 [設定圖形時鐘](setting-the-graph-clock.md)。</span><span class="sxs-lookup"><span data-stu-id="0794f-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0794f-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0794f-134">Requirements</span></span>



| <span data-ttu-id="0794f-135">需求</span><span class="sxs-lookup"><span data-stu-id="0794f-135">Requirement</span></span> | <span data-ttu-id="0794f-136">值</span><span class="sxs-lookup"><span data-stu-id="0794f-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0794f-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0794f-137">Header</span></span><br/> | <dl> <span data-ttu-id="0794f-138"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0794f-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0794f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0794f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0794f-140">DirectShow 編輯服務物件</span><span class="sxs-lookup"><span data-stu-id="0794f-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




