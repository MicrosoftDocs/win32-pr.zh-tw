---
description: 來源讀取器屬性
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: 來源讀取器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238326"
---
# <a name="source-reader-attributes"></a>來源讀取器屬性

您可以使用下列屬性來初始化 [來源讀取器](source-reader.md)。



| 屬性                                                                                                            | 描述                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 低 \_ 延遲](mf-low-latency.md)                                                                               | 啟用低延遲處理。                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ 停用 \_ 轉換器](mf-readwrite-disable-converters.md)                                            | 啟用或停用來源讀取器的格式轉換。                                                                                                                                                                       |
| [MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換](mf-readwrite-enable-hardware-transforms.md)                           | 可讓來源讀取器使用以硬體為基礎的媒體基礎轉換 (MFTs) 。                                                                                                                                                |
| [MF \_ 來源 \_ 讀取器 \_ 非同步 \_ 回呼](mf-source-reader-async-callback.md)                                           | 包含應用程式的來源讀取器回呼介面指標。                                                                                                                                                  |
| [MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md)                                                 | 包含指向 Microsoft [Direct3D 裝置管理員](direct3d-device-manager.md)的指標。                                                                                                                                        |
| [MF \_ 來源 \_ 讀取器 \_ 停用 \_ DXVA](mf-source-reader-disable-dxva.md)                                               | 指定來源讀取器是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。                                                                                                                                |
| [MF \_ 來源 \_ 讀取 \_ 器 \_ \_ 在關機時中斷 MEDIASOURCE \_ 連線](mf-source-reader-disconnect-mediasource-on-shutdown.md) | 指定來源讀取器是否關閉媒體來源。<br/> 只有當應用程式從現有的媒體來源物件建立來源讀取器時，才適用。<br/>                                           |
| [MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 先進的 \_ 影片 \_ 處理](mf-source-reader-enable-advanced-video-processing.md)     | 啟用 [來源讀取器](source-reader.md)的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。                                                           |
| [MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理](mf-source-reader-enable-video-processing.md)                        | 可讓來源讀取器進行有限的影片處理。                                                                                                                                                                             |
| [MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ CONFIG](mf-source-reader-mediasource-config.md)                                   | 包含媒體來源的設定屬性。                                                                                                                                                                            |
| [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)                                            | 包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。 如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。 |



 

使用這些屬性搭配下列方法和函數：

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

若要使用這些屬性的任何一項，請先呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。 然後使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，在屬性存放區上設定所需的屬性。 將 **IMFAttributes** 指標傳遞至先前所列之任何方法或函數的 *pAttributes* 參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




