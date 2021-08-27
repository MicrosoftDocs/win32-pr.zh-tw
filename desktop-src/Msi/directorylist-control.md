---
description: DirectoryList 控制項會顯示目前顯示在 PathEdit 控制項中的部分路徑。 DirectoryList 控制項會顯示 DirectoryCombo 控制項目前所顯示之目錄底下的資料夾。
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: DirectoryList 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce0cf409f4ca7335bd032f1fc63831db88ace14424ef7a73cd3853c9ff3e2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086188"
---
# <a name="directorylist-control"></a>DirectoryList 控制項

DirectoryList 控制項會顯示目前顯示在 [PathEdit 控制項](pathedit-control.md)中的部分路徑。 DirectoryList 控制項會顯示 [DirectoryCombo 控制項](directorycombo-control.md)目前所顯示之目錄底下的資料夾。

PathEdit、DirectoryCombo 和 DirectoryList 控制項都與相同的字串值屬性相關聯。 該屬性是使用者選取的路徑。 在 [控制資料表](control-table.md)的屬性資料行中輸入屬性的名稱。 這個屬性的初始值必須包含至少一個磁片區和一個子層次。 在 [屬性資料表](property-table.md)的 [值] 資料行中，指定屬性的初始值。

此控制項的設計目的是要搭配[PathEdit](pathedit-control.md)和 DirectoryList 控制項用於[流覽對話方塊](browse-dialog.md)。

DirectoryList 控制項會發佈下列事件。



| ControlEvent                                            | 描述                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | 建立新的資料夾，並選取 [名稱] 欄位以進行編輯。      |
| [IgnoreChange](ignorechange-controlevent.md)           | 反白顯示目前目錄中的資料夾，但不會開啟。 |
| [DirectoryListUp](directorylistup-controlevent.md)     | 選取目前目錄的父系。                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | 選取並反白顯示目錄。                               |



 

DirectoryList 控制項絕不會顯示 [控制項資料表](control-table.md) 之文字欄位的內容。 相反地，這個欄位會指定控制項顯示的文字樣式，並包含螢幕審核公用程式所使用之控制項的描述。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。 下列資訊是由螢幕審核公用程式讀取，作為控制項的描述。 請參閱 [協助工具](accessibility.md)。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                               | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | 這是與控制項相關聯之間接屬性的名稱。 如果已設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 如果設定了間接屬性位，此名稱也會是 [控制資料表](control-table.md)之屬性資料行中所列屬性的值。                        |
| [位置](position-control-attribute.md)                         |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | 這是與此控制項相關聯之屬性的名稱。 如果未設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 這個屬性是在 [控制資料表](control-table.md)的屬性資料行中指定。                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | 此控制項顯示或變更之屬性的目前值。 如果未設定間接屬性位，則這是 PropertyName 的值。 如果已設定間接屬性位，這就是 IndirectPropertyName 的值。 如果屬性變更，控制項就會反映新的值。                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | 若要在螢幕讀取器中顯示文字，請在 [ [控制] 資料表](control-table.md)的 [文字] 資料行中輸入文字。 請參閱 [協助工具](accessibility.md)。                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行的位字組中包含此位。在建立控制項時，讓控制項成為可見或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                   |
| [沉沒](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 以凹陷、3D、外觀顯示控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                             |
| [間接](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | 控制項會在 [控制資料表](control-table.md)的屬性資料行中顯示或變更屬性的值。 控制項會顯示或變更屬性的值，此屬性的識別碼列于控制資料表的屬性資料行中。<br/> 決定是否要間接參考與此控制項相關聯的屬性。<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                         |
| [雙向控制項](bidi-control-attribute.md)                         | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

您可以使用 CreateWindowEx 函數，從 WC \_ LISTVIEW 類別建立這個控制項[](/windows/win32/api/winuser/nf-winuser-createwindowexa) 。 它有 **lvs) \_ 清單**、 **lvs) \_ EDITLABELS**、 **WS \_ VSCROLL**、 **lvs) \_ SHAREIMAGELISTS**、 **lvs) \_ AUTOARRANGE**、 **lvs) \_ SINGLESEL**、 **ws \_ BORDER**、 **lvs) \_ SORTASCENDING**、 **ws \_ CHILD**、 **ws \_ GROUP** 和 **ws \_ TABSTOP** 樣式。

此控制項可讓使用者選取目前選取範圍的子資料夾。 使用其他按鈕時，也可讓使用者在目前的選取範圍中選取新資料夾，或在路徑中向上一層執行。 如果使用者選擇新資料夾已存在之資料夾中的 [ **建立新資料夾** ] 按鈕，則不會建立第二個新資料夾，並選取現有的新資料夾名稱進行編輯。

 

