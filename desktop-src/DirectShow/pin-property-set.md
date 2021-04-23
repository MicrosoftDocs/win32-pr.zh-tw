---
description: 釘選屬性集
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: 釘選屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909616"
---
# <a name="pin-property-set"></a><span data-ttu-id="1e528-103">釘選屬性集</span><span class="sxs-lookup"><span data-stu-id="1e528-103">Pin Property Set</span></span>

<span data-ttu-id="1e528-104">[釘選] 屬性集會傳回篩選上的釘選釘選類別。</span><span class="sxs-lookup"><span data-stu-id="1e528-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="1e528-105">類別會在建立 pin 時由篩選準則設定;此類別會指出 pin 由這個 pin 傳遞或接收的資料類型。</span><span class="sxs-lookup"><span data-stu-id="1e528-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="1e528-106">標籤</span><span class="sxs-lookup"><span data-stu-id="1e528-106">Label</span></span> | <span data-ttu-id="1e528-107">值</span><span class="sxs-lookup"><span data-stu-id="1e528-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="1e528-108">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="1e528-108">Property Set GUID</span></span> | <span data-ttu-id="1e528-109">**AMPROPSETID \_ 釘選**</span><span class="sxs-lookup"><span data-stu-id="1e528-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="1e528-110">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="1e528-110">Property ID</span></span>                   | <span data-ttu-id="1e528-111">描述</span><span class="sxs-lookup"><span data-stu-id="1e528-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="1e528-112">**AMPROPERTY \_ 釘選 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="1e528-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="1e528-113">指定釘選的類別。</span><span class="sxs-lookup"><span data-stu-id="1e528-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="1e528-114">DirectShow 會在 Uuid. h 標頭檔中定義下列釘選類別。</span><span class="sxs-lookup"><span data-stu-id="1e528-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="1e528-115">類別 GUID</span><span class="sxs-lookup"><span data-stu-id="1e528-115">Category GUID</span></span>                     | <span data-ttu-id="1e528-116">Description</span><span class="sxs-lookup"><span data-stu-id="1e528-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e528-117">**釘選 \_ 類別 \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="1e528-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="1e528-118">接受類比並 digitizes 的捕獲篩選器的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1e528-119">**釘選 \_ 類別 \_ 捕獲**</span><span class="sxs-lookup"><span data-stu-id="1e528-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="1e528-120">捕捉 pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1e528-121">**釘選 \_ 類別 \_ CC**</span><span class="sxs-lookup"><span data-stu-id="1e528-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="1e528-122">從第21行提供隱藏式輔助字幕資料的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1e528-123">**釘選 \_ 類別 \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="1e528-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="1e528-124">Pin 提供擴充的資料服務 (行21，甚至是欄位) 。</span><span class="sxs-lookup"><span data-stu-id="1e528-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1e528-125">**釘選 \_ 類別 \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="1e528-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="1e528-126">提供北美洲 Videotext 標準資料的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1e528-127">**釘選 \_ 類別 \_ 預覽**</span><span class="sxs-lookup"><span data-stu-id="1e528-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="1e528-128">預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1e528-129">**PIN \_ 類別 \_ 仍為**</span><span class="sxs-lookup"><span data-stu-id="1e528-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="1e528-130">提供靜止影像的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-130">Pin that provides a still image.</span></span> <span data-ttu-id="1e528-131">必須先連接篩選器的捕獲 pin，才能連接到靜止映射 pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="1e528-132">**釘選 \_ 類別 \_ TELETEXT**</span><span class="sxs-lookup"><span data-stu-id="1e528-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="1e528-133">提供 teletext (隱藏式字幕變異) 的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1e528-134">**釘選 \_ 類別時間 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="1e528-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="1e528-135">提供時間碼資料的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1e528-136">**釘選 \_ 類別 \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="1e528-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="1e528-137">提供垂直空白間隔資料的 Pin。</span><span class="sxs-lookup"><span data-stu-id="1e528-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1e528-138">**釘選 \_ 類別 \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="1e528-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="1e528-139">要連接到重迭 [混音](overlay-mixer-filter.md)器上輸入 pin 零的影片輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="1e528-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="1e528-140">**釘選 \_ 類別 \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="1e528-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="1e528-141">釘選到連接到 [VBI 介面](vbi-surface-allocator.md)配置器，這是在使用影片埠的情況下，為隱藏式字幕重迭等事物配置正確視訊記憶體所需的 VBI surface 配置器篩選器。</span><span class="sxs-lookup"><span data-stu-id="1e528-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="1e528-142">PCI、IEEE 1394 和 USB 案例都不會使用此篩選器。</span><span class="sxs-lookup"><span data-stu-id="1e528-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="1e528-143">**PINNAME \_ 影片 \_ 副本 \_ CAPTURE**</span><span class="sxs-lookup"><span data-stu-id="1e528-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="1e528-144">硬體切割已關閉-字幕釘選</span><span class="sxs-lookup"><span data-stu-id="1e528-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="1e528-145">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="1e528-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="1e528-146">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="1e528-146">Example Code</span></span>

<span data-ttu-id="1e528-147">下列程式碼示範如何檢查 pin 是否支援此屬性集，如果是，如何取得釘選類別：</span><span class="sxs-lookup"><span data-stu-id="1e528-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="1e528-148">此範例會使用 [SafeRelease](../medfound/saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="1e528-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e528-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e528-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e528-150">捕獲篩選準則的 Pin 需求</span><span class="sxs-lookup"><span data-stu-id="1e528-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="1e528-151">屬性集</span><span class="sxs-lookup"><span data-stu-id="1e528-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="1e528-152">使用 Pin 類別</span><span class="sxs-lookup"><span data-stu-id="1e528-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
