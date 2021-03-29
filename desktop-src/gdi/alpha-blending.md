---
description: Alpha 混色用來顯示 Alpha 點陣圖，也就是具有透明或半透明圖元的點陣圖。
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: " (Windows GDI) 的 Alpha 混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972785"
---
# <a name="alpha-blending-windows-gdi"></a> (Windows GDI) 的 Alpha 混合

*Alpha 混色* 用來顯示 Alpha 點陣圖，也就是具有透明或半透明圖元的點陣圖。 除了紅色、綠色和藍色色頻外，Alpha 點陣圖中的每個圖元都有一個透明元件，稱為 *Alpha* 色板。 Alpha 色板通常會包含與色頻一樣多的位數。 例如，8位 Alpha 通道可以代表256的透明度層級，從 0 (整個點陣圖) 至 255 (整個點陣圖是不透明的) 。

藉由呼叫 [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)來叫用 Alpha 混色機制，它會參考 [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) 結構。

只有 32-bpp BI RGB 支援每圖元的 Alpha 值 \_ 。 此公式定義如下：


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



這會在記憶體中表示，如下表所示。



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alpha | 紅色   | 綠色 | 藍色  |



 

點陣圖也可能會以套用至整個點陣圖的透明因數來顯示。 您可以藉由在 [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)結構中設定 **SourceConstantAlpha** ，來顯示任何點陣圖格式和全域常數 Alpha 值。 全域常數 Alpha 值具有256的透明度層級，從 0 (整個點陣圖完全透明) 至 255 (整個點陣圖完全不透明) 。 全域常數 Alpha 值會與每圖元的 Alpha 值結合。

如需範例，請參閱 [Alpha 混色點陣圖](alpha-blending-a-bitmap.md)。

 

 



