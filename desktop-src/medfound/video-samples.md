---
description: 影片範例
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: 影片範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848694"
---
# <a name="video-samples"></a>影片範例

影片範例物件是 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的特製化，可搭配 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 使用。 若要建立這個物件的實例，請呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 函數。 函式會接受 Direct3D 介面的指標，並傳回 **IMFSample** 介面的指標。 下列類型的物件應使用此函數來配置範例：

-   自訂 EVR 展示者。 展示者會配置影片範例，並將其傳送至混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法。 如需詳細資訊，請參閱 [如何撰寫 EVR 的簡報者](how-to-write-an-evr-presenter.md)。

-   支援影片加速的影片解碼器。 如需詳細資訊，請參閱 [媒體基礎中的支援 DXVA 2.0](supporting-dxva-2-0-in-media-foundation.md)。

影片範例物件會執行下列介面：

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

如果 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)的 *pUnkSurface* 參數不是 **Null**，則產生的視頻範例會包含封裝 Direct3D 介面的單一媒體緩衝區。 這個緩衝區物件的功能有限：

-   緩衝區的 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 方法會傳回 E \_ >notimpl。

-   緩衝區不會執行 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。

從緩衝區存取介面的唯一方法是使用服務識別碼 MR 緩衝區服務來呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) \_ \_ 。

如果 *pUnkSurface* 參數為 **Null**，則會以零個媒體緩衝區來建立影片範例。 若要在範例中新增緩衝區，請執行下列動作：

1.  建立 Direct3D 介面。

2.  藉由呼叫 [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer)來建立介面緩衝區。 如需詳細資訊，請參閱 [DirectX 介面緩衝區](directx-surface-buffer.md)。

3.  藉由呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)，將緩衝區新增至範例。

如果您需要可透過 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面存取 surface 記憶體，請使用此方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體緩衝區](media-buffers.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 
