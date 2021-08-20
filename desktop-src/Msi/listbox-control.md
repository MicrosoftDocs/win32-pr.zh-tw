---
description: ListBox 控制項是一般清單方塊，可讓使用者從預先決定的值清單中進行單一選取。
ms.assetid: f2aace82-3b42-4790-a817-1b874a702938
title: 'ListBox 控制項 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8ba99e0328fe2ca8096ba5aa19f7b359be805d5e233cb12208a9604160971e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013106"
---
# <a name="listbox-control"></a>ListBox 控制項

ListBox 控制項是一般清單方塊，可讓使用者從預先決定的值清單中進行單一選取。 可能的值是從 [Listbox 資料表](listbox-table.md)讀取的。 您可以在 [控制資料表](control-table.md)的屬性資料行中輸入屬性的名稱，以建立字串或整數屬性的關聯。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                               | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | 這是與控制項相關聯之間接屬性的名稱。 如果已設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 如果設定了間接屬性位，此名稱也會是 [控制資料表](control-table.md)之屬性資料行中所列屬性的值。                                                                                                                                                                               |
| [位置](position-control-attribute.md)                         |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                                                                                                                                                                    |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | 這是與此控制項相關聯之屬性的名稱。 如果未設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 這個屬性是在 [控制資料表](control-table.md)的屬性資料行中指定。                                                                                                                                                                                                                                               |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | 此控制項顯示或變更之屬性的目前值。 如果未設定間接屬性位，則這是 PropertyName 的值。 如果已設定間接屬性位，這就是 IndirectPropertyName 的值。 如果屬性變更，控制項就會反映新的值。                                                                                                                                                                                                                                  |
| [Text](text-control-attribute.md)                                 |                                  | 螢幕讀取器所顯示的文字。 輸入要顯示在 [控制項資料表](control-table.md)的文字資料行中的文字。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&style}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制資料表](control-table.md) 中的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                                                                                                                                                            |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                                                                                                                                                                          |
| [沉沒](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體、外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                                                                                                   |
| [間接](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | 控制項會在 [控制資料表](control-table.md)的屬性資料行中顯示或變更屬性的值。 控制項會顯示或變更屬性的值，此屬性的識別碼列于控制資料表的屬性資料行中。<br/> 決定是否要間接參考與此控制項相關聯的屬性。<br/>                                                                                                                                                        |
| [整數](integer-control-attribute.md)                           | 0x00000000 0x00000010<br/> | 與控制項相關聯的屬性是一個字串值。 與控制項相關聯的屬性是整數值。<br/> 在 [控制項資料表](control-table.md) 的 [屬性] 資料行的位字組中加入此位，以在建立控制項時設定這個屬性。<br/>                                                                                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                                                                                                                                                                                 |
| [排序](sorted-control-attribute.md)                             | 0x00000000 0x00010000<br/> | 依字母順序顯示的專案。 依 [ListView 資料表](listview-table.md)中指定的順序顯示的專案。<br/> 在 [屬性] 資料行的位字中包含此位，以依 ListView 資料表的 [訂單] 資料行所指定的順序來顯示專案。<br/>                                                                                                                                                                                                                                        |
| [UsersLanguage](userslanguage-control-attribute.md)               | 0x00000000 0x00100000<br/> | 在資料庫字碼頁中建立的字型。 在使用者的預設 UI 字碼頁中建立的字型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從 LISTBOX 類別建立這個控制項。 它具有 **ws \_ TABSTOP**、 **ws \_ GROUP** 和 **ws \_ 子** 樣式。 如果已排序的控制項樣式位為開啟，則會以磅的 **\_ 通知**、 **ws \_ VSCROLL** 和 **ws \_ 框線** 樣式來建立控制項，否則會以 **磅 \_ 標準** 樣式來建立控制項。

 

 
