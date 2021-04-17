---
description: 啟用來源讀取器的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: 'MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511325"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>MF \_ 來源 \_ 讀取器 \_ 啟用 \_ ADVANCED \_ VIDEO \_ 處理屬性

啟用 [來源讀取器](source-reader.md)的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則來源讀取器可以將視頻處理器插入處理管線中，以啟用下列格式轉換類型：

-   色彩空間轉換 (YUV 到 RGB-32) 
-   去交錯
-   影片調整大小
-   畫面播放速率轉換

如果此屬性為 **TRUE**，則 [ [MF \_ READWRITE 停用 \_ \_ 轉換器](mf-readwrite-disable-converters.md) ] 屬性必須為 **FALSE**。

來源讀取器會尋找在 [ **MFT \_ 類別] \_ 視頻 \_ 處理器** 類別中註冊的視頻處理器，包括針對本機進程註冊的 MFTs。 如需有關 MFTs 本機註冊的詳細資訊， (參閱 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ) 。如果找不到其他適合的視頻處理器，來源讀取器會使用轉碼視頻處理器 (XVP) 。

應用程式會藉由呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)來指定所需的輸出類型。 當來源讀取器設定視頻處理器時，它會嘗試符合輸出類型的下列屬性：

-   畫面播放速率 ([MF \_ MT \_ 幀 \_ 速率](mf-mt-frame-rate-attribute.md)) 
-   框架大小 ([MF \_ MT \_ 框架 \_ 大小](mf-mt-frame-size-attribute.md)) 
-   交錯模式 ([MF \_ MT \_ 交錯 \_ 模式](mf-mt-interlace-mode-attribute.md)) 
-   圖元外觀比例 ([MF \_ MT \_ 圖元 \_ 外觀 \_ 比例](mf-mt-pixel-aspect-ratio-attribute.md)) 
-   類型 ([MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)) 

此屬性類似于 [MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理](mf-source-reader-enable-video-processing.md) 屬性，但提供下列優點：

-   支援更廣泛的格式轉換。
-   應用程式可以註冊自己的轉換器。
-   某些轉換可在使用 GPU 的硬體上執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




