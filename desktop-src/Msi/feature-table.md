---
description: 功能資料表會定義功能的邏輯樹狀結構，並包含下表所示的資料行。
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: 功能資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dcf9177c44f407876cbe339925ca4524034a1335393161bb40310d60c158ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251758"
---
# <a name="feature-table"></a>功能資料表

功能資料表會定義功能的邏輯樹狀結構，並包含下表所示的資料行。



| Column          | 類型                         | 答案 | Nullable |
|-----------------|------------------------------|-----|----------|
| 功能         | [識別碼](identifier.md) | Y   | N        |
| 功能 \_ 父系 | [識別碼](identifier.md) | N   | Y        |
| Title           | [Text](text.md)             | N   | Y        |
| 描述     | [Text](text.md)             | N   | Y        |
| 顯示         | [整數](integer.md)       | N   | Y        |
| 層級           | [整數](integer.md)       | N   | N        |
| 目錄\_     | [識別碼](identifier.md) | N   | Y        |
| 屬性      | [整數](integer.md)       | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>特徵
</dt> <dd>

用來識別特定功能記錄的主要索引鍵。 此欄位中的值不得超過最大長度38個字元。

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>功能 \_ 父系
</dt> <dd>

相同資料表中父記錄的選擇性索引鍵。

指向特徵資料行的索引鍵。 如果未選取父項功能，則不會安裝這項功能。 此欄位中的 null 值表示這項功能沒有父代，而且是根項目。 功能 \_ 父資料行不能等於相同記錄的特徵資料行。

> [!Note]  
> 任何功能的最大深度為16。 如果有超過此最大深度的功能，則會產生 [錯誤 2701](windows-installer-error-messages.md) 。

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>標題
</dt> <dd>

識別功能的簡短文字字串。

這個字串會由 [[選取範圍] 對話方塊](selection-dialog.md)的 [ [SelectionTree] 控制項](selectiontree-control.md)列為專案。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

描述功能的較長文字字串。

此可當地語系化的字串會由 [[選取範圍] 對話方塊](selection-dialog.md)的[文字控制項](text-control.md)顯示。

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>顯示
</dt> <dd>

此欄位中的數位會指定在使用者介面中顯示功能的順序。

此值也會決定功能一開始是展開還是折迭。 如果值為 null 或 0 (零) ，則不會顯示記錄。

-   如果值為奇數，則會先展開功能節點。
-   如果值為偶數，則會一開始折迭功能節點。

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>水準
</dt> <dd>

這項功能的初始安裝層級。 處理 [條件資料表](condition-table.md) 可以修改層級值。

安裝層級 0 (零) 會停用該專案並防止其顯示。 安裝層級為 0 (零) 的功能不會在安裝期間安裝，包括系統管理安裝。 如需詳細資訊，請參閱本主題的「備註」一節中的「安裝層級」資訊。

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_
</dt> <dd>

目錄資料 \_ 行指定可由 [選取專案對話方塊](selection-dialog.md)設定的目錄名稱。

因為此欄位是 [目錄資料表](directory-table.md)中的索引鍵，所以指定的目錄必須列在目錄資料表的第一個資料行中。 您必須在此資料行中輸入 [公用屬性](public-properties.md)，才能設定目錄，並在 [[選取] 對話方塊](selection-dialog.md)中顯示 **[流覽]** 按鈕。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

未安裝之功能的遠端執行選項，以及未使用下列任何屬性進行任何功能狀態要求的功能。

-   [**ADDLOCAL 屬性**](addlocal.md)
-   [**ADDSOURCE 屬性**](addsource.md)
-   [**ADDDEFAULT 屬性**](adddefault.md)
-   [**COMPADDLOCAL 屬性**](compaddlocal.md)
-   [**COMPADDSOURCE 屬性**](compaddsource.md)
-   [**FILEADDLOCAL 屬性**](fileaddlocal.md)
-   [**FILEADDSOURCE 屬性**](fileaddsource.md)
-   [**移除屬性**](remove.md)
-   [**重新安裝屬性**](reinstall.md)
-   [**公告屬性**](advertise.md)

將指定的位加入此資料行的總值，以包含遠端執行選項。

-   如果這個欄位是空白的，則值預設為 0 (零) msidbFeatureAttributesFavorLocal。
-   如果功能安裝層級為 0 (零) 或大於或等於目前的安裝層級，則不會在功能狀態中進行任何變更。



| 名稱                                         | Decimal | 十六進位 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | 這項功能未標示為從來源安裝的元件會安裝在本機。 由兩個或多個功能所共用的元件，其中有些功能是設定為 msidbFeatureAttributesFavorLocal，而某些是設定為 msidbFeatureAttributesFavorSource，則會安裝在本機。 [元件資料表](component-table.md)中標記為 msidbComponentAttributesSourceOnly 的元件一律會從來源 CD/伺服器執行。 Bits msidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 會使用「 [**公告」屬性**](advertise.md)未列出的功能。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | 這項功能未標示為本機安裝的元件，會安裝成從來源 CD-ROM 或伺服器執行。 由兩個或多個功能所共用的元件，其中有些功能是設定為 msidbFeatureAttributesFavorLocal，而某些是設定為 msidbFeatureAttributesFavorSource，則會安裝在本機執行。 [元件資料表](component-table.md)中標記為 msidbComponentAttributesLocalOnly 的元件一律會安裝在本機。 Bits msidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 會使用「 [**公告」屬性**](advertise.md)未列出的功能。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | 設定此屬性和功能的狀態，與功能父項的狀態相同。 如果功能位於功能樹狀目錄的根目錄，則無法使用此選項。 省略這個屬性，並根據 msidbFeatureAttributesDisallowAdvertise 和 msidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 來決定功能狀態。<br/> 為了確保子功能的狀態一律會遵循其父項的狀態，即使子系和父系最初設定為不存在 SelectionTree 控制項中，您也必須在子功能的屬性中包含 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent。<br/> 請注意，如果您在沒有設定 msidbFeatureAttributesUIDisallowAbsent 的情況下設定 msidbFeatureAttributesFollowParent，安裝程式就無法強制子功能不存在的狀態。 在此情況下，只有當子系設定為不存在的專案時，子功能才會符合父系的安裝狀態。<br/> 設定 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent，以確保子功能遵循父功能的狀態。<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | 設定此屬性，並將功能狀態設為「通告」。 如果功能是由 [**ADDDEFAULT 屬性**](adddefault.md) 所列出，則會忽略這個位，而且會根據 MsidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 來決定功能狀態。 省略這個屬性，並根據 msidbFeatureAttributesDisallowAdvertise 和 msidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 來決定功能狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | 請注意，這個位只適用于 [ [**公告] 屬性**](advertise.md)所列出的功能。 設定此屬性以防止此功能被公告。<br/> 設定此屬性，而且如果列出的功能不是父系或子系，則會根據 msidbFeatureAttributesFavorLocal 和 msidbFeatureAttributesFavorSource 安裝該功能。<br/> 針對所列出功能的父系設定此屬性，並安裝父代。<br/> 為所列出功能的子系設定此屬性，但子系的狀態不存在。<br/> 省略這個屬性，如果列出的功能不是父項或子系，則會公告功能狀態。<br/> 省略這個屬性，如果列出的功能是父系或子系，則這兩個功能的狀態會是 [公告]。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | 設定此屬性，而且使用者介面不會顯示將功能狀態變更為「不存在」的選項。 無論功能是否顯示在 UI 中，設定此屬性都會強制功能安裝狀態。 省略這個屬性，使用者介面會顯示一個選項，將功能狀態變更為「不存在」。<br/> 設定 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent，以確保子功能遵循父功能的狀態。<br/> 設定此屬性不只會影響 UI，同時也會在 UI 中顯示功能是否可見時，強制功能安裝狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | 如果作業系統 shell 不支援 Windows Installer 描述元，請設定此屬性，並停用該功能的廣告。 省略這個屬性，就不會停用廣告。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

有些屬性彼此獨立。 嘗試在相同功能上同時設定這些屬性，會導致安裝套件無法通過 [**套件驗證**](package-validation.md)。

-   請勿使用 msidbFeatureAttributesFavorAdvertise 搭配 msidbFeatureAttributesDisallowAdvertise。
-   請勿搭配使用 msidbFeatureAttributesNoUnsupportedAdvertise 與 msidbFeatureAttributesDisallowAdvertise。
-   請勿使用 msidbFeatureAttributesFollowParent 搭配 msidbFeatureAttributesFavorSource。
-   請注意，msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesFavorLocal 值是互斥的。 如果使用 msidbFeatureAttributesFollowParent 值，則會假設 msidbFeatureAttributesFavorLocal 值不存在。

</dd> </dl>

請注意，如果安裝了子功能，也會一併安裝其父功能。 如果已安裝父功能，除非已設定其 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent 屬性，否則不一定會安裝其子功能。 安裝父項和子功能的階層式關聯性，也可用於使用命令列屬性的 GUI 安裝和安裝。

## <a name="remarks"></a>備註

當此資料表載入至記憶體時，會將數個額外的暫存資料行新增至記憶體中，以供成本和使用者介面的計算使用 (UI) 選取。

元件可在兩個或多個功能或應用程式之間共用。 如果有兩個以上的功能參考相同的元件，則在選取任何相關聯的功能時，就會選取該元件來進行安裝。 這也可能是移除父項功能時不會卸載子功能的原因。 如果子功能是由其他功能或應用程式所需的元件所組成，則 Windows Installer 不會移除子功能。

如需詳細資訊，請參閱 [控制特徵選取狀態](controlling-feature-selection-states.md)。

安裝層級：

-   任何安裝都有一個定義的安裝層級，也就是從1到32767的整數值。 初始值取決於 [屬性工作表](property-table.md)中設定的 [**INSTALLLEVEL 屬性**](installlevel.md)。
-   只有當功能層級值小於或等於目前的安裝層級時，才會安裝功能。 您可以撰寫 UI，如此一來，當安裝程式初始化時，安裝程式便可讓使用者修改功能資料表中任何功能的安裝層級。 例如，作者可以定義表示特定安裝選項的安裝層級值，例如 [ **自訂**]、[ **一般**] 或 [ **最小**]，然後建立使用 [SetInstallLevel 事件](setinstalllevel-controlevent.md) 的對話方塊，讓使用者可以選取其中一個狀態。
-   根據使用者選取的狀態，對話方塊會將 [安裝等級] 屬性設定為對應的值。 如果作者指派 **典型** 的100層級，而使用者選取 [ **一般**]，則只會安裝層級為100或更低的功能。 此外， **自訂** 選項可能會導致包含 [SelectionTree 控制項](selectiontree-control.md)的另一個對話方塊。 然後，SelectionTree 控制項可讓使用者個別變更是否已安裝每項功能。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




