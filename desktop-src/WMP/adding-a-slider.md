---
title: 新增滑杆
description: 新增滑杆
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- 建立外觀、滑杆
- Windows Media Player 的外觀、滑杆
- 外觀、滑杆
- 外觀中的滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021702"
---
# <a name="adding-a-slider"></a>新增滑杆

您可以新增滑杆來顯示媒體目前的位置，也可以讓使用者變更目前媒體檔案中的位置。

首先，您必須加入 **滑杆** 元素：


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



這會根據目前媒體檔案的持續時間來設定最大值。 這會使用小型 thumb 影像點陣圖，而這只是10圖元 x 綠色正方形的10圖元。 滑杆的背景會是紅色，前景則會是藍色。 當使用者將 thumb 影像拖曳至新位置，並讓滑鼠移至滑鼠按鍵時，媒體將會變更至該位置。

但是，除非您使用 **控制項** 專案的 **currentPosition \_ onchange** 屬性來測量目前的位置，它會內嵌在 **PLAYER** 元素中，否則滑杆不會自行移動。


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



當媒體的位置變更時，就會引發事件，然後執行程式程式碼，將滑杆的值變更為媒體的目前位置。

您可以在 SDK 的 [範例] 區段中看到類似的工作滑杆外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




