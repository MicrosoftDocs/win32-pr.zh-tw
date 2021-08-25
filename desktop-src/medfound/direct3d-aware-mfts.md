---
description: 本主題說明如何針對影片執行 Direct3D 感知媒體基礎轉換 (MFT) 。
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958733"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

本主題說明如何針對影片執行 *Direct3D 感知* 媒體基礎轉換 (MFT) 。

如果影片 MFT 可以處理包含 Direct3D 表面的範例，則會將其視為 *direct3d 感知* 。 在影片 MFT 中支援 Direct3D 的一般原因是，使用 DirectX Video 加速 (DXVA) 來啟用硬體加速解碼。

本主題說明讓您的 MFT Direct3D 感知所需的步驟。 本主題並未涵蓋 DXVA 解碼的機制。 如需 DXVA 的相關資訊，請參閱 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md)。

> [!IMPORTANT]
> 從 Windows 8 開始，可以使用 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ，而不是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)。 針對 Windows Store 應用程式，您必須使用 **IMFDXGIDeviceManager** 和 Microsoft Direct3D 11。 如需詳細資訊，請參閱 [Direct3D 11 影片 api](direct3d-11-video-apis.md)。

 

1.  執行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。 這個方法會傳回屬性存放區的指標。
2.  在自己的屬性存放區上，此 MFT 必須將 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md) 屬性的值設定為 **TRUE** 。 從 Windows 8 開始，如果使用 Direct3D 11，請使用[MF \_ SA \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)。
3.  在格式的協商期間， [**如果 \_ MF \_ sa \_ D3D 感知**](mf-sa-d3d-aware-attribute.md) (或 [mf \_ sa \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md) 使用 Direct3D 11) 屬性是否為 **TRUE**，用戶端可能會將 [**mft \_ 訊息集的 \_ \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。 *UlParam* 事件參數是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)介面的指標。 從 Windows 8 開始，您可以使用 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ，而不是 **IDirect3DDeviceManager9**。 用戶端不需要傳送此訊息。
4.  MFT 會呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) 來查詢所需的 DXVA 服務。 從 Windows 8 開始，如果使用 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ，則 MFT 會呼叫 [**IMFDXGIDeviceManager：： GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice)。 通常，解碼器會查詢 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)，而視頻處理器會查詢 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)。
5.  假設上一個步驟成功， [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 和 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法必須傳回 DXVA 相容的格式。
6.  用戶端會設定 MFT 上的媒體類型。 如果媒體類型與 DXVA 不相容，則此 MFT 必須傳回錯誤碼 **MF \_ \_ 不支援的 \_ D3D \_ 類型**。
7.  此時有兩個選項，取決於用戶端是否找到適當的 DXVA 格式。
    -   如果用戶端成功設定 DXVA 格式，它可能會開始處理。 此時，MFT 可以使用 DXVA 進行處理，或切換回軟體處理。
    -   或者，如果用戶端找不到可接受的 DXVA 格式，用戶端可能會傳送另一個 [**MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息，這次將 *ulParam* 設定為 **Null**。 如果使用了 **IMFDXGIDeviceManager**) 和任何其他 DXVA 介面，然後還原為軟體處理，則此 MFT 必須釋放 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)指標 ([**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)指標。 此時，MFT 不能使用 DXVA 處理。

您必須準備好 Direct3D 感知的 MFT，才能處理包含 Direct3D 介面的範例。 此範例只會包含一個媒體緩衝區。 若要從緩衝區取得 Direct3D 介面，請呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函數，並指定 **MR \_ 緩衝區 \_ 服務** 服務。 如需詳細資訊，請參閱 [DirectX 介面緩衝區](directx-surface-buffer.md)。

使用 DXVA 的 MFT 必須配置自己的輸出範例，如下所示：

1.  在 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) 方法中，設定 **MFT \_ 輸出 \_ 資料流程 \_ 提供 \_ 範例** 旗標。
2.  建立 DXVA 表面的集區，如 DXVA 規格中所述。
3.  藉由呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)來建立媒體範例。

由於 DXVA 處理可能無法使用，因此 MFT 一律支援軟體處理，因為有數個原因：

-   GPU 可能不支援 DXVA。
-   用戶端可能不會使用 Direct3D。
-   未針對每個影片格式定義 DXVA 設定檔。

Direct3D 感知的 MFT 必須有單一輸出資料流程。 它不能有多個輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



