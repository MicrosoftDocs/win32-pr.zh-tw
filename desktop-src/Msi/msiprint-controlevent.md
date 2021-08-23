---
description: 此事件是由 ScrollableText 控制項所發佈，讓使用者可以列印該控制項的內容。
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2107e4930e7d2d410846f656f25143926f8675f354976d866b2ee5d547b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519778"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent

此事件是由 [ScrollableText 控制項](scrollabletext-control.md) 所發佈，讓使用者可以列印該控制項的內容。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始提供此 ControlEvent。

此事件應由位於與[ScrollableText 控制項](scrollabletext-control.md)相同對話方塊的[按鈕控制項](pushbutton-control.md)訂閱。 TheMsiPrint ControlEvent 應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。

## <a name="published-by"></a>發佈者

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

與[ScrollableText 控制項](scrollabletext-control.md)相同對話方塊上的[按鈕](pushbutton-control.md)控制項可用來顯示模式對話方塊，讓使用者可以列印 ScrollableText 控制項的內容。

 

 



