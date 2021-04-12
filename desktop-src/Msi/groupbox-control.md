---
description: 群組方塊控制項會顯示矩形（可能有標題文字），以在對話方塊上將其他控制項群組在一起。
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: '分組控制項 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191864"
---
# <a name="groupbox-control"></a>GroupBox 控制項

群組方塊控制項會顯示矩形（可能有標題文字），以在對話方塊上將其他控制項群組在一起。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與 [分組] 控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                               | 十六進位位                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md)         |                                  | 對話方塊中的控制項位置。 將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                                                         |
| [Text](text-control-attribute.md)                 |                                  | 顯示控制項左上角的標題。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&style}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 請在 [control table](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md) 中的 Attributes 資料行的位字組中包含這個位，讓控制項在建立時可見或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                                             |
| [沉沒](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從 BUTTON 類別建立這個控制項。 它具有 **BS \_ 分組**、 **WS \_ 子** 系和 **ws \_ 群組** 樣式。

即使沒有標題，控制項視窗的頂端和可見畫面格的頂端之間一定會有間距。

 

 
