---
title: Windows Media 9.5 SDK 中新增的功能
description: Windows Media 9.5 SDK 中新增的功能
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK，功能
- Windows Media Format SDK，新功能
- Windows Media Format SDK，適用于應用程式特定處理的介面
- 'Windows Media Format SDK、DirectX Video 加速 (DXVA) '
- Windows Media Format SDK，IWMPlayerHook 介面
- IWMPlayerHook
- Windows Media Format SDK、x64 版本的 Windows
- Windows Media 格式 SDK，Windows Media 視訊映射編解碼器
- Windows Media Format SDK、音訊編解碼器
- 適用于網路裝置的 Windows Media Format SDK、DRM 10
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，Advanced Profile 編解碼器
- 'Windows Media Format SDK、索尼/Philips 數位互連格式 (S/PDIF) '
- Windows Media Format SDK，低延遲格式
- Windows Media Format SDK，近似搜尋模式
- Windows Media Format SDK，播放清單燒錄
- Windows Media Format SDK，多重語言支援
- Windows Media Format SDK、Windows Media 裝置管理員 SDK
- Windows Media Format SDK，編解碼器介面
- 編解碼器，Windows Media 視訊映射
- 數位版權管理 (DRM) ，網路裝置安全傳輸通訊協定
- DRM (數位版權管理) ，網路裝置安全傳輸通訊協定
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 編解碼器，Advanced Profile 編解碼器
- 索尼/Philips 數位互連格式 (S/PDIF) 、使用傳送或傳輸
- S/PDIF (索尼/Philips 數位互連格式) 、使用傳送或傳輸
- 近似搜尋模式
- 中繼資料、多重語言支援
- Windows Media 裝置管理員 SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092562"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="4d76e-133">Windows Media 9.5 SDK 中新增的功能</span><span class="sxs-lookup"><span data-stu-id="4d76e-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="4d76e-134">Windows Media Format 9.5 SDK 引進了新功能，可提供增強的內容安全性和彈性。</span><span class="sxs-lookup"><span data-stu-id="4d76e-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="4d76e-135">從9系列版本開始，已對 SDK 進行下列變更。</span><span class="sxs-lookup"><span data-stu-id="4d76e-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="4d76e-136">DirectX 影片加速期間應用程式特定處理的新介面</span><span class="sxs-lookup"><span data-stu-id="4d76e-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="4d76e-137">支援 DirectX Video 加速的播放程式應用程式現在可以執行 [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) 介面，以在 DirectX VA 解碼期間執行應用程式特定的處理。</span><span class="sxs-lookup"><span data-stu-id="4d76e-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="4d76e-138">讀取器會先呼叫 [**IWMPLayerHook：:P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) 回呼方法，再將壓縮的影片範例傳遞至視頻處理器進行解碼。</span><span class="sxs-lookup"><span data-stu-id="4d76e-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="4d76e-139">若要使用 **IWMPlayerHook** 介面和相關聯的 [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) 介面，您必須在 Windows Media Format SDK 中安裝更新編號888656。</span><span class="sxs-lookup"><span data-stu-id="4d76e-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="4d76e-140">您可以從 [Microsoft 網站](https://support.microsoft.com/?id=888656)下載更新。</span><span class="sxs-lookup"><span data-stu-id="4d76e-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="4d76e-141">X64 版本 Windows 的 windows Media Format SDK 版本</span><span class="sxs-lookup"><span data-stu-id="4d76e-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="4d76e-142">有 x64 型版本的 Windows Media Format SDK 可用。</span><span class="sxs-lookup"><span data-stu-id="4d76e-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="4d76e-143">這份檔適用于32位版本和 x64 版本的 SDK。</span><span class="sxs-lookup"><span data-stu-id="4d76e-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="4d76e-144">不過，x64 架構的 Windows Media 格式 SDK 不支援數位版權管理 (DRM) 。</span><span class="sxs-lookup"><span data-stu-id="4d76e-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="4d76e-145">新版本的 Windows Media 視訊映射編解碼器</span><span class="sxs-lookup"><span data-stu-id="4d76e-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="4d76e-146">Windows Media 視訊9映射 v2 編解碼器可簡化移動和縮放的範例幾何計算。</span><span class="sxs-lookup"><span data-stu-id="4d76e-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="4d76e-147">新的編解碼器也支援在影像之間進行數個複雜的轉換。</span><span class="sxs-lookup"><span data-stu-id="4d76e-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="4d76e-148">新版本的 Windows Media 音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="4d76e-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="4d76e-149">Windows Media Format 9.5 SDK 包含下列更新的音訊編解碼器：</span><span class="sxs-lookup"><span data-stu-id="4d76e-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="4d76e-150">Windows Media 音訊9。1</span><span class="sxs-lookup"><span data-stu-id="4d76e-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="4d76e-151">Windows Media 音訊9.1 專業版</span><span class="sxs-lookup"><span data-stu-id="4d76e-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="4d76e-152">Windows Media 音訊9.1 無損</span><span class="sxs-lookup"><span data-stu-id="4d76e-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="4d76e-153">適用于網路裝置的 Windows Media DRM 10 通訊協定支援</span><span class="sxs-lookup"><span data-stu-id="4d76e-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="4d76e-154">Windows Media Format 9.5 SDK 支援網路裝置安全傳輸通訊協定的新 Windows Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="4d76e-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="4d76e-155">此通訊協定可用來透過區域網路將加密的內容串流至播放裝置，例如機頂尖的影片接收者。</span><span class="sxs-lookup"><span data-stu-id="4d76e-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="4d76e-156">大部分用來為網路裝置執行 Windows Media DRM 10 支援的程式必須由應用程式執行。</span><span class="sxs-lookup"><span data-stu-id="4d76e-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="4d76e-157">不過，您可以使用 Windows Media Format SDK 的方法來提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="4d76e-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="4d76e-158">維護裝置的資料庫，包括針對網路裝置啟用 Windows Media DRM 10 的裝置。</span><span class="sxs-lookup"><span data-stu-id="4d76e-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="4d76e-159">驗證裝置，確保它們「接近」足夠的網路上的用戶端以進行安全串流。</span><span class="sxs-lookup"><span data-stu-id="4d76e-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="4d76e-160">將受 DRM 保護的檔案轉換為網路裝置串流的 Windows Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="4d76e-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="4d76e-161">使用先前加密的資料來寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="4d76e-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="4d76e-162">支援新的 DRM 授權</span><span class="sxs-lookup"><span data-stu-id="4d76e-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="4d76e-163">使用 Windows Media Rights Manager SDK 建立的新授權會使用輸出保護層級 (OPLs) 來指定播放和複製內容的許可權和限制。</span><span class="sxs-lookup"><span data-stu-id="4d76e-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="4d76e-164">Windows Media Format SDK 提供從授權讀取 OPLs 的支援。</span><span class="sxs-lookup"><span data-stu-id="4d76e-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="4d76e-165">新的影片編解碼器</span><span class="sxs-lookup"><span data-stu-id="4d76e-165">New Video Codec</span></span>

<span data-ttu-id="4d76e-166">Windows Media 視訊 9 Advanced Profile 編解碼器建基於 Windows Media 視訊9編解碼器的高品質，同時新增對交錯編碼的支援。</span><span class="sxs-lookup"><span data-stu-id="4d76e-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="4d76e-167">S/PDIF 輸出</span><span class="sxs-lookup"><span data-stu-id="4d76e-167">S/PDIF Output</span></span>

<span data-ttu-id="4d76e-168">使用 Windows Media 音訊 Professional 編解碼器編碼的內容，現在可以使用索尼/Philips 數位互連格式 (S/PDIF) 來傳送或傳輸。</span><span class="sxs-lookup"><span data-stu-id="4d76e-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="4d76e-169">Low-Delay 音訊</span><span class="sxs-lookup"><span data-stu-id="4d76e-169">Low-Delay Audio</span></span>

<span data-ttu-id="4d76e-170">Windows Media 音訊9.1 和 Windows Media 音訊 9.1 Professional 編解碼器現在都支援數個低延遲格式。</span><span class="sxs-lookup"><span data-stu-id="4d76e-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="4d76e-171">這些格式會產生可更快速啟動的音訊串流，以減少串流切換案例中的延遲。</span><span class="sxs-lookup"><span data-stu-id="4d76e-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="4d76e-172">使用低延遲格式也可以改善即時廣播的整體延遲。</span><span class="sxs-lookup"><span data-stu-id="4d76e-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="4d76e-173">近似搜尋模式</span><span class="sxs-lookup"><span data-stu-id="4d76e-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="4d76e-174">您現在可以使用讀取器在 ASF 檔案中搜尋大約的時間。</span><span class="sxs-lookup"><span data-stu-id="4d76e-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="4d76e-175">這種模式可改善執行不精確搜尋時的效能，例如當使用者按一下 Windows Media Player 中的搜尋列時。</span><span class="sxs-lookup"><span data-stu-id="4d76e-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="4d76e-176">近似搜尋會傳回先前 cleanpoint 的媒體範例，而不是針對搜尋的精確時間來重建範例。</span><span class="sxs-lookup"><span data-stu-id="4d76e-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="4d76e-177">播放清單燒錄</span><span class="sxs-lookup"><span data-stu-id="4d76e-177">Playlist Burning</span></span>

<span data-ttu-id="4d76e-178">Windows Media DRM 10 支援將音訊檔案複製到 Red Book CD 作為播放清單一部分的許可權。</span><span class="sxs-lookup"><span data-stu-id="4d76e-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="4d76e-179">Windows Media Format SDK 提供方法來確認是否允許複製播放清單中的檔案。</span><span class="sxs-lookup"><span data-stu-id="4d76e-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="4d76e-180">改進了中繼資料的 Multiple-Language 支援</span><span class="sxs-lookup"><span data-stu-id="4d76e-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="4d76e-181">在 Windows Media Format 9 系列 SDK 中，所有新增至檔案的中繼資料都已指派給以預設語言的語言識別項指定的語言清單。</span><span class="sxs-lookup"><span data-stu-id="4d76e-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="4d76e-182">這會導致當不同地區設定中的內容散發者新增一些中繼資料時發生問題，因為散發者的地區設定中的使用者只會看到為其語言新增的幾個屬性。</span><span class="sxs-lookup"><span data-stu-id="4d76e-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="4d76e-183">Windows Media Format 9.5 SDK 會解決此問題，方法是在檔案中有兩種語言的屬性之前，不會建立語言清單。</span><span class="sxs-lookup"><span data-stu-id="4d76e-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="4d76e-184">屆時，所有的中繼資料都會與第二個語言的地區設定相關聯，而這會成為預設值。</span><span class="sxs-lookup"><span data-stu-id="4d76e-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="4d76e-185">如此一來，內容散發者可以保留檔案的所有原始中繼資料（例如標題和作者），而不會在新增與其地區設定相關的某些屬性時保持不變。</span><span class="sxs-lookup"><span data-stu-id="4d76e-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="4d76e-186">安裝中包含 Windows Media 裝置管理員 SDK</span><span class="sxs-lookup"><span data-stu-id="4d76e-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="4d76e-187">Windows Media Format 9.5 SDK 的安裝套件會安裝 Windows Media 裝置管理員 SDK。</span><span class="sxs-lookup"><span data-stu-id="4d76e-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="4d76e-188">您可以在 C： WMSDK WMFSDK95 WMDM 檔資料夾中找到 Windows Media 裝置管理員 SDK 的檔 \\ \\ \\ \\ (如果沒有在預設資料夾中安裝 windows media Format SDK，您的資料夾將會有所不同。 ) </span><span class="sxs-lookup"><span data-stu-id="4d76e-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="4d76e-189">編解碼器介面檔</span><span class="sxs-lookup"><span data-stu-id="4d76e-189">Codec Interface Documentation</span></span>

<span data-ttu-id="4d76e-190">本檔包含在 Windows Media 格式 SDK 之外使用 Windows Media 音訊和影片編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4d76e-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="4d76e-191">這份檔最初是在從 Microsoft 開發人員網路下載時發行的一部分。</span><span class="sxs-lookup"><span data-stu-id="4d76e-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="4d76e-192">示範直接使用編解碼器 DMOs 的範例應用程式包含在 Windows Media 格式 SDK 安裝中，以及標頭。</span><span class="sxs-lookup"><span data-stu-id="4d76e-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d76e-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d76e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d76e-194">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="4d76e-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




