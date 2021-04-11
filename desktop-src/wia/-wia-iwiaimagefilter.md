---
description: IWiaImageFilter 介面是由影像處理篩選器開發人員所執行，並由 Windows 映像取得 (WIA) 2.0 所呼叫的延伸模組介面。
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: 'IWiaImageFilter 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849352"
---
# <a name="iwiaimagefilter-interface"></a><span data-ttu-id="7e7fa-103">IWiaImageFilter 介面</span><span class="sxs-lookup"><span data-stu-id="7e7fa-103">IWiaImageFilter interface</span></span>

<span data-ttu-id="7e7fa-104">**IWiaImageFilter** 介面是由影像處理篩選器開發人員所執行，並由 Windows 映像取得 (WIA) 2.0 所呼叫的延伸模組介面。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-104">The **IWiaImageFilter** interface is an extension interface implemented by image processing filter developers and called by Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="7e7fa-105">成員</span><span class="sxs-lookup"><span data-stu-id="7e7fa-105">Members</span></span>

<span data-ttu-id="7e7fa-106">**IWiaImageFilter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-106">The **IWiaImageFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7e7fa-107">**IWiaImageFilter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7e7fa-107">**IWiaImageFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="7e7fa-108">方法</span><span class="sxs-lookup"><span data-stu-id="7e7fa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7e7fa-109">方法</span><span class="sxs-lookup"><span data-stu-id="7e7fa-109">Methods</span></span>

<span data-ttu-id="7e7fa-110">**IWiaImageFilter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-110">The **IWiaImageFilter** interface has these methods.</span></span>



| <span data-ttu-id="7e7fa-111">方法</span><span class="sxs-lookup"><span data-stu-id="7e7fa-111">Method</span></span>                                                                | <span data-ttu-id="7e7fa-112">描述</span><span class="sxs-lookup"><span data-stu-id="7e7fa-112">Description</span></span>                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e7fa-113">**ApplyProperties**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-113">**ApplyProperties**</span></span>](-wia-iwiaimagefilter-applyproperties.md)       | <span data-ttu-id="7e7fa-114">可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-114">Enables the image processing filter to write properties back to the driver (and device).</span></span><br/>     |
| [<span data-ttu-id="7e7fa-115">**FilterPreviewImage**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-115">**FilterPreviewImage**</span></span>](-wia-iwiaimagefilter-filterpreviewimage.md) | <span data-ttu-id="7e7fa-116">篩選預覽影像。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-116">Filters the preview image.</span></span><br/>                                                                   |
| [<span data-ttu-id="7e7fa-117">**InitializeFilter**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-117">**InitializeFilter**</span></span>](-wia-iwiaimagefilter-initializefilter.md)     | <span data-ttu-id="7e7fa-118">初始化篩選。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-118">Initializes the filter.</span></span> <span data-ttu-id="7e7fa-119">在每個影像下載之前，由 WIA 2.0 呼叫。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-119">Called by WIA 2.0 before each image download.</span></span> <br/>                       |
| [<span data-ttu-id="7e7fa-120">**SetNewCallback**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-120">**SetNewCallback**</span></span>](-wia-iwiaimagefilter-setnewcallback.md)         | <span data-ttu-id="7e7fa-121">針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-121">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e7fa-122">備註</span><span class="sxs-lookup"><span data-stu-id="7e7fa-122">Remarks</span></span>

<span data-ttu-id="7e7fa-123">影像處理篩選器開發人員應該執行這個介面和 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-123">Image processing filter developers should implement this interface and the [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

<span data-ttu-id="7e7fa-124">WIA 2.0 會呼叫篩選方法。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-124">WIA 2.0 calls filter methods.</span></span> <span data-ttu-id="7e7fa-125">永遠不會直接從應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-125">They are never called directly from an application.</span></span>

<span data-ttu-id="7e7fa-126">Microsoft 會提供 WIA 2.0 Preview 元件，它會快取從掃描器取得的原始、未篩選的預覽影像。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-126">Microsoft supplies the WIA 2.0 Preview Component, which caches the original, unfiltered preview image that is acquired from the scanner.</span></span> <span data-ttu-id="7e7fa-127">應用程式會使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來共同建立 WIA 2.0 Preview 元件 (CLSID WiaPreview) 的實例 \_ ，這會使用 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md)載入篩選。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-127">An application uses [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to co-create an instance of the WIA 2.0 Preview Component (CLSID\_WiaPreview), which loads the filter using [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md).</span></span> <span data-ttu-id="7e7fa-128">當應用程式呼叫 IWiaTransfer 時，會自動呼叫篩選準則 [**：:D 下載 o)**](-wia-iwiatransfer-download.md)。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-128">The filter is called automatically when the application calls [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md).</span></span>

<span data-ttu-id="7e7fa-129">掃描影像時，一律會執行影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-129">The image processing filter is always executed when an image is scanned.</span></span> <span data-ttu-id="7e7fa-130">應用程式無法從掃描器取得影像，而不需要先套用圖像篩選。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-130">An application cannot acquire an image from the scanner without having the imaging filter applied first.</span></span>

<span data-ttu-id="7e7fa-131">篩選準則必須至少執行亮度和對比。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-131">A filter must implement brightness and contrast at a minimum.</span></span> <span data-ttu-id="7e7fa-132">可為使用者提供亮度和對比控制項的一般 UI 可顯示精確的使用者預覽。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-132">The common UI, which provides brightness and contrast controls to the user, can display accurate previews to the user.</span></span>

<span data-ttu-id="7e7fa-133">影像處理篩選絕對不應該修改 [**WiaTransferParams**](-wia-wiatransferparams.md)結構的 *lMessage* 成員。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-133">An image processing filter should never modify the *lMessage* member of the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="7e7fa-134">若要讀取所需的屬性，影像處理篩選器應該呼叫 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面上的 [**IWiaPropertyStorage：： GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) ，藉由呼叫 [IWiaImageFilter：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))從專案取得該介面。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-134">To read the required properties the image processing filter should call [**IWiaPropertyStorage::GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) on the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that it gets from the item by calling [IWiaImageFilter::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="7e7fa-135">然後，篩選準則可將此資料流程上的 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 實例具現化，以讀取專案屬性。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-135">The filter can then instantiate an [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) instance on this stream to read the items properties.</span></span> <span data-ttu-id="7e7fa-136">影像處理篩選不應直接呼叫 [IWiaPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) ，因為此方法會呼叫驅動程式 `drvReadItemProperties` ，但 WIA 2.0 服務已在呼叫中鎖定驅動程式， `drvAcquireItemData` 因此此呼叫將會超時且失敗。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-136">The image processing filter should not call [IWiaPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) directly because this method calls into the driver's `drvReadItemProperties`, but the WIA 2.0 service has already locked the driver in the `drvAcquireItemData` call so this call will timeout and fail.</span></span>

<span data-ttu-id="7e7fa-137">篩選感興趣的屬性，例如亮度和對比設定。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-137">The properties that the filter is interested in could for example be the brightness and contrast settings.</span></span> <span data-ttu-id="7e7fa-138">篩選通常也需要從 *pWiaItem2* 讀取影像格式以及預覽屬性（ [**WIA \_ DPS \_ preview**](-wia-wiaitempropscannerdevice.md)）。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-138">The filter typically also needs to read the image format as well as the preview property, [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md), from *pWiaItem2*.</span></span> <span data-ttu-id="7e7fa-139">這些屬性全都用於篩選進程。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-139">These properties are all used in the filtering process.</span></span>

<span data-ttu-id="7e7fa-140">WIA 2.0 元件一律會將未篩選的資料寫入影像處理篩選器中。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-140">The WIA 2.0 components always writes unfiltered data into the image processing filter.</span></span> <span data-ttu-id="7e7fa-141">篩選的資料流程所執行的影像處理演算法可以篩選資料一次以上，而且不需要擔心產生與篩選資料一次相同的結果。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-141">The image processing algorithm implemented by the filter's stream can filter the data more than once and does not have to be concerned with producing the same results as filtering the data once.</span></span>

<span data-ttu-id="7e7fa-142">篩選準則必須注意 [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) 內容，尤其是在硬體中處理某些篩選相關的工作時。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-142">The filter must pay attention to the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property, especially if some filter related tasks are handled in hardware.</span></span> <span data-ttu-id="7e7fa-143">例如，特定的驅動程式可能會根據應用程式將亮度設定為 WIA 2.0 專案的方式，變更掃描器硬體中的燈泡亮度。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-143">For example, a certain driver can change the brightness of the lamp in the scanner hardware depending on how the application has set the brightness into a WIA 2.0 item.</span></span> <span data-ttu-id="7e7fa-144">在最後一次掃描期間 (當應用程式呼叫 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)) 驅動程式通常會修改掃描器的實體燈泡。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-144">During the final scan (when the application calls [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md)) the driver would typically modify the physical lamp of the scanner.</span></span> <span data-ttu-id="7e7fa-145">在此情況下，影像處理篩選可能完全不需要執行任何亮度處理。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-145">In this case the image processing filter may not have to perform any brightness processing at all.</span></span> <span data-ttu-id="7e7fa-146">不過，在預覽掃描期間，驅動程式不應該修改燈泡的亮度，而應該只在影像處理篩選器中處理。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-146">During a preview scan, however, the driver should not modify the brightness of the lamp—instead this should be taken care of solely in the image processing filter.</span></span> <span data-ttu-id="7e7fa-147">WIA 2.0 Preview 元件和影像處理篩選準則必須根據設定在專案中的屬性，傳回精確的影像。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-147">It is important that the WIA 2.0 Preview Component and the image processing filter return accurate images based on the properties set into the item.</span></span>

<span data-ttu-id="7e7fa-148">影像處理篩選準則必須支援驅動程式支援的所有影像格式。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-148">An image processing filter must support all image formats that the driver supports.</span></span>

<span data-ttu-id="7e7fa-149">系統一律會將影像處理篩選器提供給選取區域的影像，並將其設定為我們取得影像的專案。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-149">The image processing filter is always given an image corresponding to the selection area set into the item for which we are acquiring the image.</span></span> <span data-ttu-id="7e7fa-150">不過請注意，如果映射支援 [**WIA \_ ip \_ 旋轉**](-wia-wiaitempropscanneritem.md) 屬性，該影像可能已經由驅動程式旋轉。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-150">Note, however, that the image may have been rotated by the driver in case it supports the [**WIA\_IPS\_ROTATION**](-wia-wiaitempropscanneritem.md) property.</span></span>

<span data-ttu-id="7e7fa-151">當應用程式呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)或 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)時，影像處理篩選是透過 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md)建立，但通常不是由應用程式所建立，而是由 WIA 2.0 元件建立。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-151">The image processing filter is created through [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md), typically not by the application but by WIA 2.0 components when an application calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) or [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md).</span></span>

<span data-ttu-id="7e7fa-152">**IWiaImageFilter** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-152">The **IWiaImageFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="7e7fa-153">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="7e7fa-153">IUnknown Methods</span></span>                                        | <span data-ttu-id="7e7fa-154">Description</span><span class="sxs-lookup"><span data-stu-id="7e7fa-154">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7e7fa-155">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="7e7fa-155">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="7e7fa-156">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-156">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="7e7fa-157">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="7e7fa-157">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="7e7fa-158">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-158">Increments reference count.</span></span>               |
| [<span data-ttu-id="7e7fa-159">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="7e7fa-159">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="7e7fa-160">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="7e7fa-160">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="7e7fa-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e7fa-161">Requirements</span></span>



| <span data-ttu-id="7e7fa-162">需求</span><span class="sxs-lookup"><span data-stu-id="7e7fa-162">Requirement</span></span> | <span data-ttu-id="7e7fa-163">值</span><span class="sxs-lookup"><span data-stu-id="7e7fa-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7fa-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e7fa-164">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7fa-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e7fa-165">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e7fa-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e7fa-166">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7fa-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e7fa-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7e7fa-168">標頭</span><span class="sxs-lookup"><span data-stu-id="7e7fa-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e7fa-169"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="7e7fa-169"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e7fa-170">Idl</span><span class="sxs-lookup"><span data-stu-id="7e7fa-170">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e7fa-171"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e7fa-171"><dt>Wia.idl</dt></span></span> </dl> |



 

 
