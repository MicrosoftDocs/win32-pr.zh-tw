---
title: 將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10
description: 將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK，轉換受 DRM 保護的檔案
- Windows Media Format SDK，受 DRM 保護的檔案
- Advanced Systems Format (ASF) ，轉換受 DRM 保護的檔案
- ASF (Advanced Systems 格式) ，轉換受 DRM 保護的檔案
- Advanced Systems Format (ASF) 、受 DRM 保護的檔案
- ASF (Advanced Systems Format) 、受 DRM 保護的檔案
- 數位版權管理 (DRM) ，轉換受 DRM 保護的檔案
- DRM (數位版權管理) ，轉換受 DRM 保護的檔案
- 數位版權管理 (DRM) 、受 DRM 保護的檔案
- DRM (數位版權管理) 、受 DRM 保護的檔案
- Windows Media Format SDK，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Windows Media Format SDK、DRM 10
- Advanced Systems Format (ASF) 、適用于網路裝置的 Windows Media DRM 10
- ASF (Advanced Systems Format) ，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Advanced Systems Format (ASF) ，DRM 10
- ASF (Advanced Systems Format) ，DRM 10 用於網路裝置
- 數位版權管理 (DRM) ，適用于網路裝置的 Windows Media DRM 10
- DRM (數位版權管理) 、適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的數位版權管理 (DRM) ，DRM 10
- DRM (數位版權管理) ，DRM 10 用於網路裝置
- 適用于網路裝置的 Windows Media DRM 10，轉換受 DRM 保護的檔案
- 適用于網路裝置的 DRM 10，轉換受 DRM 保護的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681434"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a><span data-ttu-id="bf921-125">將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10</span><span class="sxs-lookup"><span data-stu-id="bf921-125">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>

<span data-ttu-id="bf921-126">註冊並驗證裝置之後，您就可以開始處理授權要求訊息。</span><span class="sxs-lookup"><span data-stu-id="bf921-126">After a device is registered and validated, you can begin processing license request messages from it.</span></span> <span data-ttu-id="bf921-127">當需要應用程式的動作時，裝置會傳送授權要求訊息。</span><span class="sxs-lookup"><span data-stu-id="bf921-127">License request messages are sent by devices when action from the application is needed.</span></span> <span data-ttu-id="bf921-128">目前唯一支援的動作是「播放」，這是保護資料以進行播放的要求。</span><span class="sxs-lookup"><span data-stu-id="bf921-128">The only action currently supported is "Play", which is a request for secure data for playback.</span></span>

<span data-ttu-id="bf921-129">當您收到授權要求訊息時，您應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="bf921-129">When you receive a license request message, you should perform the following steps:</span></span>

1.  <span data-ttu-id="bf921-130">藉由呼叫 [**IWMDRMMessageParser：:P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) 方法來剖析授權要求訊息。</span><span class="sxs-lookup"><span data-stu-id="bf921-130">Parse the license request message by calling the [**IWMDRMMessageParser::ParseLicenseRequestMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) method.</span></span>
2.  <span data-ttu-id="bf921-131">藉由呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid)方法，並傳入步驟1中取得的憑證和序號，來取得裝置的 [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)介面。</span><span class="sxs-lookup"><span data-stu-id="bf921-131">Get the [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) interface for the device by calling the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and serial number obtained in step 1.</span></span>
3.  <span data-ttu-id="bf921-132">確認裝置已準備好接收安全資料：</span><span class="sxs-lookup"><span data-stu-id="bf921-132">Verify that the device is ready to receive secure data:</span></span>
    -   <span data-ttu-id="bf921-133">呼叫 [**IWMRegisteredDevice：： IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) 確認裝置是否已通過核准。</span><span class="sxs-lookup"><span data-stu-id="bf921-133">Call [**IWMRegisteredDevice::IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) to verify that the device has been approved.</span></span> <span data-ttu-id="bf921-134">核准應一律以使用者喜好設定為基礎。</span><span class="sxs-lookup"><span data-stu-id="bf921-134">Approval should always be based on user preference.</span></span>
    -   <span data-ttu-id="bf921-135">呼叫 [**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) 來確認裝置已在過去48小時內經過驗證。</span><span class="sxs-lookup"><span data-stu-id="bf921-135">Call [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) to verify that the device has been validated within the last 48 hours.</span></span> <span data-ttu-id="bf921-136">如果裝置無效，您需要執行鄰近性偵測。</span><span class="sxs-lookup"><span data-stu-id="bf921-136">If the device is not valid, you need to perform proximity detection.</span></span> <span data-ttu-id="bf921-137">如需詳細資訊，請參閱 [執行鄰近性偵測](performing-proximity-detection.md)。</span><span class="sxs-lookup"><span data-stu-id="bf921-137">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>
    -   <span data-ttu-id="bf921-138">呼叫 [**IWMRegisteredDevice：： IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) 來確認裝置已開啟。</span><span class="sxs-lookup"><span data-stu-id="bf921-138">Call [**IWMRegisteredDevice::IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) to verify that the device has been opened.</span></span> <span data-ttu-id="bf921-139">如果裝置未開啟，您可以藉由呼叫 [**IWMRegisteredDevice：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)來開啟它。</span><span class="sxs-lookup"><span data-stu-id="bf921-139">If the device is not open, you can open it by calling [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span> <span data-ttu-id="bf921-140">您一次只能在電腦上開啟10部裝置。</span><span class="sxs-lookup"><span data-stu-id="bf921-140">You can only have 10 devices open on the computer at a time.</span></span> <span data-ttu-id="bf921-141">您可能需要關閉其他裝置，才能開啟您要處理要求的裝置。</span><span class="sxs-lookup"><span data-stu-id="bf921-141">It is possible that you may need to close another device before you can open the one for which you are processing the request.</span></span> <span data-ttu-id="bf921-142">若要關閉裝置，請呼叫 [**IWMRegisteredDevice：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) 方法。</span><span class="sxs-lookup"><span data-stu-id="bf921-142">To close a device, call the [**IWMRegisteredDevice::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) method.</span></span>
4.  <span data-ttu-id="bf921-143">藉由呼叫 [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) 函數來建立 DRM transcryptor 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="bf921-143">Create an instance of the DRM transcryptor object by calling the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function.</span></span>
5.  <span data-ttu-id="bf921-144">呼叫 [**IWMDRMTranscryptor：： initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) 方法以初始化 transcryptor。</span><span class="sxs-lookup"><span data-stu-id="bf921-144">Call the [**IWMDRMTranscryptor::Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) method to initialize the transcryptor.</span></span> <span data-ttu-id="bf921-145">這個方法會採用 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的指標，它會用來傳遞狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="bf921-145">This method takes a pointer to your implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface, which it uses to deliver status messages.</span></span> <span data-ttu-id="bf921-146">此方法也會傳回必須傳送給裝置的授權要求訊息，然後再繼續。</span><span class="sxs-lookup"><span data-stu-id="bf921-146">This method also returns a license request message that must be sent to the device before continuing.</span></span>
6.  <span data-ttu-id="bf921-147">當您的應用程式 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法收到 WMT \_ TRANSCRYPTOR \_ INIT 狀態訊息時，請呼叫 [**IWMDRMTranscryptor：： seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) 方法來搜尋檔案中的適當開始位置。</span><span class="sxs-lookup"><span data-stu-id="bf921-147">When your application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method receives the WMT\_TRANSCRYPTOR\_INIT status message, call the [**IWMDRMTranscryptor::Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) method to seek to the appropriate start position in the file.</span></span> <span data-ttu-id="bf921-148">若要從檔案的開頭開始，您必須使用時間0呼叫 **Seek** 。</span><span class="sxs-lookup"><span data-stu-id="bf921-148">To start at the beginning of the file, you must call **Seek** with time 0.</span></span>
7.  <span data-ttu-id="bf921-149">\_ \_ 當 transcryptor 已準備好在新的呈現時間從檔案傳遞資料時，會傳送 WMT transcryptor SEEKED 訊息。</span><span class="sxs-lookup"><span data-stu-id="bf921-149">The transcryptor sends a WMT\_TRANSCRYPTOR\_SEEKED message when it is ready to deliver data from the file at the new presentation time.</span></span> <span data-ttu-id="bf921-150">對 [**IWMDRMTranscryptor：： Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) 方法進行重複呼叫，以取得轉換的媒體資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bf921-150">Make repeated calls to the [**IWMDRMTranscryptor::Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) method to get converted chunks of media data.</span></span> <span data-ttu-id="bf921-151">每個呼叫都是非同步，而且在接收到 WMT \_ TRANSCRYPTOR READ 訊息之前都不會完成 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bf921-151">Each call is asynchronous and is not complete until a WMT\_TRANSCRYPTOR\_READ message is received.</span></span> <span data-ttu-id="bf921-152">當您收到訊息時，可以將資料傳送至接收裝置。</span><span class="sxs-lookup"><span data-stu-id="bf921-152">When you receive the message, you can send the data to the receiving device.</span></span>
8.  <span data-ttu-id="bf921-153">當您收到 WMT \_ TRANSCRYPTOR \_ READ 訊息，並將 *hr* 參數設定為 NS \_ S \_ TRANSCRYPTOR EOF 時，就會 \_ 讀取整個檔案。</span><span class="sxs-lookup"><span data-stu-id="bf921-153">When you receive a WMT\_TRANSCRYPTOR\_READ message with the *hr* parameter set to NS\_S\_TRANSCRYPTOR\_EOF, the entire file has been read.</span></span> <span data-ttu-id="bf921-154">此時，請呼叫 [**IWMDRMTranscryptor：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) 方法來關閉檔案和釋放資源。</span><span class="sxs-lookup"><span data-stu-id="bf921-154">At this point, call the [**IWMDRMTranscryptor::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) method to close the file and free resources.</span></span>
9.  <span data-ttu-id="bf921-155">當收到 WMT \_ TRANSCRYPTOR \_ 已關閉的訊息時，您可以釋放 [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) 介面。</span><span class="sxs-lookup"><span data-stu-id="bf921-155">When the WMT\_TRANSCRYPTOR\_CLOSED message is received, you can release the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span>

> [!Note]  
> <span data-ttu-id="bf921-156">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="bf921-156">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bf921-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf921-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf921-158">**使用 Windows Media DRM 10 進行網路裝置通訊協定**</span><span class="sxs-lookup"><span data-stu-id="bf921-158">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




