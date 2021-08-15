---
description: 將會根據下列資訊分類 YUV 格式：
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: 'YUV 影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31afa11c855b865c7e524d393d1f86ae836e00119a3171b35a3c0c2549d184b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632688"
---
# <a name="yuv-video-subtypes"></a>YUV 影片子類型

將會根據下列資訊分類 YUV 格式：

**壓縮格式與平面格式。** 在封裝格式中，Y、U 和 V 元件會儲存在單一陣列中。 圖元會組織成 macropixels 的群組，其版面配置取決於格式。 在平面格式中，Y、U 和 V 元件會分別儲存為三個平面。

**色度取樣。** 名為 A:B： C 標記法的標記法可用來描述相對於 Y 取樣的頻率和 V 取樣頻率：

-   4:4:4 表示不含色度通道的縮減。
-   4:2:2 表示2:1 水準縮小，不含垂直的縮減取樣。 每個掃描行都包含每兩個 U 或 V 範例的四個 Y 樣本。
-   4:2:0 表示2:1 水準縮小取樣，具有2:1 垂直縮減取樣。
-   4:1:1 表示4:1 水準縮小，不含垂直的縮減取樣。 每個掃描行都包含每個 U 或 V 範例的四個 Y 樣本。 4:1:1 取樣與其他格式較不常見，在本文中不會詳細討論。

**每個通道的位數。** 最常見的範例大小為每個樣本8、10或16位。 某些 YUV 格式為調色盤。

**記憶體配置。** 另外兩個 YUV 格式類型可以是相同的，但在記憶體中的 Y、V 和 U 範例使用不同的排序。

**建議的 YUV 格式**



| GUID               | 格式 | 取樣 | 已封裝或平面 | 每個通道的位數 |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | 包裝           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | 包裝           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | 包裝           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | 平面           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | 平面           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | 平面           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | 平面           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | 平面           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | 平面           | 8                |



 

如需 Windows 上的影片轉譯格式的說明，請參閱[適用于影片轉譯的建議8位 yuv 格式](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)。

**其他 YUV 格式類型**



| GUID               | 格式                                                | 取樣                                                | 已封裝或平面                                  | 每個通道的位數                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | 平面                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | 不再支援。<br/> Indeo YVU9<br/> | 不再支援。<br/> 請參閱＜備註＞。<br/> | 不再支援。<br/> 平面<br/> | 不再支援。<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | 平面                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | 請參閱＜備註＞。                                            | 包裝                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | 包裝                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | 包裝                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | 請參閱＜備註＞。                                            | 平面                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | 包裝                                            | 8                                            |



 

-   I420 由 Y 平面組成，後面接著 U 平面，後面接著 V 平面。
-   IYUV 與 I420 相同。
-   Y211 是一種壓縮格式，在此格式中，Y 會水準取樣每2個圖元，而您和 V 會以水準方式取樣每4個圖元。 每個 macropixel 都是4個位元組，且包含4個圖元。 它會使用下列位元組順序：

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P 是4:1:1 封裝格式。 它會使用下列位元組順序：

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 是平面格式，在此格式中，您和 V 會水準和垂直取樣每4個圖元 (有時也稱為 16:1:1) 。 V 平面會出現在 U 平面之前。
-    (MEDIASUBTYPE IF09) 的 Indeo YVU9 格式 \_ 是 YVU9 的變化，以及 U 平面之後的額外差異框架資訊。 Windows 不再支援 Indeo 編解碼器。
-   YVYU 類似于具有不同位元組順序的 UYVY： `Y0 V0 Y1 U0`

-   Windows 不再支援 Indeo 編解碼器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[適用于影片轉譯的建議8位 YUV 格式](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[影片子類型](video-subtypes.md)
</dt> <dt>

[使用影片畫面](working-with-video-frames.md)
</dt> </dl>

 

 
