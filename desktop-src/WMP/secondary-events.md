---
title: 次要事件
description: 次要事件
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player 的外觀，次要事件
- 外觀，次要事件
- 事件，次要
- 撰寫適用于面板的程式碼，次要事件
- 次要事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462384"
---
# <a name="secondary-events"></a>次要事件

您可以判斷觸發特定事件時，所發生的其他事件。 例如，按一下滑鼠按鍵時，您可能會想要知道 ALT 鍵是否同時關閉。

## <a name="event-attributes"></a>事件屬性

以下是支援的事件屬性：

-   **altKey**
-   **按鈕**
-   **clientX**
-   **clientY**
-   **ctrlKey**
-   **fromElement**
-   **offsetX**
-   **offsetY**
-   **screenX**
-   **screenY**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **keyCode**

如需這些屬性的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md)。

## <a name="using-secondary-events"></a>使用次要事件

您只能處理 JScript 程式碼中的事件屬性。 您必須使用下列語法：


```C++
event.eventattributename
```



*eventattributename* 是事件屬性的名稱。 例如，若要判斷在 click 事件期間是否按下 ALT 鍵，您可以在 JScript 程式碼中使用下列幾行：


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**處理事件**](handling-events.md)
</dt> </dl>

 

 




