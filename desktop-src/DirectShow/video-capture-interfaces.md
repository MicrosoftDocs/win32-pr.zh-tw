---
description: 影片捕獲介面
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: 影片捕獲介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974348"
---
# <a name="video-capture-interfaces"></a>影片捕獲介面

這些介面支援影片捕捉、使用 Microsoft® Windows®驅動程式模型 (WDM) 裝置或適用于 Windows®® VFW (裝置的舊版 Microsoft) 影片。



| 介面                                                        | 描述                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | 控制 WDM 視頻捕捉卡上的影片數位化。                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | 控制 pin 如何分配緩衝區。                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | 用來接收檔案複製作業進度的回呼介面。                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | 在 WDM 音訊或影片來源和 WDM 捕獲裝置之間建立硬體連接。                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | 查詢有關捕獲效能的捕獲篩選。                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | 控制個別資料流程的開始和停止時間。                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | 查詢並設定捕獲篩選器的輸出格式。                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | 顯示 VFW capture 驅動程式所提供的對話方塊。                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | 從捕獲裝置控制圖片。                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | 調整視訊訊號的品質，例如亮度、對比、色調、飽和度、gamma 和清晰度。 |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | 影片捕獲的組建篩選圖形。                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | 指定輸出檔的名稱和屬性。                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外部裝置控制介面](external-device-control-interfaces.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



