---
description: 安裝資料庫的登錄資料表和相關資料表會保存應用程式需要在系統登錄中寫入的登錄資訊。
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: 新增登錄資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df31ad20fef317d5d67f7f45a7b877511d4c35b05b1517c529693e787306b44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066408"
---
# <a name="adding-registry-information"></a>新增登錄資訊

安裝資料庫的登錄 [資料表](registry-table.md)和相關資料表會保存應用程式需要在系統登錄中寫入的登錄資訊。 請參閱登錄 [資料表群組](registry-tables-group.md)。 在本節中，您會在記事本範例中新增要在使用者電腦上註冊的資訊。

使用您的資料庫編輯器開啟 MNP2000.msi，並將下列資料輸入空白的登錄資料表中。

[登錄資料表](registry-table.md)



| 登錄       | Root | 按鍵                                 | 名稱             | 值    | 元件\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfCharSet        | \#0      | [記事本]     |
| ClipPrecision  | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfClipPrecision  | \#2      | [記事本]     |
| 行距     | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfFaceName       | FixedSys | [記事本]     |
| 斜體         | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfItalic         | \#0      | [記事本]     |
| Orientation    | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfOrientation    | \#0      | [記事本]     |
| OutPrecision   | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfOutPrecision   | \#1      | [記事本]     |
| PageSettings   | 2    | 軟體 \\ Microsoft \\ 記事本範例 | fSavePageSetting | \#0      | [記事本]     |
| PitchAndFamily | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfPitchAndFamily | \#49     | [記事本]     |
| Dialog      | 2    | 軟體 \\ Microsoft \\ 記事本範例 | iPointSize       | \#120    | [記事本]     |
| 品質        | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfQuality        | \#2      | [記事本]     |
| 帶      | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfStrikeOut      | \#0      | [記事本]     |
| Weight         | 2    | 軟體 \\ Microsoft \\ 記事本範例 | lfWeight         | \#400    | [記事本]     |
| 包裝           | 2    | 軟體 \\ Microsoft \\ 記事本範例 | fWrap            | \#0      | [記事本]     |



 

[繼續](specifying-shortcuts.md)

 

 



