---
title: LISTBOX 元素
description: LISTBOX 元素
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Windows Media Player 的外觀、LISTBOX 元素
- 外觀，LISTBOX 元素
- LISTBOX 元素
- 外觀、LISTBOX 元素的參考
- 元素，LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021235"
---
# <a name="listbox-element"></a>LISTBOX 元素

**LISTBOX** 元素提供一種方式，讓使用者從清單中選取專案。 您可以使用 **ITEM 專案** 做為 **LISTBOX** 專案的子系，以指定這些專案。 如果您需要只在需要時才顯示的清單方塊控制項，請使用 **popup** 元素，這與 **LISTBOX** 元素相同，但 **popup** 屬性的預設值除外，後者會指定其顯示行為。

**LISTBOX** 元素支援下列屬性。



| 屬性                                        | 描述                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](listbox-backgroundcolor.md)   | 指定或抓取清單方塊控制項中的背景色彩。                                                  |
| [邊境](listbox-border.md)                     | 指定或抓取值，指出清單方塊控制項是否有框線。 只能在設計階段設定。  |
| [firstVisibleItem](listbox-firstvisibleitem.md) | 指定或抓取清單方塊控制項中第一個可見行的索引。                                   |
| [focusItem](listbox-focusitem.md)               | 指定或抓取包含焦點的行。                                                                  |
| [fontFace](listbox-fontface.md)                 | 指定或抓取清單方塊控制項的字型。                                                             |
| [fontSize](listbox-fontsize.md)                 | 指定或抓取清單方塊控制項的字型大小。                                                        |
| [fontStyle](listbox-fontstyle.md)               | 指定或抓取清單方塊控制項的字型樣式。                                                       |
| [foregroundColor](listbox-foregroundcolor.md)   | 指定或抓取清單方塊控制項中的文字色彩。                                                        |
| [itemCount](listbox-itemcount.md)               | 捕獲清單方塊控制項中的專案數。                                                                |
| [多](listbox-multiselect.md)           | 指定或抓取值，指出使用者是否可以選取多行。 只能在設計階段設定。 |
| [彈出](listbox-popup.md)                       | 指定值，這個值表示專案是否代表 popup 或清單方塊控制項。                              |
| [readOnly](listbox-readonly.md)                 | 指定或抓取值，指出文字是否為唯讀或可由使用者選取的文字。              |
| [selectedItem](listbox-selecteditem.md)         | 指定或抓取清單方塊控制項中所選取專案的索引。                                        |
| [排序](listbox-sorted.md)                     | 指定或抓取值，指出清單方塊控制項是否依照字母順序排序。                      |



 

**LISTBOX** 元素支援下列方法。



| 方法                                                 | 描述                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [appendItem](listbox-appenditem.md)                   | 在清單方塊控制項的結尾插入新的文字。                                                                  |
| [deleteAll](listbox-deleteall.md)                     | 刪除清單方塊控制項中的所有專案。                                                                          |
| [deleteItem](listbox-deleteitem.md)                   | 刪除指定索引處的清單方塊控制項專案。                                                             |
| [解雇](listbox-dismiss.md)                         | 隱藏控制項。                                                                                                    |
| [findItem](listbox-finditem.md)                       | 從指定的專案索引後面的專案開始搜尋指定的字串。                                |
| [getItem](listbox-getitem.md)                         | 使用指定的索引，抓取專案的文字。                                                             |
| [getNextSelectedItem](listbox-getnextselecteditem.md) | 從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。 |
| [insertItem](listbox-insertitem.md)                   | 將指定的文字插入清單方塊控制項中的指定索引處。                                            |
| [replaceItem](listbox-replaceitem.md)                 | 以指定的文字取代指定索引處的文字。                                                     |
| [setSelectedState](listbox-setselectedstate.md)       | 選取或取消選取具有指定索引的專案。                                                               |
| [show](listbox-show.md)                               | 顯示控制項。                                                                                                 |



 

> [!Note]  
> 此元素需要 Windows XP 或更新版本的 Windows Media Player。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**POPUP 元素**](popup-element.md)
</dt> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




