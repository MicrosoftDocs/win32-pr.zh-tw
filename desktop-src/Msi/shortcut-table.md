---
description: 快速鍵表格會保存應用程式在使用者電腦上建立快捷方式所需的資訊。
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: 快速鍵資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628418"
---
# <a name="shortcut-table"></a>快速鍵資料表

快速鍵表格會保存應用程式在使用者電腦上建立快捷方式所需的資訊。

快速鍵資料表具有下列資料行。



| Column                 | 類型                         | 答案 | Nullable |
|------------------------|------------------------------|-----|----------|
| 快速鍵               | [識別碼](identifier.md) | Y   | N        |
| 目錄\_            | [識別碼](identifier.md) | N   | N        |
| 名稱                   | [檔案名稱](filename.md)     | N   | N        |
| 元件\_            | [識別碼](identifier.md) | N   | N        |
| 目標                 | [快速鍵](shortcut.md)     | N   | N        |
| 引數              | [格式 化](formatted.md)   | N   | Y        |
| 描述            | [Text](text.md)             | N   | Y        |
| 熱鍵                 | [整數](integer.md)       | N   | Y        |
| 圖示\_                 | [識別碼](identifier.md) | N   | Y        |
| >iconindex              | [整數](integer.md)       | N   | Y        |
| ShowCmd                | [整數](integer.md)       | N   | Y        |
| WkDir                  | [識別碼](identifier.md) | N   | Y        |
| DisplayResourceDLL     | [格式 化](formatted.md)   | N   | Y        |
| DisplayResourceId      | [整數](integer.md)       | N   | Y        |
| DescriptionResourceDLL | [格式 化](formatted.md)   | N   | Y        |
| DescriptionResourceId  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>快捷方式
</dt> <dd>

此資料表的索引鍵值。

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_
</dt> <dd>

[目錄資料表](directory-table.md)第一個資料行中的外部索引鍵。 此資料行指定建立快捷方式檔案的目錄。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

要建立之快捷方式的可當地語系化名稱。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。 安裝程式會使用此資料行中所指定之元件的安裝狀態，來判斷是否已建立或刪除快捷方式。 此元件必須有有效的金鑰路徑，才能安裝快捷方式。 如果目標資料行包含功能的名稱，快捷方式所啟動的檔案就是此資料行中所列元件的金鑰檔。

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標
</dt> <dd>

快捷方式目標。

若為已公告的快捷方式，這個資料行必須是 [功能資料表](feature-table.md)第一個資料行中的外部索引鍵。 安裝程式會評估目標欄位中的專案做為 [識別碼](identifier.md) ，而專案必須是 [功能資料表](feature-table.md)中的有效外鍵。 在此情況下，快捷方式所啟動的檔案是元件資料行中所列元件的金鑰檔 \_ 。 當快捷方式啟用時，安裝程式會先確認功能中的所有元件都已安裝，然後再啟動此檔案。

若為非公告的快捷方式，安裝程式會將此欄位評估為 [格式化](formatted.md) 字串。 欄位應包含以方括弧括住的屬性識別碼 (\[ \]) ），該識別碼會展開至檔案或快捷方式指向的資料夾中。 如需詳細資訊，請參閱 [CreateShortcuts 動作](createshortcuts-action.md)。

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數
</dt> <dd>

快速鍵的命令列引數。

請注意，[引數] 欄位中的屬性解析有限。 \[  \] 只有在已安裝擁有快捷方式的元件時，如果屬性已經有預期的值，則只能解析此欄位中格式化為屬性的屬性。 例如，若要解析為引數 "MyDoc.doc" 的正確值 \[ \# \] ，相同的進程必須安裝檔案 MyDoc.doc 和擁有快捷方式的元件。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

快速鍵的可當地語系化描述。

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>熱鍵
</dt> <dd>

快速鍵的快速鍵。 低序位位元組包含金鑰的虛擬金鑰程式碼，而高序位位元組包含修飾詞旗標。 此值必須是非負數。 通常建議不要設定此選項，因為此選項的設定可將重複的快速鍵新增至使用者的桌面。 此外，將快速鍵指派給快速鍵的做法，對於使用快速鍵來 [存取協助工具](accessibility.md)的使用者來說可能會有問題。

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_
</dt> <dd>

[圖示資料表](icon-table.md)的第一個資料行的外部索引鍵。

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex
</dt> <dd>

快速鍵的圖示索引。 此值必須是非負數。

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

應用程式視窗的 [顯示] 命令。

您可以使用下列值。 這些值會如針對 Windows API 函數 ShowWindow 所定義。



| 值 | 意義             |
|-------|---------------------|
| 1     | SW \_ SHOWNORMAL      |
| 3     | SW \_ SHOWMAXIMIZED   |
| 7     | SW \_ SHOWMINNOACTIVE |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

屬性的名稱，該屬性具有快捷方式的工作目錄路徑。 值可以使用 Windows 格式參考環境變數，例如% USERPROFILE%。 當安裝程式解析工作目錄以建立快捷方式時，參考會解析為實際的路徑。

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

此欄位包含 [格式化](formatted.md) 的字串值，適用于非語言相關可攜性可執行檔的完整路徑 (LN 檔案) ，其中包含資源設定 (RC Config) 資料。 格式化的字串可以使用 \[ \# filekey \] 慣例。 如果此欄位包含值，則會忽略 [名稱] 資料行。 如果這個欄位是空的，安裝程式會使用 [名稱] 資料行中的值。 當此欄位包含一個值時， **DisplayResourceId** 欄位也必須包含值，否則安裝會失敗。

只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵資料表的資料行，否則會予以忽略。 此資料行適用于 Windows Installer 4.0 之前的版本。

如需有關如何新增快捷方式資料表的快捷方式以搭配 MUI 資源使用的詳細資訊，請參閱 [Mui 快捷方式範例](a-mui-shortcut-example.md)。

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

快速鍵的顯示名稱索引。 此值必須是非負數。 當此欄位包含一個值時， **DisplayResourceDLL** 欄位也必須包含值，否則安裝會失敗。

只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵資料表的資料行，否則會予以忽略。 此資料行適用于 Windows Installer 4.0 之前的版本。

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

此欄位包含 [格式化](formatted.md) 的字串值，適用于非語言相關可攜性可執行檔的完整路徑 (LN 檔案) ，其中包含資源設定 (RC Config) 資料。 格式化的字串可以使用 \[ \# filekey \] 慣例。 如果此欄位包含值，則會忽略 [名稱] 資料行。 如果這個欄位是空的，安裝程式會使用 [描述] 欄中的值。 當此欄位包含一個值時， **DescriptionResourceId** 欄位也必須包含值，否則安裝會失敗。

只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵資料表的資料行，否則會予以忽略。 此資料行適用于 Windows Installer 4.0 之前的版本。

如需有關如何新增快捷方式資料表的快捷方式以搭配 MUI 資源使用的詳細資訊，請參閱 [Mui 快捷方式範例](a-mui-shortcut-example.md)。

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

快速鍵的描述名稱索引。 此值必須是非負數。 當此欄位包含一個值時， **DescriptionResourceDLL** 欄位也必須包含值，否則安裝會失敗。

只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵資料表的資料行，否則會予以忽略。 此資料行適用于 Windows Installer 4.0 之前的版本。

</dd> </dl>

## <a name="remarks"></a>備註

只有在系統的 IShellLink 介面支援安裝程式描述項解析時，啟用功能才會建立公告的快捷方式。 microsoft Windows 2000 和執行 microsoft Internet Explorer 4.01 的系統都支援此功能。 如果不支援，安裝程式會在安裝功能元件時，在本機或從來源執行，建立非公告的快捷方式。

請注意，公告的快捷方式一律指向特定的應用程式，由 [**ProductCode**](productcode.md)識別，且不應在應用程式之間共用。 公告的快捷方式只適用于最近安裝的應用程式，而且會在移除應用程式時移除。

當 [CreateShortcuts 動作](createshortcuts-action.md) 和 [RemoveShortcuts 動作](removeshortcuts-action.md) 執行時，就會參考此資料表。

另請參閱 [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) 屬性。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



