---
description: 應用程式會藉由呼叫 FillRgn 函式並提供識別特定筆刷的控制碼，填滿區域的內部。
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: 填滿區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d909643155b027f72b4235db366e640d7e53dacd4825b85090f9958aec1c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015398"
---
# <a name="filling-regions"></a>填滿區域

應用程式會藉由呼叫 [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) 函式並提供識別特定筆刷的控制碼，填滿區域的內部。 當應用程式呼叫 FillRgn 時，系統會使用指定之裝置內容的目前填滿模式，填滿該區域中的筆刷。 填滿模式有兩種：替代和繞組。 應用程式可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函數來設定裝置內容的填滿模式。 應用程式可以藉由呼叫 [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) 函式，來取得裝置內容的目前填滿模式。

下圖顯示兩個相同的區域：一個使用替代模式填滿，另一個則使用纏繞模式填滿。

![顯示 2 5 點星星的圖例：一個只填滿在點中，另一個則完全填滿](images/csrgn-03.png)

## <a name="alternate-mode"></a>替代模式

若要判斷當指定替代模式時，系統要強調的圖元，請執行下列測試：

1.  選取區域內部的圖元。
2.  以正 x 方向繪製虛光線，從該圖元到無限大。
3.  每次光線相交界限線時，就會遞增計數值。

如果 count 值是奇數，系統就會反白顯示圖元。

## <a name="winding-mode"></a>纏繞模式

若要判斷當指定了纏繞模式時，系統要強調的圖元，請執行下列測試：

1.  決定繪製每個邊界線的方向。
2.  選取區域內部的圖元。
3.  以正 x 方向繪製虛光線，從圖元朝無限大。
4.  每次光線相交具有正面 y 元件的界限線時，就會遞增計數值。 每次光線相交具有負 y 元件的界限線時，就會遞減計數值。

如果 count 值為非零值，系統會反白顯示圖元。

 

 



