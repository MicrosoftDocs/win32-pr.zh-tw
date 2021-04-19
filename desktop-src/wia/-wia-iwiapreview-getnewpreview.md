---
description: 在內部快取從驅動程式傳回之未篩選的映射。
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'IWiaPreview：： GetNewPreview 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971409"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="c6bbe-103">IWiaPreview：： GetNewPreview 方法</span><span class="sxs-lookup"><span data-stu-id="c6bbe-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="c6bbe-104">在內部快取從驅動程式傳回之未篩選的映射。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6bbe-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6bbe-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="c6bbe-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6bbe-107">*pWiaItem2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6bbe-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6bbe-108">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c6bbe-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="c6bbe-109">指定影像的 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)專案的指標。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="c6bbe-110">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6bbe-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6bbe-111">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="c6bbe-111">Type: **LONG**</span></span>

<span data-ttu-id="c6bbe-112">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-112">Currently unused.</span></span> <span data-ttu-id="c6bbe-113">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c6bbe-114">*pWiaTransferCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6bbe-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6bbe-115">類型： \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c6bbe-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="c6bbe-116">指定呼叫應用程式 [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6bbe-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6bbe-117">Return value</span></span>

<span data-ttu-id="c6bbe-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6bbe-118">Type: **HRESULT**</span></span>

<span data-ttu-id="c6bbe-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6bbe-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6bbe-121">備註</span><span class="sxs-lookup"><span data-stu-id="c6bbe-121">Remarks</span></span>

<span data-ttu-id="c6bbe-122">應用程式必須先呼叫 **IWiaPreview：： GetNewPreview** ，然後再呼叫 [**IWiaPreview：:D etectregions**](-wia-iwiapreview-detectregions.md)。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="c6bbe-123">**IWiaPreview：： GetNewPreview** 會設定 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 屬性 (，並在傳回之前將它重設，除非它是在) 之前設定。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="c6bbe-124">這可讓驅動程式和硬體以及影像處理篩選器知道專案是預覽掃描。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="c6bbe-125">在內部，Windows 映像取得 (WIA) 2.0 preview 元件會藉由在 *pWiaItem2* 上呼叫 [**GetExtension**](-wia-iwiaitem2-getextension.md) ，建立驅動程式影像處理篩選的實例。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="c6bbe-126">當應用程式呼叫 **IWiaPreview：： GetNewPreview** 時，WIA 2.0 preview 元件會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="c6bbe-127">WIA 2.0 preview 元件也會初始化 **IWiaPreview：： GetNewPreview** 中的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="c6bbe-128">在呼叫 [**IWiaPreview：： UpdatePreview**](-wia-iwiapreview-updatepreview.md)期間，WIA 2.0 preview 元件會使用相同的篩選實例。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="c6bbe-129">在呼叫 WIA 2.0 preview 元件之前，應用程式應該呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md) ，以確定驅動程式隨附于影像處理篩選器。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="c6bbe-130">它應該在它會傳遞至 **IWiaPreview：： GetNewPreview** 的專案上呼叫 **CheckExtension** 。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="c6bbe-131">提供沒有影像處理篩選器的即時預覽是無用的。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="c6bbe-132">如果應用程式在沒有影像處理篩選的情況下呼叫驅動程式的 **IWiaPreview：： GetNewPreview** ，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="c6bbe-133">範例</span><span class="sxs-lookup"><span data-stu-id="c6bbe-133">Examples</span></span>

<span data-ttu-id="c6bbe-134">CheckImgFilter 會檢查驅動程式是否有影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="c6bbe-135">在呼叫預覽元件之前，應用程式應該確定驅動程式具有影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="c6bbe-136">DownloadPreviewImage 會藉由呼叫 preview 元件的 **IWiaPreview：： GetNewPreview** 方法，從掃描器下載影像資料。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="c6bbe-137">如果應用程式使用者想要叫用分割篩選器，它就會呼叫 DetectSubregions，它會針對它所偵測到的每個區域，在 pWiaItem2 中建立子專案。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="c6bbe-138">如需此範例中所使用的 DetectSubregions 方法，請參閱 [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) 。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="c6bbe-139">在此範例中，應用程式使用者 `m_bUseSegmentationFilter` 可以按一下核取方塊來設定。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="c6bbe-140">如果應用程式支援此程式，則應該先透過呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md)來檢查驅動程式是否有分割篩選。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="c6bbe-141">請參閱 **IWiaPreview：： GetNewPreview** ，以取得顯示如何完成此操作的 CheckImgFilter 方法範例。</span><span class="sxs-lookup"><span data-stu-id="c6bbe-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c6bbe-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6bbe-142">Requirements</span></span>



| <span data-ttu-id="c6bbe-143">需求</span><span class="sxs-lookup"><span data-stu-id="c6bbe-143">Requirement</span></span> | <span data-ttu-id="c6bbe-144">值</span><span class="sxs-lookup"><span data-stu-id="c6bbe-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6bbe-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6bbe-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c6bbe-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6bbe-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c6bbe-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6bbe-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c6bbe-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6bbe-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c6bbe-149">標頭</span><span class="sxs-lookup"><span data-stu-id="c6bbe-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6bbe-150"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="c6bbe-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6bbe-151">Idl</span><span class="sxs-lookup"><span data-stu-id="c6bbe-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6bbe-152"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6bbe-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




