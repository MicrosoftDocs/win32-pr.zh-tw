---
description: EVR 屬性
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: EVR 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974537"
---
# <a name="evr-attributes"></a>EVR 屬性

您可以使用下列屬性來設定增強型影片轉譯器 (EVR) 。



| 屬性                                                                                                         | 描述                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | 允許 EVR 對 Microsoft Direct3D **IDirect3DDevice9：:P 重發** 的方法進行批次呼叫。                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | 允許 EVR 利用 bob 去交錯來改善效能。                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | 允許 EVR 藉由略過每個交錯框架的第二個欄位來改善效能。                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | 允許 EVR 限制其輸出，以符合 GPU 頻寬。                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | 允許 EVR 在小於輸出矩形的矩形內混合影片，然後調整結果。 |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | 強制 EVR 對 **IDirect3D9Device：:P 重發** 的方法進行批次呼叫。                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | 強制 EVR 使用 bob 去交錯。                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | 強制 EVR 略過每個交錯框架的第二個欄位。                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | 強制 EVR 在小於輸出矩形的矩形內混合影片，然後調整結果。 |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | 強制 EVR 將其輸出限制為符合 GPU 頻寬。                                                               |
| [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 啟用**](mf-activate-custom-video-mixer-activate-attribute.md)         | 指定啟用物件，為增強型影片轉譯器 (EVR) 建立自訂的視頻混音器。                  |
| [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | EVR 之自訂視頻混音器的 CLSID。                                                                               |
| [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 旗標**](mf-activate-custom-video-mixer-flags-attribute.md)               | 指定如何為 EVR 建立自訂混音器。                                                                      |
| [**MF \_ 啟用 \_ 自訂 \_ 影片 \_ 演講者 \_ 啟用**](mf-activate-custom-video-presenter-activate-attribute.md) | 指定啟用物件，以建立 EVR 的自訂影片展示者。                                        |
| [**MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | EVR 之自訂影片展示者的 CLSID。                                                                           |
| [**MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ 旗標**](mf-activate-custom-video-presenter-flags-attribute.md)       | 指定如何建立 EVR 的自訂展示者。                                                                  |
| [**MF \_ 啟用 \_ 影片 \_ 視窗**](mf-activate-video-window-attribute.md)                                         | 影片裁剪視窗的控制碼。                                                                                     |
| [**MF \_ SA \_ 需求 \_ 範例 \_ 計數**](mf-sa-required-sample-count-attribute.md)                                  | 指出 EVR 媒體接收器需要去交錯的未壓縮緩衝區數目。                         |
| [**影片 \_ 縮放 \_ 矩形**](video-zoom-rect-attribute.md)                                                            | 指定 EVR 混音器的縮放矩形。                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 



