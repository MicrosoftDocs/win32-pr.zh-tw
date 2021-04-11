---
description: 媒體基礎介面
ms.assetid: 3e367190-4c88-430e-adbf-9837e1bf0d2b
title: 媒體基礎介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12379dc83287b2a03ae0223a5a9a7d945d8fa77
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945605"
---
# <a name="media-foundation-interfaces"></a>媒體基礎介面

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapture"><strong>IAdvancedMediaCapture</strong></a><br/></td>
<td>啟用 advanced media capture。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediacapture/nn-mfmediacapture-iadvancedmediacaptureinitializationsettings"><strong>IAdvancedMediaCaptureInitializationSettings</strong></a><br/></td>
<td>提供 advanced media capture 的初始設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapturesettings"><strong>IAdvancedMediaCaptureSettings</strong></a><br/></td>
<td>提供 advanced media capture 的設定。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9"><strong>IDirect3DDeviceManager9</strong></a><br/></td>
<td>可讓兩個執行緒共用相同的 Direct3D 9 裝置，並可讓您存取裝置的 DirectX Video 加速 (DXVA) 功能。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice"><strong>IDirectXVideoAccelerationService</strong></a><br/></td>
<td>提供從 Direct3D 裝置 (DXVA) 服務的 DirectX 影片加速。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder"><strong>IDirectXVideoDecoder</strong></a><br/></td>
<td>代表 DirectX Video 加速 (DXVA) 影片解碼裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice"><strong>IDirectXVideoDecoderService</strong></a><br/></td>
<td>提供 (DXVA) 解碼器服務的 DirectX Video 加速存取。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a><br/></td>
<td>設定未壓縮影片表面的視訊記憶體類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor"><strong>IDirectXVideoProcessor</strong></a><br/></td>
<td>代表 DirectX Video 加速 (DXVA) Video 處理器裝置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice"><strong>IDirectXVideoProcessorService</strong></a><br/></td>
<td>提供存取 DirectX Video 加速 (DXVA) 影片處理服務。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a><br/></td>
<td>設定 DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>增強型影片</strong></a> 轉譯器上的輸入釘選數目 (EVR) 篩選。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex"><strong>IEVRFilterConfigEx</strong></a><br/></td>
<td>設定 DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>增強型影片</strong></a> 轉譯器 (EVR) 篩選。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin"><strong>IEVRTrustedVideoPlugin</strong></a><br/></td>
<td>啟用增強型影片轉譯器的外掛程式元件， (EVR) 使用受保護的媒體。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a><br/></td>
<td>不支援此介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer"><strong>IMF2DBuffer</strong></a><br/></td>
<td>表示包含二維表面的緩衝區，例如影片畫面。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2"><strong>IMF2DBuffer2</strong></a><br/></td>
<td>表示包含二維表面的緩衝區，例如影片畫面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate"><strong>IMFActivate</strong></a><br/></td>
<td>讓應用程式延遲建立物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo"><strong>IMFASFContentInfo</strong></a><br/></td>
<td>提供方法，以使用符合 Advanced 系統格式之檔案的標頭區段， (ASF) 規格。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer"><strong>IMFASFIndexer</strong></a><br/></td>
<td>提供方法來使用系統格式的索引， (ASF) 檔。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer"><strong>IMFASFMultiplexer</strong></a><br/></td>
<td>提供方法來建立 Advanced 系統格式 (ASF) 資料封包。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion"><strong>IMFASFMutualExclusion</strong></a><br/></td>
<td>設定 Advanced 系統格式 (ASF) 相互排除物件，此物件會管理有關 ASF 設定檔中互斥的資料流程群組的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile"><strong>IMFASFProfile</strong></a><br/></td>
<td>管理 (ASF) 設定檔的 Advanced Systems 格式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter"><strong>IMFASFSplitter</strong></a><br/></td>
<td>提供從 Advanced 系統格式讀取資料的方法， (ASF) 檔。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig"><strong>IMFASFStreamConfig</strong></a><br/></td>
<td>在 ASF 檔案中設定資料流程的設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization"><strong>IMFASFStreamPrioritization</strong></a><br/></td>
<td>未實作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector"><strong>IMFASFStreamSelector</strong></a><br/></td>
<td>根據 ASF 標頭中的相互排除資訊，以 Advanced Systems 格式 (ASF) 檔案來選取資料流程。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback"><strong>IMFAsyncCallback</strong></a><br/></td>
<td>非同步方法完成時，用來通知應用程式的回呼介面。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mfobjects/nn-mfobjects-imfasynccallbacklogging"><strong>IMFAsyncCallbackLogging</strong></a><br/></td>
<td>提供與非同步回呼相關聯之父物件的記錄資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a><br/></td>
<td>提供非同步作業結果的相關資訊。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a><br/></td>
<td>提供在物件上儲存索引鍵/值組的一般方式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a> 不再適用于 Windows 7。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy"><strong>IMFAudioPolicy</strong></a><br/></td>
<td>設定與串流音訊轉譯器 (特別行政區) 相關聯的音訊會話。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume"><strong>IMFAudioStreamVolume</strong></a><br/></td>
<td>控制個別音訊頻道的音量層級。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfbufferlistnotify"><strong>IMFBufferListNotify</strong></a><br/></td>
<td>可讓 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a> 物件通知其用戶端有重大狀態變更。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream"><strong>IMFByteStream</strong></a><br/></td>
<td>表示來自某個資料來源的位元組資料流程，它可能是本機檔案、網路檔案或其他來源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering"><strong>IMFByteStreamBuffering</strong></a><br/></td>
<td>控制位元組資料流程如何從網路緩衝資料。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol"><strong>IMFByteStreamCacheControl</strong></a><br/></td>
<td>控制網路位元組資料流程將資料傳輸至本機快取的方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2"><strong>IMFByteStreamCacheControl2</strong></a><br/></td>
<td>控制網路位元組資料流程將資料傳輸至本機快取的方式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler"><strong>IMFByteStreamHandler</strong></a><br/></td>
<td>從位元組資料流程建立媒體來源。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory"><strong>IMFByteStreamProxyClassFactory</strong></a><br/></td>
<td>建立位元組資料流程的 proxy。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek"><strong>IMFByteStreamTimeSeek</strong></a><br/></td>
<td>依時間位置搜尋位元組資料流程。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine"><strong>IMFCaptureEngine</strong></a><br/></td>
<td>控制一或多個 capture 裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory"><strong>IMFCaptureEngineClassFactory</strong></a><br/></td>
<td>建立 capture 引擎的實例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback"><strong>IMFCaptureEngineOnEventCallback</strong></a><br/></td>
<td>從 capture 引擎接收事件的回呼介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a><br/></td>
<td>從 capture 引擎接收資料的回呼介面。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2"><strong>IMFCaptureEngineOnSampleCallback2</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a>回呼介面的延伸模組，用來接收來自 capture 引擎的資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink"><strong>IMFCapturePhotoSink</strong></a><br/></td>
<td>控制相片接收器。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink"><strong>IMFCapturePreviewSink</strong></a><br/></td>
<td>控制預覽接收。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink"><strong>IMFCaptureRecordSink</strong></a><br/></td>
<td>控制記錄接收。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a><br/></td>
<td>控制捕捉接收，也就是從捕獲裝置接收一或多個資料流程的物件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink2"><strong>IMFCaptureSink2</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a> 介面，以提供動態設定記錄接收或預覽接收之輸出媒體類型的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource"><strong>IMFCaptureSource</strong></a><br/></td>
<td>控制 capture 來源物件。 「捕獲來源」會管理音訊和影片捕獲裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify"><strong>IMFCdmSuspendNotify</strong></a><br/></td>
<td>用來讓用戶端通知內容解密模組 (CDM) 當全域資源應該在暫停之前進入一致狀態。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock"><strong>IMFClock</strong></a><br/></td>
<td>從 Microsoft 媒體基礎中的時鐘提供時間資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer"><strong>IMFClockConsumer</strong></a><br/></td>
<td>由應用程式執行，以取得 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a>的存取權。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink"><strong>IMFClockStateSink</strong></a><br/></td>
<td>從呈現時鐘接收狀態變更通知。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection"><strong>IMFCollection</strong></a><br/></td>
<td>表示 <strong>IUnknown</strong> 指標的泛型集合。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext"><strong>IMFContentDecryptorCoNtext</strong></a><br/></td>
<td>允許解密器管理硬體金鑰和解密硬體範例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler"><strong>IMFContentEnabler</strong></a><br/></td>
<td>會執行一個步驟，讓使用者必須執行該步驟才能存取媒體內容。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice"><strong>IMFContentProtectionDevice</strong></a><br/></td>
<td>允許解密程式與安全性處理器進行通訊，以執行保護系統的硬體解密。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager"><strong>IMFContentProtectionManager</strong></a><br/></td>
<td>藉由提供應用程式內容啟用程式物件的指標，來啟用受保護內容的播放。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample"><strong>IMFDesiredSample</strong></a><br/></td>
<td>讓展示者可以使用增強型影片轉譯器 (EVR) 從視頻混音器要求特定的畫面格。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit"><strong>IMFDLNASinkInit</strong></a><br/></td>
<td> (DLNA) 媒體接收器初始化數位客廳網路聯盟。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper"><strong>IMFDRMNetHelper</strong></a><br/></td>
<td>針對網路接收上的網路裝置，設定 Windows Media 數位 Rights Management (DRM) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer"><strong>IMFDXGIBuffer</strong></a><br/></td>
<td>表示包含 Microsoft DirectX Graphic Infrastructure (DXGI) 介面的緩衝區。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a><br/></td>
<td>可讓兩個執行緒共用相同的 Microsoft Direct3D 11 裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="imfdxgidevicemanagersource.md"><strong>IMFDXGIDeviceManagerSource</strong></a><br/></td>
<td>提供從媒體基礎 video 轉譯接收器取得 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a> 的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock"><strong>IMFFieldOfUseMFTUnlock</strong></a><br/></td>
<td>讓應用程式使用媒體基礎轉換 (MFT) 的使用方式限制。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink"><strong>IMFFinalizableMediaSink</strong></a><br/></td>
<td>在關機之前，媒體接收器可選擇性地支援執行必要的工作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a><br/></td>
<td>查詢指定服務介面的物件。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest"><strong>IMFHttpDownloadRequest</strong></a><br/></td>
<td>應用程式會執行這個介面，以覆寫 Microsoft 媒體基礎所使用的 HTTP 和 HTTPS 通訊協定的預設實值。 應用程式會透過<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a>介面上的<a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest"><strong>CreateRequest</strong></a>方法，提供<strong>IMFHttpDownloadRequest</strong>介面給媒體基礎。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a><br/></td>
<td>應用程式會執行這個介面，以覆寫 Microsoft 媒體基礎所使用的 HTTP 和 HTTPS 通訊協定的預設實值。 應用程式會透過<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a>介面上的<a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a>方法，提供<strong>IMFHttpDownloadSession</strong>介面給媒體基礎。 Microsoft 媒體基礎使用此介面來執行「串流」或「漸進式」，以下載由 HTTP 或 HTTPS URL 識別的資源。 可能會傳送多個 HTTP 要求以下載資源。 <strong>IMFHttpDownloadSession</strong>介面是用來建立這些個別的 HTTP 要求。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a><br/></td>
<td>應用程式會執行這個介面，以便提供自訂的 HTTP 或 HTTPS 下載執行。 您可以使用 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a> 介面來註冊提供者。 如需詳細資訊，請參閱 <a href="using-the-source-resolver.md">使用來源解析程式</a>。 註冊之後，Microsoft 媒體基礎會叫用提供者執行的 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> 方法，以開啟 HTTP 或 HTTPS url，而不是使用預設的實值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a><br/></td>
<td>啟用影像共用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory"><strong>IMFImageSharingEngineClassFactory</strong></a><br/></td>
<td>建立 <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a>的實例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority"><strong>IMFInputTrustAuthority</strong></a><br/></td>
<td>啟用受保護媒體路徑中的其他元件 (PMP) 使用輸入信任授權單位所提供的輸入保護系統 (ITA) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration"><strong>IMFLocalMFTRegistration</strong></a><br/></td>
<td>在呼叫端的進程中註冊媒體基礎轉換 (MFTs) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer"><strong>IMFMediaBuffer</strong></a><br/></td>
<td>代表包含媒體資料的記憶體區塊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a><br/></td>
<td>讓應用程式播放音訊或影片檔案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a><br/></td>
<td>建立媒體引擎的實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2"><strong>IMFMediaEngineClassFactory2</strong></a><br/></td>
<td>建立 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a> 物件的實例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex"><strong>IMFMediaEngineClassFactoryEx</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a>介面的延伸模組。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme"><strong>IMFMediaEngineEME</strong></a><br/></td>
<td>由媒體引擎執行以新增加密的媒體擴充方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex"><strong>IMFMediaEngineEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> 介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension"><strong>IMFMediaEngineExtension</strong></a><br/></td>
<td>讓應用程式在 Media Engine 中載入媒體資源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify"><strong>IMFMediaEngineNeedKeyNotify</strong></a><br/></td>
<td>表示對媒體引擎的回呼，以通知金鑰要求資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify"><strong>IMFMediaEngineNotify</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a>介面的回呼介面。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo"><strong>IMFMediaEngineOPMInfo</strong></a><br/></td>
<td>提供方法來取得 <a href="output-protection-manager.md">輸出保護管理員</a> (OPM) 的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent"><strong>IMFMediaEngineProtectedContent</strong></a><br/></td>
<td>讓媒體引擎播放受保護的影片內容。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a><br/></td>
<td>提供媒體引擎媒體資源的清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex"><strong>IMFMediaEngineSrcElementsEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a> 介面以提供額外的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer"><strong>IMFMediaEngineSupportsSourceTransfer</strong></a><br/></td>
<td>可在媒體引擎和共用引擎之間傳輸媒體來源以進行播放至。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginewebsupport"><strong>IMFMediaEngineWebSupport</strong></a><br/></td>
<td>啟用 web 音訊的播放。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror"><strong>IMFMediaError</strong></a><br/></td>
<td>提供媒體引擎目前的錯誤狀態。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent"><strong>IMFMediaEvent</strong></a><br/></td>
<td>代表媒體基礎物件所產生的事件。 使用這個介面可取得事件的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a><br/></td>
<td>從產生事件的任何媒體基礎物件抓取事件。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue"><strong>IMFMediaEventQueue</strong></a><br/></td>
<td>針對需要執行 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a> 介面的應用程式，提供事件佇列。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a><br/></td>
<td>代表用來使用數位 Rights Management (DRM) 金鑰系統來解密媒體資料的媒體金鑰。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession"><strong>IMFMediaKeySession</strong></a><br/></td>
<td>代表具有數位 Rights Management (DRM) 金鑰系統的會話。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysessionnotify"><strong>IMFMediaKeySessionNotify</strong></a><br/></td>
<td>提供一種機制，用來通知應用程式有關媒體金鑰會話的資訊。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession"><strong>IMFMediaSession</strong></a><br/></td>
<td>提供受保護和未受保護內容的播放控制項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a><br/></td>
<td>啟用媒體共用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory"><strong>IMFMediaSharingEngineClassFactory</strong></a><br/></td>
<td>建立 <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a>的實例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink"><strong>IMFMediaSink</strong></a><br/></td>
<td>由媒體接收器物件所執行。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll"><strong>IMFMediaSinkPreroll</strong></a><br/></td>
<td>讓媒體接收器在簡報時鐘開始之前接收範例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a><br/></td>
<td>由媒體來源物件所執行。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex"><strong>IMFMediaSourceEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> 介面以提供媒體來源的額外功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a><br/></td>
<td>提供媒體來源延伸 (MSE) 的功能。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextensionnotify"><strong>IMFMediaSourceExtensionNotify</strong></a><br/></td>
<td>提供可引發與 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>相關聯之事件的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider"><strong>IMFMediaSourcePresentationProvider</strong></a><br/></td>
<td>提供對 sequencer 來源的通知。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider"><strong>IMFMediaSourceTopologyProvider</strong></a><br/></td>
<td>讓應用程式從 sequencer 來源取得拓撲。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream"><strong>IMFMediaStream</strong></a><br/></td>
<td>表示媒體來源中的一個資料流程。 <br/></td>
</tr>
<tr class="odd">
<td><a href="imfmediastreamsourcesamplerequest.md"><strong>IMFMediaStreamSourceSampleRequest</strong></a><br/></td>
<td>表示來自 >mediastreamsource 的範例要求。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange"><strong>IMFMediaTimeRange</strong></a><br/></td>
<td>代表時間範圍的清單，其中每個範圍都是由開始和結束時間所定義。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype"><strong>IMFMediaType</strong></a><br/></td>
<td>表示媒體格式的描述。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler"><strong>IMFMediaTypeHandler</strong></a><br/></td>
<td>取得和設定物件上的媒體類型，例如媒體來源或媒體接收器。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata"><strong>IMFMetadata</strong></a><br/></td>
<td>管理物件的中繼資料。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a><br/></td>
<td>從媒體來源或其他物件取得中繼資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager"><strong>IMFMuxStreamAttributesManager</strong></a><br/></td>
<td>提供對多工媒體來源之子串流 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a> 的存取權。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager"><strong>IMFMuxStreamSampleManager</strong></a><br/></td>
<td>提供在多工媒體來源的輸出中，針對個別子串流取得 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a> 物件的能力。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager"><strong>IMFMuxStreamMediaTypeManager</strong></a><br/></td>
<td>啟用多工媒體來源的串流設定管理。 資料流程設定會定義一組可以包含多工輸出的子串流。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential"><strong>IMFNetCredential</strong></a><br/></td>
<td>設定及抓取使用者名稱和密碼資訊以供驗證之用。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache"><strong>IMFNetCredentialCache</strong></a><br/></td>
<td>從認證快取取得認證。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager"><strong>IMFNetCredentialManager</strong></a><br/></td>
<td>由應用程式所執行，提供網路來源的使用者認證。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcrossoriginsupport"><strong>IMFNetCrossOriginSupport</strong></a><br/></td>
<td>由想要強制執行 HTML5 媒體下載的跨原始原則的用戶端所執行。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator"><strong>IMFNetProxyLocator</strong></a><br/></td>
<td>決定連接到伺服器時要使用的 proxy。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory"><strong>IMFNetProxyLocatorFactory</strong></a><br/></td>
<td>建立 proxy 定位器物件，以決定要使用的 proxy。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter"><strong>IMFNetResourceFilter</strong></a><br/></td>
<td>當位元組資料流程要求 URL 時通知應用程式，並讓應用程式封鎖 URL 重新導向。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig"><strong>IMFNetSchemeHandlerConfig</strong></a><br/></td>
<td>設定網路設定外掛程式。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream"><strong>IMFObjectReferenceStream</strong></a><br/></td>
<td>封送處理資料流程的介面指標。 <br/> 支援 <strong>IStream</strong> 的資料流程物件可以公開這個介面，以提供介面指標的自訂封送處理。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy"><strong>IMFOutputPolicy</strong></a><br/></td>
<td>將輸入信任授權單位的使用原則封裝 (ITA) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema"><strong>IMFOutputSchema</strong></a><br/></td>
<td>封裝輸出保護系統及其對應設定資料的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority"><strong>IMFOutputTrustAuthority</strong></a><br/></td>
<td>封裝受信任的輸出支援的一或多個輸出保護系統的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol"><strong>IMFPluginControl</strong></a><br/></td>
<td>控制如何在媒體基礎中列舉媒體來源和轉換。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2"><strong>IMFPluginControl2</strong></a><br/></td>
<td>控制如何在媒體基礎中列舉媒體來源和轉換。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem"><strong>IMFPMediaItem</strong></a><br/></td>
<td>表示媒體專案。 (已取代。)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a><br/></td>
<td>包含用來播放媒體檔案的方法。 (已取代。)<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback"><strong>IMFPMediaPlayerCallback</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a>介面的回呼介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient"><strong>IMFPMPClient</strong></a><br/></td>
<td>讓媒體來源接收 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a> 介面的指標。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp"><strong>IMFPMPClientApp</strong></a><br/></td>
<td>提供媒體來源的機制，以在 Windows Store 應用程式中執行內容保護功能。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a><br/></td>
<td>讓應用程式進程中的媒體來源在受保護的媒體路徑中建立物件 (PMP) 進程。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp"><strong>IMFPMPHostApp</strong></a><br/></td>
<td>允許媒體來源在<a href="protected-media-path.md">受保護的媒體路徑</a>中建立<a href="/windows/desktop/WinRT/reference">WINDOWS 執行階段</a>物件 (PMP) 處理常式。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver"><strong>IMFPMPServer</strong></a><br/></td>
<td>可讓兩個 <a href="media-session.md">媒體會話</a> 實例共用相同的受保護媒體路徑 (PMP) 進程。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a><br/></td>
<td>代表標記法，用來排程轉譯樣本的時間，以及同步處理多個資料流程。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor"><strong>IMFPresentationDescriptor</strong></a><br/></td>
<td>描述簡報的詳細資料。 <em>簡報</em>是一組共用常見展示時間的相關媒體串流。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource"><strong>IMFPresentationTimeSource</strong></a><br/></td>
<td>提供標記法時鐘的時鐘時間。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess"><strong>IMFProtectedEnvironmentAccess</strong></a><br/></td>
<td>提供一種方法，可讓內容保護系統與受保護的環境執行交握。 這是必要的，因為 <strong>CreateFile</strong> 和 <strong>DeviceIoControl</strong> Api 無法供 Windows Store 應用程式使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a><br/></td>
<td>可讓品質管制員調整管線中元件的音訊或影片品質。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a><br/></td>
<td>可讓管線物件調整其本身的音訊或影片品質，以回應品質訊息。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits"><strong>IMFQualityAdviseLimits</strong></a><br/></td>
<td>查詢物件，以取得其支援的 <em>品質模式</em> 數目。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager"><strong>IMFQualityManager</strong></a><br/></td>
<td>調整播放品質。 此介面是由 quality manager 所公開。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a><br/></td>
<td>取得或設定播放速率。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a><br/></td>
<td>查詢支援的播放率範圍，包括反向播放。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory"><strong>IMFReadWriteClassFactory</strong></a><br/></td>
<td>建立接收寫入器或來源讀取器的實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a><br/></td>
<td>通知管線物件將本身註冊到多媒體類別排程器服務 (MMCSS) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex"><strong>IMFRealTimeClientEx</strong></a><br/></td>
<td>通知管線物件將本身註冊到多媒體類別排程器服務 (MMCSS) 。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfremoteasynccallback"><strong>IMFRemoteAsyncCallback</strong></a><br/></td>
<td>由媒體基礎 proxy/stub DLL 用來跨進程界限封送處理特定的非同步方法呼叫。<br/> 應用程式不會使用或執行這個介面。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin"><strong>IMFRemoteDesktopPlugin</strong></a><br/></td>
<td>修改要在終端機服務環境中使用的拓撲。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy"><strong>IMFRemoteProxy</strong></a><br/></td>
<td>由作為遠端物件之 proxy 的物件所公開。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle"><strong>IMFSAMIStyle</strong></a><br/></td>
<td>設定及抓取 <a href="sami-media-source.md">薩米媒體來源</a>上的已同步可存取媒體交換 (薩米) 樣式。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a><br/></td>
<td>表示媒體範例，也就是媒體資料的容器物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a><br/></td>
<td>回呼介面，可從範例-捕獲接收器取得媒體資料。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2"><strong>IMFSampleGrabberSinkCallback2</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a> 介面。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream"><strong>IMFSampleOutputStream</strong></a><br/></td>
<td>將媒體範例寫入位元組資料流程。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection"><strong>IMFSampleProtection</strong></a><br/></td>
<td>為受保護媒體路徑內的媒體資料提供加密 (PMP) 。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob"><strong>IMFSaveJob</strong></a><br/></td>
<td>將媒體資料從來源位元組資料流程保存到應用程式提供的位元組資料流程。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler"><strong>IMFSchemeHandler</strong></a><br/></td>
<td>從 URL 建立媒體來源或位元組資料流程。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel"><strong>IMFSecureChannel</strong></a><br/></td>
<td>在兩個物件之間建立單向安全通道。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo"><strong>IMFSeekInfo</strong></a><br/></td>
<td>針對特定的搜尋位置，取得兩個最接近的主要畫面格。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport"><strong>IMFSensorActivitiesReport</strong></a><br/></td>
<td>提供 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a> 物件的存取權，這些物件描述感應器目前的活動。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback"><strong>IMFSensorActivitiesReportCallback</strong></a><br/></td>
<td>當有可用的感應器活動報告時，用戶端所執行的介面可接收回呼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor"><strong>IMFSensorActivityMonitor</strong></a><br/></td>
<td>提供控制感應器活動監視器的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a><br/></td>
<td>代表感應器的活動報告。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice"><strong>IMFSensorDevice</strong></a><br/></td>
<td>代表可以屬於感應器群組的感應器裝置，該群組是由 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a> 介面所代表。 &quot;此內容中的「裝置」 &quot; 一詞可以參考實體裝置、自訂媒體來源或框架提供者。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a><br/></td>
<td>代表可從中建立 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> 的感應器裝置群組。 &quot;此內容中的「裝置」 &quot; 一詞可以參考實體裝置、自訂媒體來源或框架提供者。 感應器群組實際上可能包含多個感應器裝置，或只能包含單一裝置，但仍會以感應器群組的形式運作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity"><strong>IMFSensorProcessActivity</strong></a><br/></td>
<td>表示與感應器相關聯之進程的活動。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection"><strong>IMFSensorProfileCollection</strong></a><br/></td>
<td>包含 media foundation 感應器設定檔物件的集合。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile"><strong>IMFSensorProfile</strong></a><br/></td>
<td>描述 media foundation 感應器設定檔。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream"><strong>IMFSensorStream</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory"><strong>IMFSensorTransformFactory</strong></a><br/></td>
<td>由感應器轉換所執行的介面，可讓媒體管線查詢感應器轉換的需求，以及建立感應器轉換的執行時間實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource"><strong>IMFSequencerSource</strong></a><br/></td>
<td>由 <a href="sequencer-source.md">Sequencer 來源</a>所執行。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory"><strong>IMFSharingEngineClassFactory</strong></a><br/></td>
<td>建立媒體共用引擎的實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown"><strong>IMFShutdown</strong></a><br/></td>
<td>由某些媒體基礎必須明確關閉的物件所公開。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary"><strong>IMFSignedLibrary</strong></a><br/></td>
<td>提供一種方法，可讓內容保護系統取得已簽署程式庫中函式的程式位址。 這個方法所提供的功能與 <strong>GetProcAddress</strong> 的功能相同，無法供 Windows Store 應用程式使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume"><strong>IMFSimpleAudioVolume</strong></a><br/></td>
<td>控制與串流音訊轉譯器相關聯之音訊會話的主要音量層級 (SAR) 和音訊捕獲來源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a><br/></td>
<td>由媒體基礎接收寫入器物件所執行。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a><br/></td>
<td>媒體基礎接收寫入器的回呼介面。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2"><strong>IMFSinkWriterCallback2</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a> 介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig"><strong>IMFSinkWriterEncoderConfig</strong></a><br/></td>
<td>提供接收寫入器上的其他功能，以動態方式變更媒體類型和編碼器設定。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex"><strong>IMFSinkWriterEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a> 介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a><br/></td>
<td>表示緩衝區，其中包含 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>的媒體資料。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a><br/></td>
<td>代表 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a> 物件的集合。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify"><strong>IMFSourceBufferNotify</strong></a><br/></td>
<td>提供可引發與 <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a>相關聯之事件的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor"><strong>IMFSourceOpenMonitor</strong></a><br/></td>
<td>回呼介面，可在非同步開啟作業的進度接收來自網路來源的通知。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a><br/></td>
<td>由媒體基礎的來源讀取器物件所執行。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a><br/></td>
<td>媒體基礎來源讀取器的回呼介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2"><strong>IMFSourceReaderCallback2</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a> 介面。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex"><strong>IMFSourceReaderEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a> 介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a><br/></td>
<td>從 URL 或位元組資料流程建立媒體來源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a><br/></td>
<td>表示含有相關聯位置和轉譯中繼資料的音訊資料區段。 空間音訊物件會儲存在 <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> 實例中，並允許在媒體基礎元件之間傳遞空間音訊資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a><br/></td>
<td>代表具有空間音效資訊的多媒體範例。 每個 <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> 都包含一或多個 <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager"><strong>IMFSSLCertificateManager</strong></a><br/></td>
<td>由用戶端所執行並由媒體基礎呼叫，以取得伺服器所要求的用戶端安全通訊端層 (SSL) 憑證。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor"><strong>IMFStreamDescriptor</strong></a><br/></td>
<td>取得媒體來源中某個資料流程的相關資訊。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig"><strong>IMFStreamingSinkConfig</strong></a><br/></td>
<td>將設定資訊傳遞給用於串流處理內容的媒體接收器。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink"><strong>IMFStreamSink</strong></a><br/></td>
<td>表示媒體接收物件上的資料流程。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsystemid"><strong>IMFSystemId</strong></a><br/></td>
<td>提供 retireves 系統識別碼資料的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate"><strong>IMFTimecodeTranslate</strong></a><br/></td>
<td>轉換運動圖片和電視工程師 (的) 時間碼和 100-納秒時間單位。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext"><strong>IMFTimedText</strong></a><br/></td>
<td>計時文字物件代表計時文字的元件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary"><strong>IMFTimedTextBinary</strong></a><br/></td>
<td>表示計時文字物件的資料內容。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue"><strong>IMFTimedTextCue</strong></a><br/></td>
<td>表示計時文字提示物件。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext"><strong>IMFTimedTextFormattedText</strong></a><br/></td>
<td>代表格式化計時文字的區塊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify"><strong>IMFTimedTextNotify</strong></a><br/></td>
<td>介面，定義媒體基礎計時文字通知的回呼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion"><strong>IMFTimedTextRegion</strong></a><br/></td>
<td>表示計時文字物件的顯示區域。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle"><strong>IMFTimedTextStyle</strong></a><br/></td>
<td>表示計時文字的樣式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack"><strong>IMFTimedTextTrack</strong></a><br/></td>
<td>表示計時文字的軌跡。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist"><strong>IMFTimedTextTrackList</strong></a><br/></td>
<td>表示計時文字播放軌的清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer"><strong>IMFTimer</strong></a><br/></td>
<td>提供在指定的時間叫用回呼的計時器。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader"><strong>IMFTopoLoader</strong></a><br/></td>
<td>將部分拓撲轉換成完整拓撲。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology"><strong>IMFTopology</strong></a><br/></td>
<td>表示拓撲。 <em>拓撲</em>描述以特定順序連接之媒體來源、接收和轉換的集合。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode"><strong>IMFTopologyNode</strong></a><br/></td>
<td>表示拓撲中的節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor"><strong>IMFTopologyNodeAttributeEditor</strong></a><br/></td>
<td>在媒體會話的目前拓撲中更新一或多個節點的屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup"><strong>IMFTopologyServiceLookup</strong></a><br/></td>
<td>讓自訂的視頻混音器或影片展示器，從 <a href="enhanced-video-renderer.md">增強型影片</a> 轉譯器 (EVR) 取得介面指標。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient"><strong>IMFTopologyServiceLookupClient</strong></a><br/></td>
<td>初始化視頻混音器或展示者。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample"><strong>IMFTrackedSample</strong></a><br/></td>
<td>追蹤影片媒體範例上的參考計數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile"><strong>IMFTranscodeProfile</strong></a><br/></td>
<td>由轉碼設定檔物件所執行。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider"><strong>IMFTranscodeSinkInfoProvider</strong></a><br/></td>
<td>由轉碼接收啟用物件所執行。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a><br/></td>
<td>由所有 <a href="media-foundation-transforms.md">媒體基礎轉換</a> 所執行 (MFTs) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput"><strong>IMFTrustedInput</strong></a><br/></td>
<td>由提供 (ITAs) 之輸入信任授權單位的元件所執行。 此介面是用來取得每個元件資料流程的 ITA。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput"><strong>IMFTrustedOutput</strong></a><br/></td>
<td>由提供 (OTAs) 之輸出信任授權單位的元件所執行。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid"><strong>IMFVideoDeviceID</strong></a><br/></td>
<td>傳回影片轉譯器元件所支援的裝置識別碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol"><strong>IMFVideoDisplayControl</strong></a><br/></td>
<td>控制 <a href="enhanced-video-renderer.md">增強型影片</a> 轉譯器 (EVR) 顯示影片的方式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype"><strong>IMFVideoMediaType</strong></a><br/></td>
<td>表示影片格式的描述。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap"><strong>IMFVideoMixerBitmap</strong></a><br/></td>
<td>Alpha-將靜態點陣圖影像與 <a href="enhanced-video-renderer.md">增強影片</a> 轉譯器所顯示的影片混合 (EVR) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol"><strong>IMFVideoMixerControl</strong></a><br/></td>
<td>控制 <a href="enhanced-video-renderer.md">增強型影片</a> 轉譯器 (EVR) 如何混合影片子串流。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2"><strong>IMFVideoMixerControl2</strong></a><br/></td>
<td>控制影片去交錯的喜好設定。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a><br/></td>
<td>將輸入影片串流上的位置對應到輸出影片資料流程上的對應位置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter"><strong>IMFVideoPresenter</strong></a><br/></td>
<td>代表影片演講者。 <em>影片展示者</em>是一種物件，可接收影片畫面（通常是從視頻混音器），並以某種方式呈現，通常是藉由將它們轉譯成顯示器。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor"><strong>IMFVideoProcessor</strong></a><br/></td>
<td>在 <a href="enhanced-video-renderer.md">增強型影片</a> 轉譯器中控制影片處理 (EVR) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol"><strong>IMFVideoProcessorControl</strong></a><br/></td>
<td>設定 <a href="video-processor-mft.md"><strong>視頻處理器 MFT</strong></a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2"><strong>IMFVideoProcessorControl2</strong></a><br/></td>
<td>設定 <a href="video-processor-mft.md"><strong>視頻處理器 MFT</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a><br/></td>
<td>設定 <a href="enhanced-video-renderer.md">增強型影片</a> 轉譯器 (EVR) 的新混音器或展示者。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator"><strong>IMFVideoSampleAllocator</strong></a><br/></td>
<td>配置影片媒體接收器的影片範例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a><br/></td>
<td>可讓應用程式追蹤增強型影片轉譯器所配置的影片樣本 (EVR) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex"><strong>IMFVideoSampleAllocatorEx</strong></a><br/></td>
<td>配置包含 Direct3D 11 紋理表面的影片範例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify"><strong>IMFVideoSampleAllocatorNotify</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a>介面的回呼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex"><strong>IMFVideoSampleAllocatorNotifyEx</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a>介面的回呼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a><br/></td>
<td>控制 <a href="media-session.md">媒體會話</a>所建立的工作佇列。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex"><strong>IMFWorkQueueServicesEx</strong></a><br/></td>
<td>擴充 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a> 介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol"><strong>IPlayToControl</strong></a><br/></td>
<td>啟用 <strong>PlayToConnection</strong> 物件以連接到媒體元件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrolwithcapabilities"><strong>IPlayToControlWithCapabilities</strong></a><br/></td>
<td>提供 <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSource</strong></a> 的功能來判斷內容的功能。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSourceClassFactory</strong></a><br/></td>
<td>建立 <a href="/uwp/api/Windows.Media.PlayTo.PlayToSource"><strong>PlayToSource</strong></a> 物件的實例。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket"><strong>IWMCodecLeakyBucket</strong></a><br/></td>
<td>&quot; &quot; 在影片編碼器上設定有漏洞 bucket 參數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp"><strong>IWMCodecOutputTimestamp</strong></a><br/></td>
<td>取得要解碼下一個影片畫面格的時間戳記。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata"><strong>IWMCodecPrivateData</strong></a><br/></td>
<td>取得必須附加至輸出媒體類型的私用編解碼器資料。 需要此編解碼器資料，才能正確地解碼 Windows Media 視訊內容。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops"><strong>IWMCodecProps</strong></a><br/></td>
<td>提供可取出格式特定編解碼器屬性的方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings"><strong>IWMCodecStrings</strong></a><br/></td>
<td>抓取編解碼器和格式的名稱和描述性字串。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops"><strong>IWMColorConvProps</strong></a><br/></td>
<td>設定色彩轉換器 DSP 上的屬性。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops"><strong>IWMResamplerProps</strong></a><br/></td>
<td>設定音訊 resampler DSP 上的屬性。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops"><strong>IWMResizerProps</strong></a><br/></td>
<td>在影片調整的 DSP 上設定屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport"><strong>IWMSampleExtensionSupport</strong></a><br/></td>
<td>設定範例延伸模組的編解碼器支援。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup"><strong>IWMVideoDecoderHurryup</strong></a><br/></td>
<td>控制影片解碼的速度。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer"><strong>IWMVideoDecoderReconBuffer</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
此介面已過時，不應該使用。
</blockquote>
<br/> 管理重建的影片畫面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe"><strong>IWMVideoForceKeyFrame</strong></a><br/></td>
<td>強制編碼器將目前的框架編碼為主要畫面格。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計參考](media-foundation-programming-reference.md)
</dt> </dl>

 

 
