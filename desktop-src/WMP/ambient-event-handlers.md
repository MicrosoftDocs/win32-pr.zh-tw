---
title: 環境事件處理常式
description: 環境事件處理常式
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Windows Media Player 的外觀、環境事件處理常式
- 外觀，環境事件處理常式
- 外觀、環境事件處理常式的參考
- 環境事件處理常式
- 事件，環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff72739ec1791b79d6113415f1219a1ddee578b4b5a690ffaaac62bf6b3dbcfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865088"
---
# <a name="ambient-event-handlers"></a>環境事件處理常式

下列事件處理常式可以針對大部分的外觀元素來執行。 使用 **事件** 關鍵字存取的環境事件屬性，可以在事件處理常式中使用，以判斷在事件發生時的鍵盤和滑鼠狀態。



| 事件處理常式                                   | 描述                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*屬性* \_onchange](attribute-onchange.md) | 當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。 事件處理常式的名稱是屬性的名稱，後面接著底線和 "onchange"，例如「值 \_ onchange」。 |
| [onblur](onblur.md)                            | 處理當元素失去鍵盤焦點時所發生的事件。                                                                                                                                                       |
| [onclick](onclick.md)                          | 處理當使用者按一下專案時所發生的事件。                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | 處理使用者按兩下元素時所發生的事件。                                                                                                                                                         |
| [onendAlphablend](onendalphablend.md)          | 處理元素完成 **AlphaBlendTo** 作業時所發生的事件。                                                                                                                                         |
| [onendmove](onendmove.md)                      | 處理元素完成 **moveTo** 作業時所發生的事件。                                                                                                                                                |
| [onfocus](onfocus.md)                          | 處理當元素收到鍵盤焦點時所發生的事件。                                                                                                                                                    |
| [onkeydown](onkeydown.md)                      | 處理按下按鍵時所發生的事件。                                                                                                                                                                           |
| [onkeypress](onkeypress.md)                    | 處理使用者按下英數位鍵時所發生的事件。                                                                                                                                                       |
| [onkeyup](onkeyup.md)                          | 處理釋放金鑰時所發生的事件。                                                                                                                                                                          |
| [onmousedown](onmousedown.md)                  | 處理當使用者按一下滑鼠按鍵時所發生的事件。                                                                                                                                                             |
| [](onmousemove.md)                  | 處理當使用者在專案上方移動滑鼠指標時所發生的事件。                                                                                                                               |
| [onmouseout](onmouseout.md)                    | 處理當使用者將指標移出元素時所發生的事件。                                                                                                                                                 |
| [onmouseover](onmouseover.md)                  | 處理使用者第一次將指標放在元素上時所發生的事件。                                                                                                                                         |
| [onmouseup](onmouseup.md)                      | 處理當滑鼠指標在專案上方時，當使用者放開滑鼠按鍵時所發生的事件。                                                                                                                     |
| [onresize](onresize.md)                        | 處理控制項調整時所發生的事件。                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**環境事件屬性**](ambient-event-attributes.md)
</dt> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




