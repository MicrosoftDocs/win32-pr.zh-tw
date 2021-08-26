---
description: VMR 篩選元件
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: VMR 篩選元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6e8d37e1b5ac8c00da024fe78d4e18e38eed1e1735e787284d389769cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903331"
---
# <a name="vmr-filter-components"></a>VMR 篩選元件

VMR 採用模組化設計，可讓應用程式針對許多不同的轉譯案例進行設定。 根據其設定，除了) 的輸入圖釘之外，VMR 還包含二到五個子元件 (。

![具有多個資料流程的視窗模式 vmr](images/vmr-multiple-streams.png)

**Mixer：** 混音器是負責混合多個資料流程的 COM 物件。 去交錯也會出現在混音器內。 當偵測到多個輸入資料流程時，或當輸入影片交錯時，VMR 會載入混音器。 此混音器會收集每個輸入資料流程的相關資訊，並將資料流程排序成正確的 Z 順序。 它負責判斷每個輸入 pin 何時收到範例，並在適當的時間指示影像組合器執行實際的混合。 混音器也會計算要套用至每個輸出影像的時間戳記。 當應用程式提供要顯示在複合影像上方的點陣圖時，混音器會負責確保即使在輸入資料流程的迭置順序已修改的情況下，點陣圖也會顯示在頂端。

**影像組合器：** 影像組合器是一種 COM 物件，它會執行輸入資料流程的實際混合，以在配置器提供者所提供的單一 DirectDraw 或 Direct3D 介面上執行。 VMR 會提供預設的影像組合器，可讓應用程式執行立體的 Alpha 混色效果。 應用程式可以提供自訂影像組合器來啟用其他的立體和3-d 效果，例如將材質套用至影像的部分、每圖元的 Alpha 混色、將影像對應至固定或移動立體物件等等。

配置器 **-展示者：** 配置器-展示者是一種 COM 物件，它會配置 DirectDraw 或 Direct3D 物件，並處理與圖形配接器的通訊。 繪圖可作為翻轉或 array.blit 執行。 您可以插入自己的配置器-展示器，以便建立及控制 DirectDraw 或 Direct3D 物件，以及/或在簡報時取得影片位的存取權。

**視窗管理員：** 視窗管理員只會在視窗模式中使用。 視窗管理員支援舊版 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 和 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面，以提供回溯相容性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於影片混合轉譯](about-the-video-mixing-render.md)
</dt> </dl>

 

 



