---
description: ComboBox 控制項會顯示預先定義值的下拉式清單，以及使用者可以在其中輸入值的編輯欄位。
ms.assetid: 81fbc039-3c86-4086-a565-57a4ea2c12fb
title: 'ComboBox 控制項 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664244a4e14b198bf532551bb67abdd405fa780d394312de4c5f2ad093885f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145577"
---
# <a name="combobox-control"></a>ComboBox 控制項

ComboBox 控制項會顯示預先定義值的下拉式清單，以及使用者可以在其中輸入值的編輯欄位。 若要將這個控制項與字串或整數屬性產生關聯，請在 [控制資料表](control-table.md)的屬性資料行中輸入屬性的名稱。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                               | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | 這是與控制項相關聯之間接屬性的名稱。 如果已設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 如果設定了間接屬性位，此名稱也會是 [控制資料表](control-table.md)之屬性資料行中所列屬性的值。                                                                                                                                                                               |
| [位置](position-control-attribute.md)                         |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                                                                                                                                                                    |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | 這是與此控制項相關聯之屬性的名稱。 如果未設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 這個屬性是在 [控制資料表](control-table.md)的屬性資料行中指定。                                                                                                                                                                                                                                               |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | 此控制項顯示或變更之屬性的目前值。 如果未設定間接屬性位，則這是 PropertyName 的值。 如果已設定間接屬性位，這就是 IndirectPropertyName 的值。 如果屬性變更，控制項就會反映新的值。                                                                                                                                                                                                                              |
| [Text](text-control-attribute.md)                                 |                                  | 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&style}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。 若要指定使用者可以輸入的字元數，請在任何字型規格之後附加 {n}，其中 n 是正整數。<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制資料表](control-table.md) 中的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                                                                                                                                                            |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                                                                                                                                                                          |
| [沉沒](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體、外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                                                                                                   |
| [間接](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | 控制項會在 [控制資料表](control-table.md)的屬性資料行中顯示或變更屬性的值。 控制項會顯示或變更屬性的值，此屬性的識別碼列于控制資料表的屬性資料行中。<br/> 決定是否要間接參考與此控制項相關聯的屬性。<br/>                                                                                                                                                        |
| [整數](integer-control-attribute.md)                           | 0x00000000 0x00000010<br/> | 與控制項相關聯的屬性是一個字串值。 與控制項相關聯的屬性是整數值。<br/> 在 [控制項資料表](control-table.md) 的 [屬性] 資料行的位字組中加入此位，以在建立控制項時設定這個屬性。<br/>                                                                                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                                                                                                                                                                                 |
| [排序](sorted-control-attribute.md)                             | 未設定0x00010000<br/>    | 依字母順序顯示的專案。 依 [ListView 資料表](listview-table.md)中指定的順序顯示的專案。<br/> 控制項會查詢 [ComboBox 資料表](combobox-table.md)，如果已設定排序的樣式位，則下拉式方塊 **會具有 CBS** \_ 排序樣式，並依排序指定顯示專案。 如果未設定此樣式位，專案會依字母順序顯示。<br/>                                                                                                                    |
| [ComboList](combolist-control-attribute.md)                       | 未設定0x00020000<br/>    | 具有編輯欄位的下拉式方塊。 具有編輯欄位的下拉式方塊會以靜態文字欄位取代。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [UsersLanguage](userslanguage-control-attribute.md)               | 0x00000000 0x00100000<br/> | 在資料庫字碼頁中建立的字型。 在使用者的預設 UI 字碼頁中建立的字型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從 COMBOBOX 類別建立這個控制項。 它具有 **CBS \_ AUTOHSCROLL**、 **WS \_ TABSTOP**、 **ws \_ GROUP** 和 **ws \_ 子** 樣式。 如果 ComboList 位是 on，它也會有 **cbs \_ DROPDOWNLIST** 樣式，否則它會有 **cbs \_ 下拉式清單** 樣式。

在 [控制項資料表](control-table.md)的文字欄位開頭，將0到2147483646的數位放在大括弧中，即可限制可輸入文字的長度。 例如，如果文字欄位以開頭 {80} ，則字串的長度會限制為80個字元。 如果未在資料表中提供這類限制，或指定0，則長度會設定為最大可能的 (2147483646 個字元) 。 負數值或非數值將會產生錯誤。

為了與螢幕閱讀程式相容，在撰寫具有 ComboBox 控制項的對話方塊做為第一個使用中控制項時，您必須將 [編輯] 欄位中的文字欄位設為 [對話方塊資料表](dialog-table.md)中的第一個使用中控制項。 由於靜態文字無法取得焦點，因此當建立對話方塊時，[編輯] 欄位一開始會有焦點。 這樣做可確保螢幕讀取器會顯示正確的資訊。

 

