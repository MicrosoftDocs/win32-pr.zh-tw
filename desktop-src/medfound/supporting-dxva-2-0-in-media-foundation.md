---
description: 媒體基礎中支援 DXVA 2。0
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: 媒體基礎中支援 DXVA 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721927"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>媒體基礎中支援 DXVA 2。0

本主題說明如何在使用 Microsoft Direct3D 9 的媒體基礎轉換 (MFT) 中，支援 (DXVA) 2.0 的 DirectX 影片加速，它會描述解碼器和影片轉譯器（由拓撲載入器所 mediated）之間的通訊。 本主題不會說明如何執行 DXVA 解碼。

在本主題的其餘部分中，「 *解碼* 」一詞指的是可接收壓縮影片並輸出未壓縮影片的「解碼器 MFT」。 「 *解碼* 」一詞是指由圖形驅動程式所執行的硬體視頻加速器。

> [!TIP]
> 如需有關 Microsoft Direct3D 11 影片解碼的詳細資訊，請參閱 [支援媒體基礎中的 Direct3D 11 影片解碼](supporting-direct3d-11-video-decoding-in-media-foundation.md)。

 

> [!Note]  
> WindowsStore 應用程式必須使用 Direct3D 11。

 

以下是解碼器在媒體基礎中支援 DXVA 2.0 所必須執行的基本步驟：

1.  開啟 Direct3D 9 裝置的控制碼。
2.  尋找 DXVA 的解碼器設定。
3.  配置未壓縮的緩衝區。
4.  解碼框架。

本主題的其餘部分將更詳細地描述這些步驟。

## <a name="opening-a-direct3d-device-handle"></a>開啟 Direct3D 裝置控制碼

MFT 會使用 Microsoft Direct3D 裝置管理員來取得 Direct3D 9 裝置的控制碼。 若要開啟裝置控制碼，請執行下列步驟：

1.  使用值 **TRUE** 公開 [MF \_ SA \_ D3D \_ 感知](mf-sa-d3d-aware-attribute.md)屬性。 拓撲載入器會藉由呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)來查詢此屬性。 將此屬性設定為 **TRUE** 會通知拓撲載入器，此 MFT 支援 DXVA。
2.  當格式協調開始時，拓撲載入器會呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 與 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息。 *UlParam* 參數是影片轉譯器之 Direct3D 裝置管理員的 **IUnknown** 指標。 查詢此指標以取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面。
3.  呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) 來取得轉譯器之 Direct3D 裝置的控制碼。
4.  呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) ，並傳入裝置控制碼。 這個方法會傳回 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面的指標。
5.  快取指標和裝置控制碼。

## <a name="finding-a-decoder-configuration"></a>尋找解碼器設定

此 MFT 必須找到 DXVA 解碼器裝置的相容設定。 驗證輸入類型之後，請在 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法內執行下列步驟：

1.  呼叫 [**IDirectXVideoDecoderService：： GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids)。 這個方法會傳回一組解碼裝置 Guid。
2.  在解碼 Guid 陣列中迴圈，以找出該解碼器支援的專案。 例如，針對 MPEG-2 解碼器，您會尋找 **DXVA2 \_ ModeMPEG2 \_ MOCOMP**、 **DXVA2 \_ ModeMPEG2 \_ IDCT** 或 **DXVA2 \_ ModeMPEG2 \_ VLD**。

3.  當您找到候選的解碼器裝置 GUID 時，請將 GUID 傳遞給 [**IDirectXVideoDecoderService：： GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) 方法。 這個方法會傳回呈現目標格式的陣列，並指定為 **D3DFORMAT** 值。
4.  在轉譯目標格式中執行迴圈，並尋找此解碼器所支援的格式。
5.  呼叫 [**IDirectXVideoDecoderService：： GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations)。 傳入相同的解碼器裝置 GUID，以及描述所建議輸出格式的 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構。 方法會傳回 [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) 結構的陣列。 每個結構都描述一個可能的解碼器裝置設定。 尋找此解碼器支援的設定。
6.  儲存轉譯目標格式和設定。

在 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法中，根據建議的轉譯目標格式傳回未壓縮的影片格式。

在 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法中，針對呈現目標格式檢查媒體類型。

### <a name="fallback-to-software-decoding"></a>回到軟體解碼

如果 MFT 找不到 DXVA 設定 (例如，如果圖形驅動程式沒有正確的功能) ，則應該從 [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)和 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)方法傳回錯誤碼 **MF \_ \_ 不支援的 \_ D3D \_ 類型**。 拓撲載入器會藉由傳送 *ulParam* 參數的值 **為 Null** 的 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md)訊息來回應。 MFT 應釋放其指向 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。 拓撲載入器接著會重新協商媒體類型，而 MFT 可以使用軟體解碼。

## <a name="allocating-uncompressed-buffers"></a>配置未壓縮的緩衝區

在 DXVA 2.0 中，此解碼器負責配置 Direct3D 介面，以作為未壓縮的視訊緩衝區。 此解碼器應配置3個表面，讓 EVR 用於去交錯。 這個數位是固定的，因為媒體基礎不會提供方法讓 EVR 指定圖形驅動程式需要去交錯的表面數目。 有三個表面應該足以應付任何驅動程式。

在 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)方法中，設定 mft 輸出資料流程 [**\_ \_ \_ 資訊**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info)結構中的 **mft \_ 輸出 \_ 資料流程 \_ 提供 \_ 範例** 旗標。 此旗標會通知媒體會話，該 MFT 會配置自己的輸出範例。

若要建立介面，請呼叫 [**IDirectXVideoAccelerationService：： CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface)。  ([**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面會從 [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)繼承這個方法。 ) 您可以在 [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)中找到轉譯目標格式之後，進行這項作業。

針對每個介面，呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 來建立媒體範例以保存表面。 方法會傳回 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的指標。

## <a name="decoding"></a>解碼

若要建立解碼器裝置，請呼叫 [**IDirectXVideoDecoderService：： CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)。 方法會傳回解碼裝置之 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 介面的指標。

解碼應該在 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法內進行。 在每個畫面上，呼叫 [**IDirect3DDeviceManager9：： TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) 來測試裝置控制碼。 如果裝置已變更，此方法會傳回 **DXVA2 \_ E \_ NEW \_ VIDEO \_ 裝置**。 如果發生這種情況，請執行下列動作：

1.  藉由呼叫 [**IDirect3DDeviceManager9：： CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle)來關閉裝置控制碼。
2.  釋放 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 和 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 指標。
3.  開啟新的裝置控制碼。
4.  依照本頁面先前的「尋找解碼器設定」所述，協商新的解碼器設定。
5.  建立新的解碼器裝置。

假設裝置控制碼有效，則解碼程式的運作方式如下：

1.  取得目前未使用的可用介面。  (一開始都有所有表面可用。 ) 
2.  查詢媒體範例以取得 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面。
3.  呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) ，並提供指向 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標，該介面是由解碼器所執行。 當影片轉譯器釋放範例時，將會叫用解碼器的回呼。
4.  呼叫 [**IDirectXVideoDecoder：： BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)。
5.  執行下列一或多次：
    1.  呼叫 [**IDirectXVideoDecoder：： GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) 來取得 DXVA 的解碼器緩衝區。
    2.  填滿緩衝區。
    3.  呼叫 [**IDirectXVideoDecoder：： ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)。
    4.  呼叫 [**IDirectXVideoDecoder：： Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) 以執行框架上的解碼作業。

DXVA 2.0 使用與 DXVA 1.0 相同的資料結構來進行解碼作業。 針對 DXVA 設定檔的原創組 (261、.H 和 MPEG-2) ，這些資料結構會在 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中說明。

在每對 [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**執行**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)呼叫中，您可以多次呼叫 [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) ，但每種類型的 DXVA 緩衝區都只會呼叫一次。 如果您使用相同的緩衝區類型呼叫它兩次，則會覆寫資料。

使用 [**SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) 方法中的回呼 (步驟 3) 來追蹤目前可用且正在使用中的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 
