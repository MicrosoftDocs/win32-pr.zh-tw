---
description: 此控制項會顯示一段長串的文字，無法完全放在頁面上。 此控制項的常見用途是顯示授權合約。
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: ScrollableText 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f4d5ac48f6b89b779960126e62c204d1d09e1f9a7bc832b0e3477635df35ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041298"
---
# <a name="scrollabletext-control"></a>ScrollableText 控制項

此控制項會顯示一段長串的文字，無法完全放在頁面上。 此控制項的常見用途是顯示授權合約。

請注意，與此控制項搭配使用的文字字串不能包含內嵌屬性。 若要以內嵌屬性顯示文字，請改用 [文字控制項](text-control.md)。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                               | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md)         |                                  | 對話方塊中的控制項位置。 將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | 控制項所顯示的文字。 在 [ [控制] 資料表](control-table.md)的 [文字] 資料行中輸入 RTF 文字字串。                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 若要在建立控制項時顯示或隱藏控制項，請在 [control table](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)中，于 [屬性] 資料行的位字組中加入此位。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md) 的 [屬性] 資料行中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>             |
| [沉沒](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 以凹陷、3D、外觀顯示控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字會靠右對齊。<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                              |
| [BiDi](bidi-control-attribute.md)                 | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從 RICHEDIT 類別建立這個控制項。 它有 **es \_ 多行**、 **ws \_ VSCROLL**、 **es \_ READONLY**、 **ws \_ TABSTOP**、 **ES \_ AUTOVSCROLL**、 **ws \_ CHILD**、 **ws \_ GROUP** 和 **es \_ NOOLEDRAGDROP** 樣式。

 

 
