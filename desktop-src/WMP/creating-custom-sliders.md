---
title: 建立自訂滑杆
description: 建立自訂滑杆
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- 建立外觀、滑杆
- Windows Media Player 的外觀、滑杆
- 外觀、滑杆
- 外觀中的滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507332"
---
# <a name="creating-custom-sliders"></a>建立自訂滑杆

您可以在任何想要的圖形中建立自訂滑杆。 在此範例中，選擇了簡單的帶，但實際的圖形可以是任何一種。 以下是 **CUSTOMSLIDER** 元素的程式碼：


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



這會設定滑杆的初始值。 引進兩個新的點陣圖。 其中一個是灰階點陣圖 (slider.bmp) ，可定義按一下時將使用的值，另一個 (slider.bmp) 則會決定按一下灰階的特定部分時，會顯示哪個影像。

初始值是藉由使用 wmpprop 接聽磁片區來決定，然後當使用者按一下會觸發值變更的滑杆部分時，就可以變更該磁片區。

您可以在 SDK 的 [範例] 區段中看到類似的工作滑杆外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




