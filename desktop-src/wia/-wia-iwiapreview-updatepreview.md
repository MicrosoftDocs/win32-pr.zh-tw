---
description: 取得 IWiaPreview：： GetNewPreview 方法快取的未篩選影像。
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview：： UpdatePreview 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113301"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="67585-103">IWiaPreview：： UpdatePreview 方法</span><span class="sxs-lookup"><span data-stu-id="67585-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="67585-104">取得 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像。</span><span class="sxs-lookup"><span data-stu-id="67585-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67585-105">語法</span><span class="sxs-lookup"><span data-stu-id="67585-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="67585-106">參數</span><span class="sxs-lookup"><span data-stu-id="67585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67585-107">*lOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67585-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67585-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="67585-108">Type: **LONG**</span></span>

<span data-ttu-id="67585-109">指定應用程式是否需要 WIA 2.0 Preview 元件，將快取影像的子領域或整個快取影像傳遞給影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="67585-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="67585-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span><span class="sxs-lookup"><span data-stu-id="67585-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="67585-111">將整個快取的影像傳遞至影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="67585-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="67585-112">*pChildWiaItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67585-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67585-113">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="67585-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="67585-114">指定 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)專案的指標，這是 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)方法的 *pWiaItem2* 參數所指定之 **IWiaItem2** 專案的子系。</span><span class="sxs-lookup"><span data-stu-id="67585-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="67585-115">或者，如果應用程式需要整個平板的預覽，請指定 **IWiaPreview：： GetNewPreview** 方法的 *pWiaItem2* 參數指標。</span><span class="sxs-lookup"><span data-stu-id="67585-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="67585-116">當 *pChildWiaItem* 是 **IWiaPreview：： GetNewPreview** 之 *pWiaItem2* 參數的子系時，這個子專案通常是由分割篩選所建立。</span><span class="sxs-lookup"><span data-stu-id="67585-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67585-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="67585-117">Return value</span></span>

<span data-ttu-id="67585-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="67585-118">Type: **HRESULT**</span></span>

<span data-ttu-id="67585-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="67585-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67585-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67585-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67585-121">備註</span><span class="sxs-lookup"><span data-stu-id="67585-121">Remarks</span></span>

<span data-ttu-id="67585-122">這個方法會透過影像處理篩選準則傳遞快取的未篩選影像，然後將篩選的資料寫入應用程式提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="67585-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="67585-123">WIA 2.0 Preview 元件會藉由呼叫影像處理篩選器的 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 方法來抓取此資料流程，然後呼叫應用程式回呼的 **GetNextStream** 執行。</span><span class="sxs-lookup"><span data-stu-id="67585-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="67585-124">在呼叫 **IWiaPreview：： UpdatePreview** 之前，應用程式必須先呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ，以從掃描器取得映射;否則，方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="67585-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="67585-125">WIA 2.0 Preview 元件會儲存從驅動程式下載的未篩選映射。</span><span class="sxs-lookup"><span data-stu-id="67585-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="67585-126">將 WIA 2.0 專案傳遞至 **IWiaPreview：： UpdatePreview** ，可能只代表從驅動程式下載影像的小型區域。</span><span class="sxs-lookup"><span data-stu-id="67585-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="67585-127">如果發生這種情況，WIA 2.0 Preview 元件在將此區域傳遞給影像處理篩選器之前，實際上會從快取的影像中將它截斷，然後再將篩選的影像資料傳遞回應用程式。</span><span class="sxs-lookup"><span data-stu-id="67585-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="67585-128">若要讓應用程式將整個快取的影像傳遞至影像處理篩選 (接著將它傳遞給應用程式) ，它必須在呼叫 **IWiaPreview：： UpdatePreview** 時，將 *LOptions* 設定為 **WiaPreviewReturnOriginalImage** 。</span><span class="sxs-lookup"><span data-stu-id="67585-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="67585-129">將 *lOptions* 設定為 **WiaPreviewReturnOriginalImage** 時，應用程式必須確定傳遞至 **IWiaPreview：： UpdatePreview** 的專案的範圍設定 ([**wia \_ ip \_ 範圍**](-wia-wiaitempropscanneritem.md)和 **wia \_ ip \_ YEXTENT**) 符合完整快取的影像。</span><span class="sxs-lookup"><span data-stu-id="67585-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="67585-130">在此情況下，影像處理篩選不需要採取任何不同的動作;它只會根據 *pChildWiaItem* 的屬性來篩選影像 (一般來說，在此案例中， *pChildWiaItem* 是傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)) 的相同專案。</span><span class="sxs-lookup"><span data-stu-id="67585-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="67585-131">系統會忽略不同的子領域，並使用相同的設定篩選整個映射。</span><span class="sxs-lookup"><span data-stu-id="67585-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="67585-132">有幾個原因會導致應用程式這麼做。</span><span class="sxs-lookup"><span data-stu-id="67585-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="67585-133">應用程式可能不支援針對分割篩選所偵測 (到的每個區域，個別變更設定 (例如 [**wia \_ ip \_ 亮度**](-wia-wiaitempropscanneritem.md) 和 **wia \_ ip \_ 對比**) ，也可能甚至不會想要使用分割篩選) 。</span><span class="sxs-lookup"><span data-stu-id="67585-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="67585-134">應用程式更容易以 **WiaPreviewReturnOriginalImage** 呼叫 **IWiaPreview：： UpdatePreview** ，讓它一律會從 WIA 2.0 Preview 元件收到完整的影像。</span><span class="sxs-lookup"><span data-stu-id="67585-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="67585-135">WIA 2.0 Preview 元件不支援預覽影像的影像格式，在這種情況下，它無法執行動作來剪下所需的區域。</span><span class="sxs-lookup"><span data-stu-id="67585-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="67585-136">WIA 2.0 Preview 元件的影像格式支援僅限於有 Windows GDI + 1.1 編碼器和解碼器的格式。</span><span class="sxs-lookup"><span data-stu-id="67585-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="67585-137">這些格式為點陣圖 (BMP)  (包含 BITMAPFILEHEADER) 的點陣圖、圖形交換格式 (GIF) 、JPEG、便攜網狀圖形 (PNG) ，以及標記的影像檔案格式 (TIFF) 。</span><span class="sxs-lookup"><span data-stu-id="67585-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="67585-138">請注意，如果應用程式將 **WiaPreviewReturnOriginalImage** 傳遞至 **IWiaPreview：： UPDATEPREVIEW**，則 WIA 2.0 Preview 元件可以支援任何影像或像素格式。</span><span class="sxs-lookup"><span data-stu-id="67585-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="67585-139">**IWiaPreview：： UpdatePreview** 會設定 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 屬性 (，並在傳回之前將它重設，除非它是在) 之前設定。</span><span class="sxs-lookup"><span data-stu-id="67585-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="67585-140">這可讓驅動程式 (和硬體) 以及映射處理篩選器，知道專案是預覽掃描。</span><span class="sxs-lookup"><span data-stu-id="67585-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="67585-141">應用程式必須確定 *pChildWiaItem* 具有相同的影像格式 ([**wia \_ IPA \_ 格式**](-wia-wiaitempropcommonitem.md)) 和解析度 ([**wia \_ ips \_ XRES**](-wia-wiaitempropscanneritem.md)和 **wia \_ Ip \_ YRES**) 在傳遞至 [**pWiaItem：： IWiaPreview**](-wia-iwiapreview-getnewpreview.md)時的 *GetNewPreview* 。</span><span class="sxs-lookup"><span data-stu-id="67585-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="67585-142">子專案的格式必須對應至 WIA 2.0 Preview 元件的快取影像格式， (WIA 2.0 Preview 元件不會執行任何影像轉換) 。</span><span class="sxs-lookup"><span data-stu-id="67585-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="67585-143">範例</span><span class="sxs-lookup"><span data-stu-id="67585-143">Examples</span></span>

<span data-ttu-id="67585-144">每次使用者變更時都應該呼叫 UpdateRegion，例如，所代表之子專案的亮度或對比 `dwRegionNumber` 。</span><span class="sxs-lookup"><span data-stu-id="67585-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="67585-145">此子專案先前是由分割篩選 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)所建立。</span><span class="sxs-lookup"><span data-stu-id="67585-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="67585-146">寫入 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 的影像會由傳輸回呼介面的 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="67585-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="67585-147">在此範例中，會省略 GetSubRegionItem 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="67585-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="67585-148">呼叫此函式之後，應用程式通常會重繪螢幕上的區域。</span><span class="sxs-lookup"><span data-stu-id="67585-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="67585-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="67585-149">Requirements</span></span>



| <span data-ttu-id="67585-150">需求</span><span class="sxs-lookup"><span data-stu-id="67585-150">Requirement</span></span> | <span data-ttu-id="67585-151">值</span><span class="sxs-lookup"><span data-stu-id="67585-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67585-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67585-152">Minimum supported client</span></span><br/> | <span data-ttu-id="67585-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67585-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67585-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67585-154">Minimum supported server</span></span><br/> | <span data-ttu-id="67585-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67585-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67585-156">標頭</span><span class="sxs-lookup"><span data-stu-id="67585-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="67585-157"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="67585-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="67585-158">Idl</span><span class="sxs-lookup"><span data-stu-id="67585-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67585-159"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="67585-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
