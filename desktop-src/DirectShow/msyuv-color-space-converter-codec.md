---
description: MSYUV 是 YUV 至 RGB 的色彩空間轉換器編解碼器。
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV 色彩空間轉換器編解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001935"
---
# <a name="msyuv-color-space-converter-codec"></a>MSYUV 色彩空間轉換器編解碼器

MSYUV 是 YUV 至 RGB 的色彩空間轉換器編解碼器。 它可在用戶端上以 YUV 格式播放影片來源資料，而這些用戶端的視頻顯示器介面卡無法用於硬體中的 YUV 至 RGB 轉換。 編解碼器會透過 [AVI 解壓縮](avi-decompressor-filter.md) 套裝程式裝函式篩選來參與篩選圖形。

具有1394或 USB 介面的數位會議攝影機，可以產生各種形式的影像資料。 如果顯示器硬體不支援面板上的 YUV 到 RGB 轉換，或者硬體轉換功能無法用於某些其他原因，則必須先將 YUV 影像資料轉換成 RGB 格式，然後再傳送到影片轉譯器。

由於 [影片](video-renderer-filter.md)轉譯器在連接時需要 RGB 輸入類型，因此在自動建立圖表時，此篩選器可能會從影片轉譯器插入圖形上游。 具體而言，如果圖形產生器在上游篩選器輸出釘選的媒體類型中偵測到 YUV 格式，則圖形產生器會插入 AVI 解壓縮程式，然後載入 MSYUV 編解碼器，並一開始就設定它以執行轉換成 RGB。 在圖形首次轉換成執行中或已暫停狀態之後，影片轉譯器篩選器可以偵測視頻顯示器介面卡是否可以在硬體中執行轉換。 如果可以，則會通知 AVI 解壓縮程式，並將 MSYUV 重新配置為以「傳遞模式」操作，這會造成編解碼器略過轉換，並將 YUV 影像資料直接複製到視訊記憶體中的 DirectDraw 重迭表面。

由於影片混合轉譯器 (VMR-7 和 VMR-9) 絕不會使用 GDI，因此在連接時不需要 RGB 類型，而且 MSYUV 色彩空間轉換器永遠不會在圖形中的 VMR 之前插入。

MSYUV 會將封裝的 YUV 格式轉換為 RGB，如下列清單所示：

-   輸入格式： UYVY、YUY2、YVYU
-   輸出格式： RGB 8、RGB 16、RGB 24、RGB 32

MSYUV 色彩空間轉換器編解碼器是視訊壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器。 它會透過 [AVI 解壓縮](avi-decompressor-filter.md) 程式篩選器用於 DirectShow 中。 若為更一般用途的色彩轉換器，請使用 [**色彩轉換器 DSP**](../medfound/colorconverter.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 
