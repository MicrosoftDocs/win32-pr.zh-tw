---
description: 作業的 VMR 模式
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: 作業的 VMR 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980730"
---
# <a name="vmr-modes-of-operation"></a>作業的 VMR 模式

VMR 的元件架構可讓應用程式以各種方式進行設定，視轉譯的執行方式而定。 下表顯示三種呈現模式以及兩種混合模式，以及每個設定都存在的元件。



| 模式       | 單一資料流程                                                                     | 多個資料流程 (混合模式)                                                                                              |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 視窗   | 配置器-presenterCore 同步處理單位<br/> 視窗管理員<br/> | MixerCompositor\*<br/> 配置器-展示者<br/> 核心同步處理單位<br/> 視窗管理員<br/> |
| 窗戶 | 配置器-presenterCore 同步處理單位<br/>                           | MixerCompositor\*<br/> 配置器-展示者<br/> 核心同步處理單位<br/>                           |
| Renderless | 配置器-) 核心同步處理單位提供的應用程式提供者 (<br/> | MixerCompositor\*<br/> 配置器-由應用程式) 提供的簡報者 (<br/> 核心同步處理單位<br/> |



 

\* 指出應用程式有提供自訂群組件或使用預設元件的選項。

在 [所有設定] 中，當您使用 VMR 建立篩選圖形時要記住的重點是，您必須先設定 VMR，然後再進行連接。

對於所有設定，VMR 連接到上游篩選器之後，就無法動態新增或移除 pin，但可以連線並中斷連線。 如果應用程式不確定需要多少 pin，則應該將 VMR 設定為可能需要的最大數目。 篩選器上是否有未使用的輸入 pin 不會降低轉譯效能。 不同于舊的重迭混音器，VMR 沒有輸出的 pin，因為它不需要個別的視窗管理篩選。

下列各節說明如何設定指定模式的 VMR：

-   [VMR 視窗 (相容性) 模式](vmr-windowed--compatibility--mode.md)
-   [VMR 無視窗模式](vmr-windowless-mode.md)
-   [具有多個資料流程 (混合模式的 VMR) ](vmr-with-multiple-streams--mixing-mode.md)
-   [YUV 混合模式](yuv-mixing-mode.md)
-   [在組合空間中定位和移動影片矩形](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [VMR Renderless 播放模式 (自訂配置器-展示者) ](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [DirectDraw 獨佔模式](directdraw-exclusive-mode.md)

 

 




