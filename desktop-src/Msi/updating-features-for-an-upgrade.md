---
description: 範例 Windows Installer 升級套件會將新功能新增至原始產品。
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: 更新升級的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985229"
---
# <a name="updating-features-for-an-upgrade"></a>更新升級的功能

範例升級套件會將三項新功能新增至原始產品：

-   籃球是運動功能的新子功能。
-   Opera 是藝術功能的新子功能。
-   紀念堂，這是閘道功能的新子功能。

使用您的資料庫編輯器開啟 MNP2001.msi，並在 [功能資料表](feature-table.md)中輸入下列資料。

[功能資料表](feature-table.md)



| 功能    | 功能 \_ 父系 | 標題         | 描述                | 顯示 | 層級 | 目錄\_ | 屬性 |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| 藝術       |                 | 藝術          | 以紅色公園為活動的藝術。   | 18      | 3     | NOTEPADDIR  | 0          |
| 棒球   | 運動項目           | 棒球      | 棒球             | 17      | 3     | SPORTDIR    | 32         |
| 演唱會    | 藝術            | 演唱會       | 紅色公園的協同活動 | 19      | 3     | ARTSDIR     | 2          |
| 舞蹈      | 藝術            | 舞蹈         | Dance 位於紅色公園的事件   | 21      | 3     | ARTSDIR     | 2          |
| 足球   | 運動項目           | 足球      | 足球遊戲             | 13      | 3     | SPORTDIR    | 2          |
| 門       |                 | 門          | Red 公園的招生      | 6       | 3     | NOTEPADDIR  | 0          |
| Help       | [記事本]         | Help          | 說明檔。                 | 5       | 3     | NOTEPADDIR  | 1          |
| 一月    | 門            | 一月       | 1月招生         | 7       | 3     | MONDIR      | 2          |
| NewYears   | 一月         | 新的年份日 | 新的年份招生   | 9       | 3     | HOLDIR      | 2          |
| [記事本]    |                 | [記事本]       | 記事本編輯器             | 1       | 3     | NOTEPADDIR  | 0          |
| 讀我檔案     | [記事本]         | 讀我檔案        | 讀我檔案                | 3       | 3     | NOTEPADDIR  | 0          |
| 運動項目      |                 | 運動事件  | 在紅色公園運動事件   | 12      | 3     | NOTEPADDIR  | 0          |
| 籃球 | 運動項目           | 籃球    | 籃球遊戲           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | 藝術            | Opera         | Opera 效能         | 23      | 3     | ARTSDIR     | 2          |
| 紀念   | 門            | 紀念堂日  | 紀念堂 Day 招生    | 11      | 3     | HOLDIR      | 2          |



 

使用資料庫編輯器開啟 MNP2001.msi，並將下列資料輸入空白的 [FeatureComponents 資料表](featurecomponents-table.md)中。



| 功能\_  | 元件\_ |
|------------|-------------|
| 棒球   | 棒球    |
| 演唱會    | 演唱會     |
| 舞蹈      | 舞蹈       |
| 足球   | 足球    |
| Help       | Help        |
| 一月    | 一月     |
| NewYears   | NewYears    |
| [記事本]    | [記事本]     |
| 讀我檔案     | [記事本]     |
| 籃球 | 籃球  |
| Opera      | Opera       |
| 紀念   | 紀念    |



 

[繼續](updating-shortcuts-for-an-upgrade.md)

 

 



