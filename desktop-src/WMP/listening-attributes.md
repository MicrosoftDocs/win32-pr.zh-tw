---
title: 接聽屬性
description: 接聽屬性
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player 的外觀，接聽屬性
- 外觀，接聽屬性
- 外觀的參考，接聽屬性
- 接聽屬性
- 屬性，接聽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507173"
---
# <a name="listening-attributes"></a>接聽屬性

接聽屬性是用來將某個屬性連接到另一個屬性，讓它的值會在每次其他屬性的值變更時變更。

接聽屬性 **wmpprop：** 是最有用的。 如果有一個屬性的值指定為 **wmpprop：** 第二個屬性，則第一個值會自動更新，以反映第二個值變更時的第二個值。

**範例︰**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



如此一來，mySlider 的值（顯示于滑杆控制項的位置）也可以在文字方塊內顯示為數字。

您可以使用其他兩個接聽屬性 **wmpenabled：** 和 **wmpdisabled：** 來變更控制項的 **已啟用** 屬性，視播放程式中目前是否有可用的功能而定。 這些屬性只能接聽 **Controls** 物件的方法。

**範例︰**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**雜項**](miscellaneous.md)
</dt> </dl>

 

 




