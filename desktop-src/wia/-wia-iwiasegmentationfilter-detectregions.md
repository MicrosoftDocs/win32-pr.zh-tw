---
description: 決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: 'IWiaSegmentationFilter：:D etectRegions 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113300"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="fc7c5-103">IWiaSegmentationFilter：:D etectRegions 方法</span><span class="sxs-lookup"><span data-stu-id="fc7c5-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="fc7c5-104">決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7c5-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc7c5-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="fc7c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc7c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc7c5-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc7c5-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7c5-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-108">Type: **LONG**</span></span>

<span data-ttu-id="fc7c5-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-109">Currently unused.</span></span> <span data-ttu-id="fc7c5-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc7c5-111">*pInputStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc7c5-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7c5-112">類型： \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="fc7c5-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="fc7c5-113">指定 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 預覽影像的指標。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="fc7c5-114">_pWiaItem2 \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc7c5-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7c5-115">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="fc7c5-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="fc7c5-116">指定取得 *pInputStream* 之 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)專案的指標。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="fc7c5-117">分割篩選會建立此專案的子專案。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc7c5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc7c5-118">Return value</span></span>

<span data-ttu-id="fc7c5-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-119">Type: **HRESULT**</span></span>

<span data-ttu-id="fc7c5-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc7c5-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7c5-122">備註</span><span class="sxs-lookup"><span data-stu-id="fc7c5-122">Remarks</span></span>

<span data-ttu-id="fc7c5-123">這個方法會判斷 pInputStream 所代表之影像的子領域。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="fc7c5-124">針對每個子領域偵測到的子領域，它會針對 *pWiaItem2* 參數中指定的 [**IWiaItem2**](-wia-iwiaitem2.md)專案建立子專案。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="fc7c5-125">針對每個子專案，分割篩選必須使用下列 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md)，設定要掃描之區域周框矩形的值。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="fc7c5-126">**WIA \_ IP \_ XPOS**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="fc7c5-127">**WIA \_ IP \_ YPOS**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="fc7c5-128">**WIA \_ IP \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="fc7c5-129">**WIA \_ IP \_ YEXTENT**</span><span class="sxs-lookup"><span data-stu-id="fc7c5-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="fc7c5-130">如果驅動程式支援反扭曲，則更高階的篩選器可能也需要其他 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md) ，例如 **WIA \_ ip \_ 反扭曲 \_ X** 和 **wia \_ ip \_ \_**。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="fc7c5-131">如果應用程式呼叫 **IWiaSegmentationFilter：:D etectregions** 超過一次，應用程式必須先刪除最後一次呼叫 **IWiaSegmentationFilter：:D etectregions** 所建立的子專案。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="fc7c5-132">如果應用程式將任何屬性變更為 *pWiaItem2*，請在將影像取得至 *pInputStream* ，以及其對 **IWiaSegmentationFilter：:D etectregions** 的呼叫之間，原始屬性 (亦即，當取得串流時，專案具有的屬性) 必須還原。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="fc7c5-133">這可以藉由 [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) 和 [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)來完成。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="fc7c5-134">如果應用程式的呼叫將相同的資料流程傳遞給分割篩選一次以上，則必須重設 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="fc7c5-135">應用程式也必須在初始下載之後和呼叫 IWiaSegmentationFilter 之前重設資料流程 **：:D etectregions**。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="fc7c5-136">範例</span><span class="sxs-lookup"><span data-stu-id="fc7c5-136">Examples</span></span>

<span data-ttu-id="fc7c5-137">分割會在資料流程上執列區域偵測， (`pImageStream`) 傳遞至 DetectSubregions。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="fc7c5-138">請參閱此範例中使用的 CreateSegmentationFilter 方法 [**GetExtension**](-wia-iwiaitem2-getextension.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="fc7c5-139">DownloadPreviewImage 會藉由呼叫預覽元件的 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法，從掃描器下載影像資料。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="fc7c5-140">如果應用程式使用者想要叫用分割篩選器，它就會呼叫 DetectSubregions，它會針對它所偵測到的每個區域，在 pWiaItem2 中建立子專案。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="fc7c5-141">如需此範例中使用的 DetectSubregions 方法，請參閱 **IWiaSegmentationFilter：:D etectregions** 。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="fc7c5-142">在此範例中，應用程式使用者 `m_bUseSegmentationFilter` 可以按一下核取方塊來設定。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="fc7c5-143">如果應用程式支援此程式，則應該先透過呼叫 [**CheckExtension**](-wia-iwiaitem2-checkextension.md)來檢查驅動程式是否有分割篩選。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="fc7c5-144">如需說明如何完成此操作的 CheckImgFilter 方法範例，請參閱 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc7c5-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="fc7c5-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc7c5-145">Requirements</span></span>



| <span data-ttu-id="fc7c5-146">需求</span><span class="sxs-lookup"><span data-stu-id="fc7c5-146">Requirement</span></span> | <span data-ttu-id="fc7c5-147">值</span><span class="sxs-lookup"><span data-stu-id="fc7c5-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7c5-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc7c5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7c5-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc7c5-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc7c5-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc7c5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7c5-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc7c5-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc7c5-152">標頭</span><span class="sxs-lookup"><span data-stu-id="fc7c5-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7c5-153"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="fc7c5-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc7c5-154">Idl</span><span class="sxs-lookup"><span data-stu-id="fc7c5-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc7c5-155"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc7c5-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
