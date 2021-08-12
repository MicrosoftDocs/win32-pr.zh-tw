---
description: Microsoft 安裝程式可讓使用者安裝和移除稱為 Windows Installer 功能的應用程式功能區塊。
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: 指定功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8356020ce79881948b0886cfb83f634789f1ec9cfa55e7b150eb275ea1b81fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624692"
---
# <a name="specifying-features"></a>指定功能

Microsoft 安裝程式可讓使用者安裝和移除稱為[Windows Installer 功能](windows-installer-features.md)的應用程式功能區塊。 在本節中，您會將有關記事本範例可用功能的資訊新增至安裝資料庫。 如需詳細資訊，請參閱 [核心資料表群組](core-tables-group.md) 和 [元件和功能](components-and-features.md)。

記事本範例會在父項和子功能的階層中安裝功能。 在下列清單中，子功能會相對於其父項功能進行縮排。 這些功能應該會以這個順序顯示在使用者介面 (UI) 的 [SelectionTree 控制項](selectiontree-control.md) 中。

[記事本]

-   讀我檔案
-   說明

門

-   一月
    -   NewYears

運動項目

-   棒球
-   足球

藝術

-   演唱會
-   舞蹈

使用資料庫編輯器開啟 MNP2000.msi，並將下列資料輸入空白的 [功能資料表](feature-table.md)中。



| 功能  | 功能 \_ 父系 | Title         | 描述                | 顯示 | 層級 | 目錄\_ | 屬性 |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| 藝術     |                 | 藝術          | 以紅色公園為活動的藝術。   | 20      | 3     | NOTEPADDIR  | 0          |
| 棒球 | 運動項目           | 棒球      | 棒球             | 17      | 3     | SPORTDIR    | 32         |
| 演唱會  | 藝術            | 演唱會       | 紅色公園的協同活動 | 21      | 3     | ARTSDIR     | 2          |
| 舞蹈    | 藝術            | 舞蹈         | Dance 位於紅色公園的事件   | 23      | 3     | ARTSDIR     | 2          |
| 足球 | 運動項目           | 足球      | 足球遊戲             | 19      | 3     | SPORTDIR    | 2          |
| 門     |                 | 門          | Red 公園的招生      | 6       | 3     | NOTEPADDIR  | 0          |
| 說明     | [記事本]         | 說明          | 說明檔。                 | 5       | 3     | NOTEPADDIR  | 1          |
| 一月  | 門            | 一月       | 1月招生         | 10      | 3     | MONDIR      | 2          |
| NewYears | 一月         | 新的年份日 | 新的年份招生   | 11      | 3     | HOLDIR      | 2          |
| [記事本]  |                 | [記事本]       | 記事本編輯 器             | 1       | 3     | NOTEPADDIR  | 0          |
| 讀我檔案   | [記事本]         | 讀我檔案        | 讀我檔案                | 3       | 3     | NOTEPADDIR  | 0          |
| 運動項目    |                 | 運動事件  | 在紅色公園運動事件   | 14      | 3     | NOTEPADDIR  | 0          |



 

[繼續](specifying-feature-component-relationships.md)

 

 



