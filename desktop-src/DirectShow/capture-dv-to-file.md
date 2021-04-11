---
description: 捕獲 DV 至檔案
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: 捕獲 DV 至檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317743"
---
# <a name="capture-dv-to-file"></a>捕獲 DV 至檔案

本節說明如何從 DV 攝影機或 VTR 磁帶捕捉數位視訊 (DV) 。

1.  建立 [MSDV 驅動程式](msdv-driver.md) 篩選器的實例。 如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。
2.  如 [關於 Capture graph](about-the-capture-graph-builder.md)產生器中所述，初始化 Capture graph builder。
3.  根據目的檔案類型建立 capture graph：
    -   [捕捉類型 1 DV 檔案](capture-a-type-1-dv-file.md)
    -   [捕捉類型 2 DV 檔案](capture-a-type-2-dv-file.md)
    -   [將 DV 捕獲到未壓縮的 RGB](capture-dv-to-uncompressed-rgb.md)
4.  執行圖形。

從 VTR 磁帶進行捕捉的運作方式，就像是從相機中捕捉即時影片，但您必須播放磁帶，如 [控制 DV](controlling-a-dv-camcorder.md)攝影機所述。 若要避免遺失任何框架，請先執行圖形，然後播放磁帶。 當您完成傳送時，請先停止磁帶，然後再停止圖形。

> [!Note]  
> 攝像機必須處於 VTR 模式。 請參閱 [裝置模式](device-mode.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[類型1與類型 2 DV AVI 檔案](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



