---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player 線上商店，list.csv
- 線上商店、list.csv
- 輸入1個線上商店，list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480784"
---
# <a name="listcsv"></a>list.csv

此檔案包含目錄包含的每個清單專案。 清單可以是曲目、專輯、演出者、流派、subgenres 或廣播的清單;或者也可以是其他清單的清單。 每個清單專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。




| 欄位 | 必要 | 格式 | 描述 | 
|-------|----------|--------|-------------|
| ListID | 是 | 非負整數。 | 清單識別碼，在 list.csv 中是唯一的。 必須為非負數且小於 2 ^ 32。<strong>在樹狀檢視控制項中顯示清單節點：</strong> 如果 ListID 為0、1、2、3、4、5、6或7，則清單會在您的線上商店的樹狀檢視控制項中，顯示為您的線上商店最上層節點下的自訂節點。 自訂節點會出現在線上商店最上層節點下的標準節點之前，並依 ListID 以遞增順序放置。 例如，如果有三個自訂節點（Listid 為1、3和5），則會在線上商店的最上層節點下顯示第一、第二和第三個節點。<br /> | 
| >listtitle | 否 | Unicode 字串。範例：十大點擊數<br /> | 清單標題。 | 
| ListSubtitle | 否 | Unicode 字串 | 列出替代標題，顯示在磚視圖的第二行中。 | 
| ListDescription | 是 | Unicode 字串 | 列出在 [屬性頁]) 中顯示的易記顯示文字 (。 | 
| Linked_ItemType | 是 | Unicode 字串。格式： [T|P|A|L|G|S|桌上型電腦主機板<br /> 範例： T<br /> | 指出連結專案的型別。<ul><li>T = 追蹤</li><li>P = 執行者</li><li>A = 專輯</li><li>L = 清單</li><li>G = 內容類型</li><li>S = Subgenre</li><li>R = 選項按鈕</li></ul> | 
| ListPrice | 是 | Unicode 字串。範例： $9.99<br /> | 清單的價格。 應包含貨幣符號。零表示清單是免費的。 無值表示價格不明。 連字號表示無法購買清單。<br /> | 
| 熱門程度 | 是 | 整數或十進位值。範例：1259。3<br /> | 指出此清單出現在其他清單中的熱門等級。 如果不適用，則可以為零。 | 
| IsRecentlyAdded | 是 | 布林值。格式： [0|1]<br /> 範例：0<br /> | 指出最近是否加入清單。 | 
| IsFeatured | 是 | 布林值。格式： [0|1]<br /> 範例：0<br /> | 指出清單是否為精選。 可以用來決定排序次序。 | 
| EditorialGlyph | 是 | 非負整數。 應為0。 | 未在此版本中使用。 應為0。 | 
| ViewType | 是 | Unicode 字串。 格式： [I|T|R|L|O）範例： T<br /> | 表示要用於清單的檢視類型。<ul><li>I = 圖示</li><li>T = 磚</li><li>R = 報表</li><li>L = 清單</li><li>O = 已排序清單</li></ul> | 
| ViewImageSize | 是 | 非負整數。範例：180<br /> | 顯示清單影像的大小。 如果為0，則會自動決定大小。 | 
| GroupBy | 是 | Unicode 字串。格式： [-|P|A|C|R|D<br /> 範例： P<br /> | 指出用來將清單中的專案分組的欄位。<ul><li>-= 自動</li><li>P = 執行者</li><li>A = 專輯</li><li>C = Composer</li><li>R = 評等</li><li>D = 日期</li></ul> | 
| ListItemsAreDynamic | 是 | 布林值。 可以是0或1。 | 指出是否動態產生清單。 動態清單在 listitem.csv 中沒有專案。 如果清單標示為動態，則其專案會由 <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner：： GetListContents 提供。</a> | 




 

 

 





