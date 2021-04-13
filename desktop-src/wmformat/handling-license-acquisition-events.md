---
title: 處理授權取得事件
description: 處理授權取得事件
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK，處理授權取得事件
- Windows Media Format SDK，授權取得事件
- Advanced Systems Format (ASF) ，處理授權取得事件
- ASF (Advanced Systems Format) ，處理授權取得事件
- Advanced Systems Format (ASF) 、授權取得事件
- ASF (Advanced Systems Format) 、授權取得事件
- 數位版權管理 (DRM) ，處理授權取得事件
- DRM (數位版權管理) ，處理授權取得事件
- 數位版權管理 (DRM) 、授權取得事件
- DRM (數位版權管理) 、授權取得事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374470"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="d68f1-113">處理授權取得事件</span><span class="sxs-lookup"><span data-stu-id="d68f1-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="d68f1-114">在其 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法中，已啟用 DRM 的讀取器應用程式會處理下列四個與授權取得程式相關的事件：</span><span class="sxs-lookup"><span data-stu-id="d68f1-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="d68f1-115">**WMT \_ LICENSEURL 簽章 \_ \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d68f1-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="d68f1-116">**WMT \_ 無 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="d68f1-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="d68f1-117">**WMT \_ 沒有任何 \_ 許可權， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="d68f1-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="d68f1-118">**WMT \_ 取得 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="d68f1-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="d68f1-119">**WMT \_ LICENSEURL 簽章 \_ \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d68f1-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="d68f1-120">當 DRM 元件偵測到受 DRM 版本7保護的內容時，它會先在本機系統上尋找有效的授權。</span><span class="sxs-lookup"><span data-stu-id="d68f1-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="d68f1-121">如果不存在，則會在檔案的 DRM 標頭中評估授權取得 URL，並將 *pValue* 設定為其中一個 [**WMT \_ DRMLA \_ 信任**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)值的 **WMT LICENSEURL 簽章 \_ \_ \_ 狀態** 事件，指出 URL 是否受信任、未受信任或已遭修改。</span><span class="sxs-lookup"><span data-stu-id="d68f1-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="d68f1-122">如果 URL 不受信任，則應用程式應該警告使用者。</span><span class="sxs-lookup"><span data-stu-id="d68f1-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="d68f1-123">如果 URL 已遭修改，則應該將檔案視為損毀，而且應用程式不應該在不發出強烈警告的情況下流覽至 URL。</span><span class="sxs-lookup"><span data-stu-id="d68f1-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="d68f1-124">**WMT \_ 無 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="d68f1-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="d68f1-125">**WMT 「 \_ 沒有 \_ 許可權**」事件只會傳送給 DRM 第1版內容，這表示必須以非無訊息方式取得授權。</span><span class="sxs-lookup"><span data-stu-id="d68f1-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="d68f1-126">換句話說，使用者必須流覽至網頁才能取得授權。</span><span class="sxs-lookup"><span data-stu-id="d68f1-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="d68f1-127">頁面的 URL 會從 **OnStatus** 方法中的 *pValue* 參數，以寬字元的 null 終止字串形式取出。</span><span class="sxs-lookup"><span data-stu-id="d68f1-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="d68f1-128">如果有的話，應用程式可讓使用者更輕鬆地流覽至網頁，方法是在不同的進程中開啟 Internet Explorer，或是裝載網頁瀏覽器控制項。</span><span class="sxs-lookup"><span data-stu-id="d68f1-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="d68f1-129">但是，這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="d68f1-129">This is not required, however.</span></span> <span data-ttu-id="d68f1-130">應用程式至少可以在訊息方塊中顯示使用者的 URL，並提示他們將它貼入 Internet Explorer 的 [網址] 列。</span><span class="sxs-lookup"><span data-stu-id="d68f1-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="d68f1-131">>audioplayer 範例會示範如何正確處理 **WMT \_ 無 \_ 許可權** 事件，包括如何格式化 URL 字串，以及如何使用 **CreateProcess** 方法開啟 INTERNET EXPLORER 並流覽至指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="d68f1-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="d68f1-132">因為應用程式無法得知何時取得 DRM 第1版授權，所以使用者必須在取得授權之後再次嘗試開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="d68f1-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="d68f1-133">這個相同的非無訊息授權取得程式也可以用於版本7授權，但在此情況下，應用程式可以先呼叫 [**IWMDRMReader：： MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition)。</span><span class="sxs-lookup"><span data-stu-id="d68f1-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="d68f1-134">這個方法將會重複檢查本機授權存放區，直到找到新檔案的授權為止。</span><span class="sxs-lookup"><span data-stu-id="d68f1-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="d68f1-135">屆時，應用程式將會收到 **WMT \_ 取得 \_ 授權** 事件。</span><span class="sxs-lookup"><span data-stu-id="d68f1-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="d68f1-136">針對所有版本7的授權，建議應用程式提供使用者以無訊息方式或非無訊息方式取得授權的選項。</span><span class="sxs-lookup"><span data-stu-id="d68f1-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="d68f1-137">**WMT \_ 沒有任何 \_ 許可權， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="d68f1-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="d68f1-138">**WMT \_ NO \_ RIGHTS \_ EX** 事件表示內容受到 DRM 版本7的保護，因此授權取得程式可以無訊息方式或以無訊息方式進行。</span><span class="sxs-lookup"><span data-stu-id="d68f1-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="d68f1-139">一般情況下，使用者的無訊息授權取得較方便，但有些人偏好以非無訊息方式取得所有授權。</span><span class="sxs-lookup"><span data-stu-id="d68f1-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="d68f1-140">當授權取得要求使用者提交付款或個人資訊時，應一律以非無訊息模式執行此流程。</span><span class="sxs-lookup"><span data-stu-id="d68f1-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="d68f1-141">非無訊息授權取得的說明位於 **WMT \_ NO \_ RIGHTS** 標題之下。</span><span class="sxs-lookup"><span data-stu-id="d68f1-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="d68f1-142">無訊息取得會繼續進行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d68f1-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="d68f1-143">將 *pValue* 參數轉換為 [**WM \_ GET \_ 授權 \_ 資料**](wm-get-license-data.md) 結構，並儲存結構，以防稍後在非無訊息授權取得時需要它。</span><span class="sxs-lookup"><span data-stu-id="d68f1-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="d68f1-144">呼叫讀取器物件上的 **QueryInterface** 來取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面。</span><span class="sxs-lookup"><span data-stu-id="d68f1-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="d68f1-145">呼叫 [**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) ，並在 *dwFlags* 參數中指定0x1 以表示無訊息語言取得。</span><span class="sxs-lookup"><span data-stu-id="d68f1-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="d68f1-146">這是非同步呼叫，會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d68f1-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="d68f1-147">等候 **WMT \_ 取得 \_ 授權** 事件。</span><span class="sxs-lookup"><span data-stu-id="d68f1-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="d68f1-148">**WMT \_ 取得 \_ 授權**</span><span class="sxs-lookup"><span data-stu-id="d68f1-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="d68f1-149">**WMT \_ 取得 \_ 授權** 事件會在取得 DRM 第7版授權的授權取得程式完成之後傳送。</span><span class="sxs-lookup"><span data-stu-id="d68f1-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="d68f1-150">[**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) 會導致傳送此事件以進行無訊息取得，而 [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) 則會將它傳送給非無訊息的取得。</span><span class="sxs-lookup"><span data-stu-id="d68f1-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="d68f1-151">在您的事件處理常式中，將 *pValue* 轉換為 [**WM \_ GET \_ 授權 \_ 資料**](wm-get-license-data.md) 結構的指標，並檢查 **hr** 成員以判斷是否成功取得授權。</span><span class="sxs-lookup"><span data-stu-id="d68f1-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="d68f1-152">如果 **hr** 等於 NS \_ E \_ DRM \_ 沒有任何 \_ 許可權，則表示授權必須以非無訊息的方式取得。</span><span class="sxs-lookup"><span data-stu-id="d68f1-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="d68f1-153">應用程式應可讓使用者隨時取消授權取得程式。</span><span class="sxs-lookup"><span data-stu-id="d68f1-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="d68f1-154">這是藉由呼叫 [**IWMDRMReader：： CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition)來完成。</span><span class="sxs-lookup"><span data-stu-id="d68f1-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="d68f1-155">呼叫這個方法將會傳送 **WMT \_ 取得 \_ 授權** 事件，其 **HRESULT** 值為 NS \_ S 的 \_ DRM 已 \_ \_ 取消。</span><span class="sxs-lookup"><span data-stu-id="d68f1-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="d68f1-156">如果已取得 **hr** 等於 NS \_ S \_ \_ 的 DRM 授權，則 \_ 會取得授權，而且應用程式可以嘗試播放該檔案，或將它複製到裝置，或執行任何已要求許可權的動作。</span><span class="sxs-lookup"><span data-stu-id="d68f1-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="d68f1-157">在 Windows XP 上引進了新的錯誤碼： NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED。</span><span class="sxs-lookup"><span data-stu-id="d68f1-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="d68f1-158">每當 Windows XP 上的 Windows Media Format 執行時間元件無法在無訊息授權取得期間取得授權時，就會產生此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d68f1-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="d68f1-159">在其他平臺上， \_ \_ \_ \_ \_ 當授權取得失敗時，通常會傳回 NS E DRM 授權存放區錯誤。</span><span class="sxs-lookup"><span data-stu-id="d68f1-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="d68f1-160">新的錯誤碼旨在區別授權取得失敗，以及 \_ 產生 NS E \_ DRM \_ 授權 \_ 存放區 \_ 錯誤的其他失敗情況。</span><span class="sxs-lookup"><span data-stu-id="d68f1-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="d68f1-161">下列程式碼片段會顯示在無訊息授權取得嘗試之後傳回這些錯誤的建議方式：</span><span class="sxs-lookup"><span data-stu-id="d68f1-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="d68f1-162">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="d68f1-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d68f1-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="d68f1-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d68f1-164">**讀取受保護的檔案**</span><span class="sxs-lookup"><span data-stu-id="d68f1-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




