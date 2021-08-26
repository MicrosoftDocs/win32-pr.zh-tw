---
description: 此控制項可讓使用者變更功能資料表中所列功能的選取狀態。
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: SelectionTree 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894a7d90829172c29a6f1df1ffc4139cc0bf6c540bd49193c3cc2f3a396891ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040348"
---
# <a name="selectiontree-control"></a>SelectionTree 控制項

此控制項可讓使用者變更 [功能資料表](feature-table.md)中所列功能的選取狀態。 控制項與字串值屬性相關聯，使用者可透過 [流覽對話方塊](browse-dialog.md)來設定此屬性。 您可以在 [控制資料表](control-table.md)的屬性資料行中輸入屬性的名稱，以便將控制項與屬性產生關聯。

SelectionTree 控制項會自動在 Windows XP 或舊版作業系統上發佈下列 [控制項事件](control-events.md) 。 當選取的專案從一個節點變更為另一個節點時，SelectionTree 控制項會發佈這些事件。 如果選取樹狀目錄沒有任何節點，控制項會發佈這些事件，並清除訂閱事件的控制項內容。 這些事件不需要列在 [ControlEvent 資料表](controlevent-table.md)中。



| 控制項事件                                                 | 描述                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | 從描述反白顯示專案的 [UIText 資料表](uitext-table.md) 發行字串。      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | 產生流覽對話方塊，用來修改反白專案的路徑。                     |
| [SelectionDescription](selectiondescription-controlevent.md) | 從描述反白顯示專案的 [功能表](feature-table.md) 發佈字串。    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | 刪除描述性文字，或停用過時專案的按鈕。                          |
| [SelectionPath](selectionpath-controlevent.md)               | 發佈反白顯示專案的路徑。                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | 發佈是否有與目前選取的功能相關聯的選取路徑。 |
| [SelectionSize](selectionsize-controlevent.md)               | 發佈反白顯示專案的大小。                                                        |



 

從 Windows Server 2003 系統開始，SelectionTree 控制項會發行上表中的所有事件，此外也會發行 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 或 [SetProperty ControlEvent](setproperty-controlevent.md)。 您必須將記錄新增至 [ControlEvent 資料表](controlevent-table.md) ，才能發行 Dataadapter.doaction 或 SetProperty 事件記錄。



| 控制項事件                               | 描述                                        |
|---------------------------------------------|----------------------------------------------------|
| [Dataadapter.doaction](doaction-controlevent.md)       | 通知安裝程式執行自訂動作。 |
| [SetProperty](setproperty-controlevent.md) | 將屬性設定為新的值。                    |



 

從 Windows Installer 版本3.0 開始，SelectionTree 控制項會發行一個事件，以執行[ControlEvent 資料表](controlevent-table.md)中所列的[自訂動作](custom-actions.md)。 SelectionTree 控制項會在控制項中的特徵選取變更時，或每次針對目前功能選擇不同的選取狀態時，發佈此事件。 每次發行事件時都會執行自訂動作。 SelectionTree 控制項會藉由設定下列屬性的值，將資訊傳送至自訂動作。 當關閉 SelectionTree 控制項時，所有這些屬性都會清除。

**Windows Installer 2.0：** 不支援。 SelectionTree 控制項不會發行事件，也不會設定下列屬性。



| 屬性                                | 描述                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | 在 [功能資料表](feature-table.md)的 [功能] 欄位中，選取的功能名稱。                                                                      |
| MsiSelectionTreeSelectedAction          | 選取的功能的安裝動作狀態。 此值可能是 INSTALLSTATE 不 \_ 存在、INSTALLSTATE \_ LOCAL、INSTALLSTATE \_ SOURCE 或 INSTALLSTATE \_ 公告。 |
| MsiSelectonTreeChildrenCount            | 直接子節點的數目。                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | INSTALLSTATE \_ 本機、INSTALLSTATE \_ 來源或 INSTALLSTATE 公告的直接子節點數目 \_ 。                                                    |
| MsiSelectionTreeSelectedCost            | 安裝所選功能的成本（單位為512個位元組）。                                                                                                   |
| MsiSelectionTreeChildrenCost            | 安裝所有子功能的成本，單位為512個位元組。                                                                                              |
| MsiSelectionTreeSelectedPath            | 所選功能的安裝路徑。 只有在功能安裝為 INSTALLSTATE LOCAL 時才會定義 \_ 。                                       |



 

> [!Note]
>
> SelectionTree 控制項絕不會顯示 [控制項資料表](control-table.md) 之文字欄位的內容。 相反地，這個欄位會指定控制項顯示的文字樣式，並包含螢幕審核公用程式所使用之控制項的描述。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。 下列資訊是由螢幕審核公用程式讀取，作為控制項的描述。 請參閱 [協助工具](accessibility.md)。

 

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                                               | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | 與控制項相關聯之間接屬性的名稱。 如果已設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 如果設定了間接屬性位，此名稱也會是 [控制資料表](control-table.md)之屬性資料行中所列屬性的值。                                    |
| [位置](position-control-attribute.md)                         |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | 與此控制項相關聯之屬性的名稱。 如果未設定間接屬性位，控制項會顯示或變更具有這個名稱的屬性值。 這個屬性是在 [控制資料表](control-table.md)的屬性資料行中指定。                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | 此控制項顯示或變更之屬性的目前值。 如果未設定間接屬性位，則這是 PropertyName 的值。 如果已設定間接屬性位，這就是 IndirectPropertyName 的值。 如果屬性變更，控制項就會反映新的值。                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | 根據在 [控制項資料表](control-table.md)的文字資料行中輸入的文字，在螢幕助讀程式中顯示文字。 請參閱 [協助工具](accessibility.md)。                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制資料表](control-table.md) 中的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | 控制項處於停用狀態。 控制項處於已啟用狀態。<br/> 在 [控制項](control-table.md) 的 [屬性] 資料行中的位字組中包含這個位，以在建立時啟用控制項。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來啟用或停用控制項。<br/>                                   |
| [沉沒](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 以凹陷、3D、外觀顯示控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                             |
| [間接](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | 控制項會在 [控制資料表](control-table.md)的屬性資料行中顯示或變更屬性的值。 控制項會顯示或變更屬性的值，此屬性的識別碼列于控制資料表的屬性資料行中。<br/> 決定是否要間接參考與此控制項相關聯的屬性。<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | 控制項中的文字靠左對齊。 控制項中的文字靠右對齊。<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | 捲軸位於控制項的右側。 捲軸位於控制項的左邊。<br/>                                                                                                                                                                                                                                         |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | 將此值設定為 [RTLRO](rtlro-control-attribute.md)、 [RightAligned](rightaligned-control-attribute.md)和 [LeftScroll](leftscroll-control-attribute.md) 屬性的組合。                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

您可以使用 CreateWindowEx 函數，從 WC \_ TREEVIEW 類別建立這個控制項[](/windows/win32/api/winuser/nf-winuser-createwindowexa) 。 它有 **WS \_ 框線**、 **電視 \_ HASLINES**、 **電視 \_ HASBUTTONS**、 **電視 \_ LINESATROOT**、 **電視 \_ DISABLEDRAGDROP**、 **電視 \_ SHOWSELALWAYS**、 **ws \_ CHILD**、 **WS \_ TABSTOP** 和 **ws \_ GROUP** 樣式。

只有在已呼叫 [CostInitialize 動作](costinitialize-action.md) 和 [CostFinalize 動作](costfinalize-action.md) 時，才會填入選取樹狀目錄。

[UIText 資料表](uitext-table.md)中的下列字串與此控制項相關。



| 詞彙                                                                                                         | 描述                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | 針對處於「未存在」狀態的專案顯示的路徑。<br/> |



 

下列六個字串是用來顯示所選子系的數目，以及與反白顯示專案相關聯的大小：

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

下列字串是用來顯示快顯功能表中專案的可用選項選項：

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

下列字串會用來說明 [SelectionDescription](selectiondescription-controlevent.md) ControlEvent 中的目前選取專案。

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

下列四個當地語系化字串用於格式化檔案的大小：

-   位元組
-   KB
-   MB
-   GB

 

 
