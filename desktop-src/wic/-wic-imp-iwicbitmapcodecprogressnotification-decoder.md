---
description: '執行 IWICBitmapCodecProgressNotification (解碼器) '
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: '執行 IWICBitmapCodecProgressNotification (解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977353"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="b3d2f-103">執行 IWICBitmapCodecProgressNotification (解碼器) </span><span class="sxs-lookup"><span data-stu-id="b3d2f-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="b3d2f-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3d2f-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="b3d2f-105">當編解碼器在大型映射上執行 i/o 作業（例如 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) ）時，可能需要數秒鐘或甚至幾分鐘才能完成。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="b3d2f-106">當終端使用者無法中斷長時間執行的作業時，他們可能會認為應用程式已停止運作。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="b3d2f-107">使用者經常會關閉應用程式，或甚至重新開機電腦，以嘗試在應用程式沒有回應時重新取得電腦的控制權。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="b3d2f-108">這個介面可讓應用程式指定一個回呼函式，以供編解碼器在指定的間隔呼叫，以通知呼叫端目前作業的進度。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="b3d2f-109">應用程式可以使用這個回呼函式，在使用者介面中顯示進度的指示，以通知使用者作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="b3d2f-110">如果使用者按一下 [**進度**] 對話方塊中的 [**取消**] 按鈕，應用程式會傳回從回呼函式 **中止的 WINCODEC \_ 錯誤 \_** 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="b3d2f-111">發生這種情況時，編解碼器必須取消指定的作業，並將此 **HRESULT** 傳播回執行作業之方法的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="b3d2f-112">此介面應該在容器層級的解碼器類別上執行。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="b3d2f-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3d2f-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="b3d2f-114">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3d2f-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="b3d2f-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3d2f-115">RegisterProgressNotification</span></span>

<span data-ttu-id="b3d2f-116">應用程式會叫用 [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) ，以註冊編解碼器可在指定間隔呼叫的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="b3d2f-117">第一個參數（ *pfnProgressNotification*）是回呼函式的指標，該函式會定期呼叫編解碼器。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="b3d2f-118">*PvData* 參數會指向某些物件，呼叫端想要在每次叫用回呼函式時，將編解碼器傳回到回呼函式。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="b3d2f-119">此物件可能是所有的物件，而且對編解碼器沒有任何特殊意義。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="b3d2f-120">*DwProgressFlags* 參數會指定編解碼器應該呼叫回呼函式的時機。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="b3d2f-121">您可以使用此參數的兩個列舉來執行或函數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="b3d2f-122">[**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation)列舉會指定在解碼 (**WICProgressOperationCopyPixels**) 、編碼 (**WICProgerssOperationWritePixels**) ，或 (**WICProgressOperationAll**) 時，是否要呼叫回呼函式。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="b3d2f-123">編解碼器應該在整個作業期間定期呼叫回呼函式，但是呼叫端可能會指定特定需求。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="b3d2f-124">[**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification)列舉會指出作業中呼叫回呼函式的位置。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="b3d2f-125">如果呼叫端指定 **WICProgressNotificationBegin**，您必須在作業的開頭呼叫它 (0.0) 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="b3d2f-126">如果呼叫端未指定此項，則為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="b3d2f-127">同樣地，如果呼叫端指定 **WICProgerssNotificationEnd**，您必須在作業完成時呼叫它 (1.0) 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="b3d2f-128">如果呼叫端指定 **WICProgressNotificationAll**，您必須在開頭和結尾呼叫它，以及在整個作業中定期呼叫它。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="b3d2f-129">呼叫端也可以指定 **WICProgerssNotificationFrequent**，這表示他們想要以頻繁的間隔（也許是在每幾個掃描行之後）來呼叫。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="b3d2f-130"> (呼叫端通常只會針對非常大的影像使用此旗標 ) 。否則，您通常應該以大約10% 的間隔來回呼要處理的掃描行總數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="b3d2f-131">一次只能針對特定的解碼器或編碼器實例註冊一個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="b3d2f-132">如果應用程式多次呼叫 [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) ，請將先前註冊的回呼函式取代為新的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="b3d2f-133">若要取消回呼註冊，呼叫端會將 *pfnProgressNotification* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="b3d2f-134">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="b3d2f-134">PFNProgressNotification</span></span>

<span data-ttu-id="b3d2f-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) 是具有下列簽章的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="b3d2f-136">當您叫用回呼函式時，請使用 *pvData* 參數傳回應用程式在註冊回呼函式時所指定的相同 *pvData* 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="b3d2f-137">*UFrameNum* 參數應該指出正在處理之框架的索引。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="b3d2f-138">將 operation 參數設定為在編碼時解碼和 **WICProgressOperationWritePixels** 時的 **WICProgressOperationCopyPixels** 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="b3d2f-139">*DblProgress* 參數應該是在作業開始 (0.0 之間的數位) 和 1.0 (完成作業) 。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="b3d2f-140">此值應該會反映已處理的掃描行相對於要處理的掃描行總數的比例。</span><span class="sxs-lookup"><span data-stu-id="b3d2f-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3d2f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3d2f-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3d2f-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="b3d2f-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b3d2f-143">**ProgressNotificationCallback**</span><span class="sxs-lookup"><span data-stu-id="b3d2f-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="b3d2f-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="b3d2f-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="b3d2f-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="b3d2f-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3d2f-146">執行 IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="b3d2f-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="b3d2f-147">執行 IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="b3d2f-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="b3d2f-148">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="b3d2f-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b3d2f-149">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="b3d2f-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



