---
description: DirectoryCombo \_ 控制項會顯示目前顯示在 PathEdit 控制項中的部分路徑。 此控制項不會顯示路徑的最後一個區段，DirectoryList 控制項會顯示該區段。
ms.assetid: c2dd494b-b51d-4d3a-ab8f-f6d64a62feb3
title: DirectoryCombo 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76729786c1e305e0ed4902750bd47f6a10427f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991881"
---
# <a name="directorycombo-control"></a>DirectoryCombo 控制項

DirectoryCombo \_ 控制項會顯示目前顯示在 [PathEdit 控制項](pathedit-control.md)中的部分路徑。 此控制項不會顯示路徑的最後一個區段， [DirectoryList 控制項](directorylist-control.md)會顯示該區段。

DirectoryCombo \_ 控制項會依字母順序顯示所有可用的磁片區，以及目前路徑的階層式步驟。 如果選取的路徑包含任何不存在的資料夾，則會以不同的圖示顯示這些檔案。 您可以使用與 [RemovableVolume](removablevolume-control-attribute.md)、 [FixedVolume](fixedvolume-control-attribute.md)、 [RemoteVolume](remotevolume-control-attribute.md)、 [CDROMVolume](cdromvolume-control-attribute.md)、 [RAMDiskVolume](ramdiskvolume-control-attribute.md)和 [FloppyVolume](floppyvolume-control-attribute.md) 控制項相關聯的位來指定所顯示的磁片區類型。

PathEdit、DirectoryCombo 和 DirectoryList 控制項都與相同的字串值屬性相關聯。 該屬性是使用者選取的路徑。 在 [控制資料表](control-table.md)的屬性資料行中輸入屬性的名稱。 這個屬性的初始值必須包含至少一個磁片區和一個子層次。 在 [屬性資料表](property-table.md)的 [值] 資料行中，指定屬性的初始值。

此控制項的設計目的是要用於 [流覽對話方塊](browse-dialog.md) ，以及 [PathEdit](pathedit-control.md) 和 [DirectoryList](directorylist-control.md) 控制項。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                               | 十六進位位                  | Description                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | 這是與控制項相關聯之間接屬性的名稱。 如果已設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 如果設定了間接屬性位，此名稱也會是 [控制資料表](control-table.md)之屬性資料行中所列屬性的值。                                   |
| [位置](position-control-attribute.md)                         |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                        |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | 這是與此控制項相關聯之屬性的名稱。 如果未設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 這個屬性是在 [控制資料表](control-table.md)的屬性資料行中指定。                                                                                                   |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | 此控制項顯示或變更之屬性的目前值。 如果未設定間接屬性位，則這是 PropertyName 的值。 如果已設定間接屬性位，這就是 IndirectPropertyName 的值。 如果屬性變更，控制項就會反映新的值。                                                                                      |
| [Text](text-control-attribute.md)                                 |                                  | 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&style}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制資料表](control-table.md) 中的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項資料表](control-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                        |
| [沉沒](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 以凹陷的3D 外觀顯示控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                         |
| [間接](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | 控制項會在 [控制資料表](control-table.md)的屬性資料行中顯示或變更屬性的值。 控制項會顯示或變更屬性的值，此屬性的識別碼列于控制資料表的屬性資料行中。<br/> 決定是否要間接參考與此控制項相關聯的屬性。<br/>            |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                                         |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                                  |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                                    |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                                     |
| [RemovableVolume](removablevolume-control-attribute.md)           | 0x00010000                       | 控制項清單抽取式磁碟機。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                               |
| [FixedVolume](fixedvolume-control-attribute.md)                   | 0x00020000                       | 控制項清單固定的內部硬碟。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                     |
| [RemoteVolume](remotevolume-control-attribute.md)                 | 0x00040000                       | 控制項清單遠端磁片區。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                                 |
| [CDROMVolume](cdromvolume-control-attribute.md)                   | 0x00080000                       | 控制項清單： cd-rom 磁片區。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                                 |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)               | 0x00100000                       | 控制項列出 RAM 磁碟。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                                      |
| [FloppyVolume](floppyvolume-control-attribute.md)                 | 0x00200000                       | 控制清單磁片磁碟機。 在 [控制項資料表](control-table.md)的 [屬性] 資料行中包含位單字。<br/>                                                                                                                                                                                                                                                  |



 

## <a name="remarks"></a>備註

您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從 COMBOBOX 類別建立這個控制項。 它有 **cbs \_ DROPDOWNLIST**、 **cbs \_ OWNERDRAWFIXED**、 **cbs \_ HASSTRINGS**、 **ws \_ CHILD**、 **ws \_ GROUP**、 **ws \_ TABSTOP** 和 **WS \_ VSCROLL** 樣式。

 

