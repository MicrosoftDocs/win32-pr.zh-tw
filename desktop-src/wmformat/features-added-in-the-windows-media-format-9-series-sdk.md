---
title: Windows Media Format 9 系列 SDK 中新增的功能
description: Windows Media Format 9 系列 SDK 中新增的功能
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK，功能
- Windows Media Format SDK，新功能
- Windows Media Format SDK，同步讀取器
- Windows Media 格式 SDK，以框架為基礎的索引
- Windows Media Format SDK、SMPTE 時間碼
- Windows Media Format SDK，DirectShow 篩選器
- Windows Media Format SDK，DRM 寫入功能
- Windows Media Format SDK，file 接收
- 'Windows Media Format SDK、DirectX Video 加速 (DXVA) '
- Windows Media Format SDK，多頻道音訊
- Windows Media Format SDK，浮水印
- Windows Media Format SDK，多重語言支援
- Windows Media Format SDK，裝置一致性範本
- Windows Media Format SDK，編解碼器列舉
- Windows Media Format SDK，相互排除
- Windows Media 格式 SDK， (MBR) 多位元率
- Windows Media Format SDK，使用智慧型 recompression 進行轉碼
- Windows Media Format SDK、smart recompression
- Windows Media Format SDK、recompression
- Windows Media Format SDK，中繼資料
- Windows Media Format SDK，動態圖元外觀比例
- Windows Media Format SDK，交錯式影片串流
- Windows Media Format SDK，雙通編碼
- Windows Media Format SDK、WMStub .lib
- 同步讀取器，關於
- 以框架為基礎的索引
- SMPTE 時間代碼，關於
- DirectShow 篩選
- 檔案接收，增強功能
- 多頻道音訊，關於
- 浮水印，關於
- 編解碼器，列舉
- 相互排除，關於
- 數位版權管理 (DRM) ，寫入功能
- DRM (數位版權管理) ，書寫功能
- DirectX Video 加速 (DXVA) ，關於
- DXVA (DirectX Video 加速) ，關於
- Advanced Systems Format (ASF) 、多重語言支援
- ASF (Advanced Systems Format) 、多重語言支援
- " (MBR) 的多重位元速率，關於"
- MBR (多位元率) ，關於
- 使用智慧型 recompression 進行轉碼
- 智慧型 recompression
- recompression
- 中繼資料，Windows Media Format SDK
- 動態圖元外觀比例
- 交錯式影片串流
- 雙通路編碼，關於
- 2-通過編碼，關於
- WMStub .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183566"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="2f832-153">Windows Media Format 9 系列 SDK 中新增的功能</span><span class="sxs-lookup"><span data-stu-id="2f832-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="2f832-154">Windows Media Format 9 系列 SDK 引進了許多改進和功能。</span><span class="sxs-lookup"><span data-stu-id="2f832-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="2f832-155">本節概述從舊版 SDK 進行遷移的使用者所具備的優點。</span><span class="sxs-lookup"><span data-stu-id="2f832-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="2f832-156">同步讀取</span><span class="sxs-lookup"><span data-stu-id="2f832-156">Synchronous Reading</span></span>

<span data-ttu-id="2f832-157">您可以使用同步呼叫來讀取 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="2f832-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="2f832-158">以同步方式讀取檔案時，您可以在讀取時變更讀取器的設定。</span><span class="sxs-lookup"><span data-stu-id="2f832-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="2f832-159">SDK 的同步讀取作業不支援透過網際網路讀取檔案，但您可以使用標準 COM 介面 **IStream**，從自訂來源讀取。</span><span class="sxs-lookup"><span data-stu-id="2f832-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="2f832-160">以框架為基礎的索引</span><span class="sxs-lookup"><span data-stu-id="2f832-160">Frame-based Indexing</span></span>

<span data-ttu-id="2f832-161">您可以根據影片畫面來編制 ASF 檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="2f832-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="2f832-162">讀取器和同步讀取器都可以搜尋影片資料流程的框架，並將其他資料流程同步處理至該框架。</span><span class="sxs-lookup"><span data-stu-id="2f832-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="2f832-163">使用 SMPTE 時間碼來編制索引和搜尋</span><span class="sxs-lookup"><span data-stu-id="2f832-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="2f832-164">Windows Media Format SDK 可讓您將 SMPTE 時間代碼儲存在 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="2f832-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="2f832-165">檔案可以透過 SMPTE 時間程式碼來編制索引，而非同步讀取器和同步讀取器可以搜尋 SMPTE 時間的程式碼索引項目。</span><span class="sxs-lookup"><span data-stu-id="2f832-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="2f832-166">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="2f832-166">DirectShow Filters</span></span>

<span data-ttu-id="2f832-167">Windows Media Format SDK 包含兩個 Microsoft DirectShow®篩選器，可讓 DirectShow 型應用程式讀取和寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="2f832-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="2f832-168">DirectShow 也可讓應用程式從音訊視頻裝置捕獲資料，並從各種不同的格式解壓縮資料，然後再將其編碼為 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="2f832-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="2f832-169">增強型設定檔</span><span class="sxs-lookup"><span data-stu-id="2f832-169">Enhanced Profiles</span></span>

<span data-ttu-id="2f832-170">設定檔可以包含頻寬共用資訊，以及串流優先順序資訊。</span><span class="sxs-lookup"><span data-stu-id="2f832-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="2f832-171">頻寬共用可讓您指定兩個或多個資料流程（不論其個別的位元速率為何）永遠不會使用超過指定的頻寬量。</span><span class="sxs-lookup"><span data-stu-id="2f832-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="2f832-172">設定檔中共用資料的頻寬純粹僅供參考;SDK 中的任何邏輯都不會強制執行。</span><span class="sxs-lookup"><span data-stu-id="2f832-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="2f832-173">資料流程優先順序可讓您針對設定檔中的資料流程指定優先權順序。</span><span class="sxs-lookup"><span data-stu-id="2f832-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="2f832-174">如果在播放時沒有足夠的頻寬可正常串流檔案，則可以忽略最低優先順序的資料流程，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="2f832-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="2f832-175">DRM 寫入功能</span><span class="sxs-lookup"><span data-stu-id="2f832-175">DRM Writing Capability</span></span>

<span data-ttu-id="2f832-176">除了現有的 DRM 讀取支援，Windows Media Format 9 系列 SDK 還新增了使用 DRM 第1版或 DRM 版本7保護來撰寫 ASF 檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="2f832-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="2f832-177">這項新功能可提供「即時 DRM」案例，例如即時體育活動或演唱會的每一視圖網路廣播。</span><span class="sxs-lookup"><span data-stu-id="2f832-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="2f832-178">增強的檔案接收</span><span class="sxs-lookup"><span data-stu-id="2f832-178">Enhanced File Sink</span></span>

<span data-ttu-id="2f832-179">9系列版本的 SDK 新增了數個新的檔案接收功能。</span><span class="sxs-lookup"><span data-stu-id="2f832-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="2f832-180">您可以設定檔案接收，以停用自動編制新建立之 ASF 檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="2f832-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="2f832-181">您也可以選擇將它設定為未緩衝的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="2f832-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="2f832-182">DirectX 影片加速</span><span class="sxs-lookup"><span data-stu-id="2f832-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="2f832-183">DirectX Video 加速 (DXVA) 是一種技術，可讓您以具有 DXVA 功能的圖形配接器，在功能較少的電腦上播放高位速率的影片 (DVD 品質或更好的) 。</span><span class="sxs-lookup"><span data-stu-id="2f832-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="2f832-184">您可以使用此 SDK 的 reader 物件，在播放 ASF 檔案時啟用 DirectX Video 加速（如果硬體支援的話）。</span><span class="sxs-lookup"><span data-stu-id="2f832-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="2f832-185">多頻道音訊</span><span class="sxs-lookup"><span data-stu-id="2f832-185">Multichannel Audio</span></span>

<span data-ttu-id="2f832-186">您可以編碼和播放多頻道音訊。</span><span class="sxs-lookup"><span data-stu-id="2f832-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="2f832-187">Windows Media 音訊 9 Professional 編解碼器支援具有6個通道和8個通道以及高定義身歷聲的格式。</span><span class="sxs-lookup"><span data-stu-id="2f832-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="2f832-188">浮水印</span><span class="sxs-lookup"><span data-stu-id="2f832-188">Watermarking</span></span>

<span data-ttu-id="2f832-189">您可以使用數位浮水印來編碼 ASF 檔案，以獲得安全性。</span><span class="sxs-lookup"><span data-stu-id="2f832-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="2f832-190">所有浮水印系統在其方法中都不同，但所有內嵌識別碼都是編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="2f832-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="2f832-191">浮水印是使用特殊的協力廠商 DirectX®媒體物件 (DMOs) 來執行。</span><span class="sxs-lookup"><span data-stu-id="2f832-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="2f832-192">在 ASF 檔案中支援多種語言</span><span class="sxs-lookup"><span data-stu-id="2f832-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="2f832-193">您可以在多個 ASF 檔案中支援多種語言，包括資料流程和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2f832-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="2f832-194">例如，您可以使用數種語言建立包含音訊串流的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="2f832-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="2f832-195">在播放時，使用者可以選取要使用的語言，或您的應用程式可以查詢播放電腦上的系統資訊，並自動選取語言。</span><span class="sxs-lookup"><span data-stu-id="2f832-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="2f832-196">中繼資料屬性也可以多次輸入，並以不同語言的值。</span><span class="sxs-lookup"><span data-stu-id="2f832-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="2f832-197">裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="2f832-197">Device Conformance Templates</span></span>

<span data-ttu-id="2f832-198">為了協助將內容設定為特定用戶端裝置，Windows Media 編解碼器現在支援裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="2f832-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="2f832-199">每個範本都包含一組已定義的設定和編解碼器功能，這些功能應用於適用于特定平臺類別的媒體。</span><span class="sxs-lookup"><span data-stu-id="2f832-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="2f832-200">Windows Media 編解碼器的最新版本不再支援系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f832-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="2f832-201">所有設定檔都必須自訂，以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="2f832-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="2f832-202">您可以使用「裝置一致性範本」來協助您設計您的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f832-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="2f832-203">擴充的編解碼器列舉</span><span class="sxs-lookup"><span data-stu-id="2f832-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="2f832-204">配置檔案管理員物件可以查詢 Windows Media 音訊和影片編解碼器，以取得支援的格式。</span><span class="sxs-lookup"><span data-stu-id="2f832-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="2f832-205">您可以設定所抓取格式的參數。</span><span class="sxs-lookup"><span data-stu-id="2f832-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="2f832-206">例如，您可以取出 Windows Media 音訊9編解碼器所支援的所有品質型變數位速率格式。</span><span class="sxs-lookup"><span data-stu-id="2f832-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="2f832-207">改進互斥</span><span class="sxs-lookup"><span data-stu-id="2f832-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="2f832-208">您可以建立包含相互排除物件內多個資料流程的命名記錄。</span><span class="sxs-lookup"><span data-stu-id="2f832-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="2f832-209">您也可以命名相互排除物件，使其更容易識別。</span><span class="sxs-lookup"><span data-stu-id="2f832-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="2f832-210">這可讓您建立相互排除的層級。</span><span class="sxs-lookup"><span data-stu-id="2f832-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="2f832-211">例如，檔案可以包含依位元速率和語言相互排斥的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2f832-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="2f832-212">以語言為基礎的相互排除牽涉到資料流程群組，每個群組都是由相同語言的資料流程所組成，但位元速率互斥。</span><span class="sxs-lookup"><span data-stu-id="2f832-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="2f832-213">擴充的多位元率支援</span><span class="sxs-lookup"><span data-stu-id="2f832-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="2f832-214">相互排除支援包含在多個位速率內 (MBR) 音訊，以及串流不同映射大小的影片。</span><span class="sxs-lookup"><span data-stu-id="2f832-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="2f832-215">資料流程的屬性</span><span class="sxs-lookup"><span data-stu-id="2f832-215">Attributes for Streams</span></span>

<span data-ttu-id="2f832-216">您可以將屬性指派給 ASF 檔案中的個別資料流程。</span><span class="sxs-lookup"><span data-stu-id="2f832-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="2f832-217">您仍然必須針對 MP3 檔案使用檔案層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f832-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="2f832-218">這項功能不會將任何方法新增至 SDK，但現有的方法現在會接受零以外的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="2f832-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="2f832-219">使用智慧型 Recompression 進行轉碼</span><span class="sxs-lookup"><span data-stu-id="2f832-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="2f832-220">Smart recompression 可讓您以比以往更高的品質，以較高的位元速率轉碼 Windows Media 音訊檔案與較低的位元速率。</span><span class="sxs-lookup"><span data-stu-id="2f832-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="2f832-221">擴充的中繼資料支援</span><span class="sxs-lookup"><span data-stu-id="2f832-221">Expanded Metadata Support</span></span>

<span data-ttu-id="2f832-222">Windows Media Format SDK 提供下列新的中繼資料功能：</span><span class="sxs-lookup"><span data-stu-id="2f832-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="2f832-223">以索引為基礎的元資料標記，啟用多個具有相同名稱的標記。</span><span class="sxs-lookup"><span data-stu-id="2f832-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="2f832-224">能夠讀取不含 WMStubDRM .lib 檔案的 DRM 標頭屬性。</span><span class="sxs-lookup"><span data-stu-id="2f832-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="2f832-225">具有超過 64 kb 相關聯資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f832-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="2f832-226">多種語言的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f832-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="2f832-227">數十個新的預先定義屬性。</span><span class="sxs-lookup"><span data-stu-id="2f832-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="2f832-228">動態圖元外觀比例</span><span class="sxs-lookup"><span data-stu-id="2f832-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="2f832-229">您可以藉由識別資料流程中不同樣本的圖元外觀比例，來容納包含各種內容類型的影片串流。</span><span class="sxs-lookup"><span data-stu-id="2f832-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="2f832-230">這可讓播放應用程式提供更好的內容播放。</span><span class="sxs-lookup"><span data-stu-id="2f832-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="2f832-231">交錯式影片串流</span><span class="sxs-lookup"><span data-stu-id="2f832-231">Interlaced Video Streams</span></span>

<span data-ttu-id="2f832-232">舊版 Windows Media 格式 SDK 已提供將 [*交錯*](wmformat-glossary.md) 式內容編碼成漸進式掃描影片串流的功能。</span><span class="sxs-lookup"><span data-stu-id="2f832-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="2f832-233">從 Windows Media Format 9 系列 SDK 開始，您可以編碼交錯式影片，同時保留其交錯式格式。</span><span class="sxs-lookup"><span data-stu-id="2f832-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="2f832-234">這可能會導致播放改善，特別是在交錯裝置上，例如電視組。</span><span class="sxs-lookup"><span data-stu-id="2f832-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="2f832-235">Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="2f832-235">Two-Pass Encoding</span></span>

<span data-ttu-id="2f832-236">新的 Windows Media 編解碼器可啟用兩個傳遞的編碼。</span><span class="sxs-lookup"><span data-stu-id="2f832-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="2f832-237">在兩個階段中編碼的內容可以達到更高品質的輸出。</span><span class="sxs-lookup"><span data-stu-id="2f832-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="2f832-238">新的語音編解碼器</span><span class="sxs-lookup"><span data-stu-id="2f832-238">New Speech Codec</span></span>

<span data-ttu-id="2f832-239">此 SDK 包含新的 Windows Media 音訊9語音編解碼器，最適合用來在使用低位速率的情況下編碼人類聲音。</span><span class="sxs-lookup"><span data-stu-id="2f832-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="2f832-240">此編解碼器也可為混合音樂-語音內容提供絕佳的效能。</span><span class="sxs-lookup"><span data-stu-id="2f832-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="2f832-241">可存取的影片畫面持續時間</span><span class="sxs-lookup"><span data-stu-id="2f832-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="2f832-242">您可以讓此 SDK 的寫入器物件將影片畫面的持續時間提供給讀者。</span><span class="sxs-lookup"><span data-stu-id="2f832-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="2f832-243">串流 HTML</span><span class="sxs-lookup"><span data-stu-id="2f832-243">Streaming HTML</span></span>

<span data-ttu-id="2f832-244">在舊版的 SDK 中，您可以使用指令碼命令來指示您的應用程式開啟網頁。</span><span class="sxs-lookup"><span data-stu-id="2f832-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="2f832-245">從 Windows Media Format 9 系列 SDK 開始，您可以在 ASF 檔案中儲存網頁的元件，以確保簡報中沒有任何延隔時間。</span><span class="sxs-lookup"><span data-stu-id="2f832-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="2f832-246">組建環境不再需要 WMStub .lib</span><span class="sxs-lookup"><span data-stu-id="2f832-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="2f832-247">Windows Media format SDK 的組建環境設定從 Windows Media Format 9 系列 SDK 開始變更。</span><span class="sxs-lookup"><span data-stu-id="2f832-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="2f832-248">您不再需要為使用此 SDK 的應用程式包含 WMStub。</span><span class="sxs-lookup"><span data-stu-id="2f832-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="2f832-249">不過，啟用 DRM 的應用程式仍然必須取得並簽署個別的授權合約，並從 Microsoft 取得唯一的靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="2f832-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="2f832-250">wmla@microsoft.com如需 DRM 程式庫和授權合約的詳細資訊，請洽詢。</span><span class="sxs-lookup"><span data-stu-id="2f832-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="2f832-251">如需使用此 SDK 建立專案的詳細資訊，請參閱連結 [庫檔案和編譯器設定](library-files-and-compiler-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="2f832-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f832-252">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f832-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f832-253">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="2f832-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




