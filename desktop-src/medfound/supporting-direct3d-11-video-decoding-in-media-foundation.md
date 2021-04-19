---
description: 本主題說明如何在 Microsoft 媒體基礎的解碼器中支援 Microsoft Direct3D 11。
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: 支援媒體基礎中的 Direct3D 11 影片解碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542f7244922dc7947f22e4d33027fdcac1962fe5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991397"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>支援媒體基礎中的 Direct3D 11 影片解碼

本主題說明如何在 Microsoft 媒體基礎的解碼器中支援 Microsoft Direct3D 11。 具體而言，它會描述解碼器與影片轉譯器之間的通訊。 本主題不會說明如何執行解碼作業。

-   [概觀](#overview)
-   [開啟裝置控制碼](#open-a-device-handle)
-   [尋找解碼器設定](#find-a-decoder-configuration)
-   [回到軟體解碼](#fallback-to-software-decoding)
-   [配置未壓縮的緩衝區](#allocating-uncompressed-buffers)
-   [解碼](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

本主題的其餘部分會使用下列詞彙：

-   **軟體解碼器**。 軟體解碼器是媒體基礎轉換 (MFT) ，可接收壓縮的影片範例並輸出未壓縮的影片畫面。
-   **解碼裝置**。 解碼器裝置是影片加速器，由圖形驅動程式所執行。 解碼器裝置會執行加速解碼作業。
-   **管線**。 管線裝載軟體的解碼器，並在軟體解碼器之間傳遞緩衝區。 視應用程式而定，管線可能是直接呼叫 MFT 的 [媒體會話](media-session.md)、 [來源讀取](source-reader.md)程式或應用程式程式碼。

若要使用 Direct3D 11 執行解碼，軟體解碼器必須有 Direct3D 11 裝置的指標。 Direct3D 11 裝置會從外部建立到軟體解碼器。 在 [媒體會話](media-session.md) 案例中，影片轉譯器會建立 Direct3D 11 裝置。 在 [來源讀取器](source-reader.md) 案例中，應用程式通常會建立 Direct3D 11 裝置。

DXGI 裝置管理員是用來在元件之間共用 Direct3D 11。 DXGI 裝置管理員會公開 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面。 管線會藉由傳送 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md)訊息，在軟體解碼器上設定 **IMFDXGIDeviceManager** 指標。

下圖顯示軟體解碼器、Direct3D 11 和管線之間的關聯性。

![顯示軟體解碼器和 [dxgi 裝置管理員] 的圖表。](images/d3d11video01.png)

以下是軟體解碼器在媒體基礎中支援 Direct3D 11 所必須執行的基本步驟：

1.  開啟 Direct3D 11 裝置的控制碼。
2.  尋找解碼器設定。
3.  配置未壓縮的緩衝區。
4.  解碼框架。

本主題的其餘部分將更詳細地描述這些步驟。

## <a name="open-a-device-handle"></a>開啟裝置控制碼

解碼器 MFT 使用 DXGI 裝置管理員來取得 Direct3D 11 裝置的控制碼。 若要開啟裝置控制碼，請執行下列步驟：

1.  解碼器 MFT 必須公開具有值 **TRUE** 的 [MF \_ SA \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)屬性。
2.  拓撲載入器會藉由呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)來查詢此屬性。 值 **TRUE** 表示 MFT 支援 Direct3D 11。
3.  拓撲載入器會呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 與 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息。 *UlParam* 參數是 DXGI 裝置管理員的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。 查詢此指標以取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面。
4.  呼叫 [**IMFDXGIDeviceManager：： OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) 來取得 Direct3D 11 裝置的控制碼。
5.  若要取得 Direct3D 11 裝置的指標，請呼叫 [**IMFDXGIDeviceManager：： GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice)。 傳入裝置控制碼和值 **IID \_ ID3D11Device**。 方法會傳回 [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) 介面的指標。
6.  若要取得影片加速器的指標，請再次呼叫 [**IMFDXGIDeviceManager：： GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) 。 這次，傳入裝置控制碼和值 **IID \_ ID3D11VideoDevice**。 方法會傳回 [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) 介面的指標。
7.  呼叫 [**ID3D11Device：： GetImmediateCoNtext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) 來取得 [**>id3d11devicecoNtext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) 指標。
8.  呼叫 [**>id3d11devicecoNtext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext)上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得 [**ID3D11VideoCoNtext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)指標。
9.  建議您在裝置內容上使用多執行緒保護，以防止有時候當您呼叫 [**ID3D11VideoCoNtext：： GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) 或 [**ID3D11VideoCoNtext：： ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)時可能會發生的鎖死問題。 若要設定多執行緒保護，請先呼叫 [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得 [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread)指標。 然後呼叫 [**ID3D10Multithread：： SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected)，將 *bMTProtect* 傳遞 **為 true** 。

## <a name="find-a-decoder-configuration"></a>尋找解碼器設定

若要執行解碼，軟體解碼器必須找到解碼器裝置所支援的相容設定，包括轉譯目標格式。 此步驟會在 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法內發生，如下所示。

1.  驗證輸入媒體類型。 如果類型遭到拒絕，請略過其餘步驟，並傳回錯誤碼。
2.  呼叫 [**ID3D11VideoDevice：： GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) 以取得支援的設定檔數目。
3.  呼叫 [**ID3D11VideoDevice：： GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) 來列舉設定檔，並取得設定檔 guid。
4.  尋找符合影片格式和軟體解碼器功能的設定檔 GUID。 例如，MPEG-2 解碼器會尋找 **D3D11 \_ 解碼器 \_ 設定檔的 \_ mpeg2 \_ MOCOMP**、**D3D11 的 \_ 解碼器 \_ 設定檔 \_ mpeg2 \_ IDCT**，以及 **D3D11 \_ 解碼器 \_ 設定檔 \_ mpeg2 \_ VLD**。
5.  如果找到適當的解碼器 GUID，請藉由呼叫 [**ID3D11VideoDevice：： CheckVideoDecoderFormat**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) 方法來檢查輸出格式。 傳入用來指定轉譯目標格式的解碼器 GUID 和 **DXGI \_ 格式** 值。
6.  接下來，尋找適當的解碼器設定。
    1.  呼叫 [**ID3D11VideoDevice：： GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) 來取得解碼器設定的數目。 傳入相同的解碼器裝置 GUID，以及描述建議轉譯目標格式的 [**D3D11 \_ VIDEO \_ 解碼器 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) 結構。
    2.  呼叫 [**ID3D11VideoDevice：： GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) 來列舉解碼器設定。

在 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法中，根據建議的呈現目標格式傳回未壓縮的影片格式。

在 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法中，針對呈現目標格式檢查媒體類型。

## <a name="fallback-to-software-decoding"></a>回到軟體解碼

MFT 可能找不到設定。 例如，圖形驅動程式可能不支援正確的功能。 在此情況下，MFT 必須切換回軟體解碼，如下所示。

1.  [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)和 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)方法都應傳回 **MF \_ E \_ 不支援的 \_ D3D \_ 類型**。
2.  為了回應，拓撲載入器會將 *ulParam* 參數的值 **為 Null** 的 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md)訊息傳送給。
3.  MFT 會釋放其指向 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。
4.  拓撲載入器會重新協商媒體類型。

此時，MFT 可以使用軟體解碼。

## <a name="allocating-uncompressed-buffers"></a>配置未壓縮的緩衝區

此解碼器負責配置 Direct3D 11 紋理以作為未壓縮的視訊緩衝區。 輸出資料流程屬性中的 [MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數](mf-sa-minimum-output-sample-count.md) 屬性 (請參閱 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) 用來判斷應針對影片轉譯器配置多少個要用於去交錯的介面。 如果有一些合理的上限和下限，則應該使用此值來將它界限，例如3-32。 如需漸進內容，請參閱 [MF \_ SA \_ 最小 \_ 輸出 \_ 取樣 \_ 計數 \_ 漸進式](mf-sa-minimum-output-sample-count-progressive.md)。

在 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)方法中，設定 mft 輸出資料流程 [**\_ \_ \_ 資訊**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)結構中的 **mft \_ 輸出 \_ 資料流程 \_ 提供 \_ 範例** 旗標。 此旗標會通知媒體會話，該 MFT 會配置自己的輸出範例。 為了配置輸出範例，MFT 會執行下列步驟：

1.  藉由呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)來建立2d 材質陣列。 在 [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) 結構中，將 **ArraySize** 設定為等於該解碼器所需的表面數目。 這包括：
    -   參考框架的表面。
    -   去交錯 (三個表面) 的表面。
    -   此為緩衝處理所需的表面。

    系結旗標 (**BindFlags**) 應該包含 **D3D11 系結 \_ \_ 解碼器** 旗標，以及在輸出資料流程屬性中透過 [MF \_ SA \_ D3D11 \_ BindFlags](mf-sa-d3d11-bindflags.md) 屬性設定的任何系結旗標。
2.  針對材質陣列中的每個介面，呼叫 [**ID3D11VideoDevice：： CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) 來建立影片解碼輸出視圖。 在解碼期間，這些輸出視圖會傳遞至 [**ID3D11VideoCoNtext：:D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) 方法。
3.  針對材質陣列中的每個介面，建立媒體範例，如下所示：
    1.  藉由呼叫 [**MFCreateDXGISurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) 函數來建立 DXGI 媒體緩衝區。 傳入 [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) 指標和紋理陣列中每個元素的位移。 函數會傳回 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 指標。
    2.  藉由呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 函數來建立空白媒體範例。 將 *pUnkSurface* 參數設定為等於 **Null**。 函數會傳回 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標。
    3.  呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) ，將媒體緩衝區新增至範例。

您應該同時終結您建立的所有紋理，而不只終結部分，並繼續使用提醒。

## <a name="decoding"></a>解碼

若要建立解碼器裝置，請呼叫 [**ID3D11VideoDevice：： CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder)。 方法會傳回 [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) 介面的指標。 解碼應該在 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法內進行。 在每個畫面上，呼叫 [**IMFDXGIDeviceManager：： TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) 來測試 DXGI 的可用性。 如果裝置已變更，軟體解碼器必須重新建立解碼器裝置，如下所示：

1.  藉由呼叫 [**IMFDXGIDeviceManager：： CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle)來關閉裝置控制碼。
2.  釋放與先前 Direct3D 11 裝置相關聯的所有資源，包括 [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)、 [**ID3D11VideoCoNtext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)、 [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)和 [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) 介面。
3.  開啟新的裝置控制碼。
4.  如先前在 [尋找解碼器](#find-a-decoder-configuration)設定中所述，協商新的解碼器設定。 這是必要步驟，因為裝置功能可能已變更。
5.  建立新的解碼器裝置。

假設裝置控制碼有效，則解碼程式的運作方式如下：

1.  取得目前未使用的可用介面。 一開始，所有表面都可以使用。
2.  查詢媒體範例以取得 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面。
3.  呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) ，並提供 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。  (軟體解碼器必須執行此介面 ) 。當影片轉譯器釋放範例時，將會叫用回呼。 使用此回呼來追蹤哪些範例目前可用且正在使用中。
4.  呼叫 [**ID3D11VideoCoNtext：:D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)。 傳遞 [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) 介面的指標給解碼器裝置和輸出視圖的 [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) 介面。
5.  執行下列一或多次：
    1.  呼叫 [**ID3D11VideoCoNtext：： GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) 以取得緩衝區。
    2.  填滿緩衝區。
    3.  呼叫 [**ID3D11VideoCoNtext：： ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)。
    4.  呼叫 [**ID3D11VideoCoNtext：： SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)。 此方法會指示解碼器裝置在框架上執行解碼作業。
6.  呼叫 [**ID3D11VideoCoNtext：:D ecoderendframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) ，以信號表示目前框架的解碼結尾。

Direct3D 11 使用與 DXVA 2.0 相同的資料結構來進行解碼作業。 針對 DXVA 設定檔的原創組 (261、.H 和 MPEG-2) ，這些資料結構會在 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中說明。

在每一對 [**DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) 和 [**SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) 呼叫中，您可以呼叫 [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) 多次，但只針對每個緩衝區類型呼叫一次。 如果您使用相同的緩衝區類型兩次而不呼叫 **SubmitDecoderBuffer**，則會覆寫緩衝區中的資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 影片 Api](direct3d-11-video-apis.md)
</dt> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
