---
description: 將範例 Windows Installer 安裝套件的複本複製 MNP2000.msi，然後重新命名此複製 MNP2000t.msi。
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: 自訂原始資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075038"
---
# <a name="customizing-an-original-database"></a>自訂原始資料庫

將範例 Windows Installer 安裝套件的複本複製 MNP2000.msi，然後重新命名此複製 MNP2000t.msi。 在下列步驟中，您將使用資料庫資料表編輯器（例如，在 SDK 中提供的 Orca）自訂此檔案，或使用另一個資料庫編輯器來自訂此檔案。

在 [記事本] 資料夾中包含與其他原始程式檔 Phone.txt 的電話清單新資源檔。



| 檔案      | 描述                             | 來源的路徑                 | 目標路徑                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | 電話清單功能的資源 \_ 。 | C： \\ 範例 \\ 記事本 \\phone.txt | \[ProgramFilesFolder \] \\ Red \_ 公園 \\phone.txt |



 

您可以使用資料庫編輯器，將記錄新增至新檔案之 MNP2000t.msi 的檔案 [資料表](file-table.md) 中。

[FileTable](file-table.md)



| 檔案      | 元件\_ | FileName  | FileSize | 版本 | 語言 | 屬性 | 順序 |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | 電話       | Phone.txt | 1000     |         |          | 0          | 1        |



 

如「 [使用轉換來新增資源](using-transforms-to-add-resources.md)」一節所述，轉換應該將一或多個新元件新增至安裝資料庫，以包含新的電話清單功能。 您可以使用資料庫編輯器，將下列記錄加入 MNP2000t.msi 的 [元件資料表](component-table.md) 中。

應使用唯一的元件識別碼[GUID](guid.md)來識別電話元件。 如果您要重新產生範例，請不要重複使用與下表中相同的元件識別碼 GUID。 相反地，請使用 Guidgen.exe 之類的公用程式來產生新的 GUID。 請確定您使用的 guid 字串與 Windows Installer [guid](guid.md)資料類型一致。

[元件資料表](component-table.md)



| 元件 | ComponentId                            | 目錄\_ | 屬性 | 條件 | Keypath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| 電話     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

您可以使用資料庫編輯器來修改 MNP2000t.msi [功能資料表](feature-table.md) 中的資料。 在閘道功能記錄的 [層級] 資料行中輸入0。 這會停用閘道功能和其子功能，並將這些功能從 UI 中隱藏。 請注意，因為 [屬性工作表](property-table.md)中的 [**INSTALLLEVEL**](installlevel.md)屬性設定為3，所以安裝程式不會安裝層級為0的功能。 為新的電話 \_ 清單功能新增記錄。

[功能資料表](feature-table.md)



| 功能     | 功能 \_ 父系 | 標題         | 描述                | 顯示 | 層級 | 目錄\_ | 屬性 |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| 藝術        |                 | 藝術          | 以紅色公園為活動的藝術。   | 20      | 3     | NOTEPADDIR  | 0          |
| 棒球    | 運動項目           | 棒球      | 棒球             | 17      | 3     | SPORTDIR    | 32         |
| 演唱會     | 藝術            | 演唱會       | 紅色公園的協同活動 | 21      | 3     | ARTSDIR     | 2          |
| 舞蹈       | 藝術            | 舞蹈         | Dance 位於紅色公園的事件   | 23      | 3     | ARTSDIR     | 2          |
| 足球    | 運動項目           | 足球      | 足球遊戲             | 19      | 3     | SPORTDIR    | 2          |
| 門        |                 | 門          | Red 公園的招生      | 6       | 0     | NOTEPADDIR  | 0          |
| 說明        | [記事本]         | 說明          | 說明檔。                 | 5       | 3     | NOTEPADDIR  | 1          |
| 一月     | 門            | 一月       | 1月招生         | 10      | 3     | MONDIR      | 2          |
| NewYears    | 一月         | 新的年份日 | 新的年份招生   | 11      | 3     | HOLDIR      | 2          |
| [記事本]     |                 | [記事本]       | 記事本編輯 器             | 1       | 3     | NOTEPADDIR  | 0          |
| 讀我檔案      | [記事本]         | 讀我檔案        | 讀我檔案                | 3       | 3     | NOTEPADDIR  | 0          |
| 運動項目       |                 | 運動事件  | 在紅色公園運動事件   | 14      | 3     | NOTEPADDIR  | 0          |
| 電話 \_清單 |                 | 電話表    | 電話表                 | 24      | 3     | NOTEPADDIR  | 0          |



 

將下列記錄新增至 MNP2000t.msi 的 [FeatureComponents 資料表](featurecomponents-table.md) 。

[FeatureComponents 資料表](featurecomponents-table.md)



| 特徵\_   | 元件\_ |
|-------------|-------------|
| 電話 \_清單 | 電話       |



 

在[快捷方式資料表](shortcut-table.md)中加入新的記錄，以建立電話清單功能的快捷方式 \_ 。

[快速鍵資料表](shortcut-table.md)



| 快速鍵 | 目錄\_ | 名稱      | 元件\_ | 目標          | 引數 | 描述 | 熱鍵 | 圖示\_ | >iconindex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | 電話       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[繼續](generating-a-customization-transform.md)

 

 



