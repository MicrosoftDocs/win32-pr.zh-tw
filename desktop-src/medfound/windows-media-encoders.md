---
description: 編碼器會使用應用程式所指定的格式，將未壓縮的音訊或影片轉換成壓縮的封包。 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows 媒體音訊和影片編解碼器。
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows媒體編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d79ff55e98227c63e9761a8dec5ae068c8b1786c067230548ad0028dbe301a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237287"
---
# <a name="windows-media-encoders"></a>Windows媒體編碼器

編碼器會使用應用程式所指定的格式，將未壓縮的音訊或影片轉換成壓縮的封包。 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows 媒體音訊和影片編解碼器。

編碼器是由代表類別：音訊或影片的 GUID 所識別。 編碼器的輸出類型是以媒體類型的主要和子類型 GUID 表示。

-   Windows媒體音訊編解碼器

    類別： **MFT \_ 類別 \_ 音訊 \_ 編碼器**

    主要類型： MFMediaType \_ 音訊

    子類型： MFAudioFormat \_ WMAudioV9、MFAudioFormat \_ WMAudioV8、MFAudioFormat \_ WMAudio \_ 無損、MFAudioFormat \_ WMASPDIF

-   Windows媒體視頻編碼器

    類別： **MFT \_ 類別 \_ 影片 \_ 編碼器**

    主要類型： MFMediaType \_ 影片

    子類型： MFVideoFormat \_ WVC1、MFVideoFormat \_ WMV3、MFVideoFormat \_ WMV2、MFVideoFormat \_ WMV1

這些編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，媒體基礎可透過編碼器的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面來提供應用程式的存取權。 如果您使用管線層元件進行 ASF 編碼，則編碼器 MFT 會以轉換節點的形式插入管線中，因為它負責將流經來源的媒體資料轉換為接收。 如果來源是壓縮型別，則管線會新增必要的解碼器，以將來源轉換成未壓縮的型別。 編碼器有一個輸入資料流程和一個輸出資料流程。 編碼器會根據應用程式在編碼會話之前所設定的設定和格式，接收輸入資料並產生編碼的資料。 輸出資料流程的格式是由媒體類型所描述。

此章節包含下列主題。



| 主題                                                                              | 描述                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [具現化編碼器 MFT](instantiating-the-encoder-mft.md)                  | 說明如何建立編碼器。                                                         |
| [編碼屬性](configuring-the-encoder.md)                                 | 說明如何藉由在編碼器 MFT 上設定適當的屬性來設定編碼器。 |
| [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md) | 說明如何設定編碼器上的輸入和輸出媒體類型。                            |
| [設定 WMV 編碼器](configuring-a-wmv-encoder.md)                         | 說明如何設定 Windows Media 視訊 (WMV) 編碼器。                              |
| [設定 WMA 編碼器的輸出類型](configuring-a-wma-encoder.md)          | 說明如何設定 Windows Media 音訊 (WMA) 編碼器的輸出類型。                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



