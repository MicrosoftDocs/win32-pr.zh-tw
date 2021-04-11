---
description: 本章節描述 MsiEvaluateCondition 函數和動作順序資料表所使用之條件陳述式的語法。 如需詳細資訊，請參閱，條件陳述式語法的範例。
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: 條件陳述式語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848936"
---
# <a name="conditional-statement-syntax"></a>條件陳述式語法

本章節描述 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數和動作 [順序資料表](using-a-sequence-table.md)所使用之條件陳述式的語法。 如需詳細資訊，請參閱， [條件陳述式語法的範例](examples-of-conditional-statement-syntax.md)。

## <a name="summary-of-conditional-statement-syntax"></a>條件陳述式語法的摘要

此資料表和下列清單摘要說明在條件運算式中使用的語法。



| 項目                | Syntax                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | 符號 \| 常值 \| 整數                                                                                    |
| 比較-運算子 | < \| > \| <= \| >= \| = \| <>                                                                 |
| 詞彙                | 值 \| 比較-運算子值 \| ( 運算式 ) \|                                                    |
| 布林值因數      | 詞彙 \| **不** 是詞彙                                                                                            |
| 布林值詞彙        | 布林因數 \| 布林因數 **和** 詞彙                                                                   |
| 運算式          | 布林詞彙 \| 布林值詞彙 **或** 運算式                                                                  |
| 符號              | 屬性 \| % 環境-變數 \| $component-動作 \| ？元件狀態 \| &功能-動作 \| ！功能狀態 |



 

-   符號名稱和值會區分大小寫。
-   環境變數名稱不區分大小寫。
-   常值文字必須用引號括住 ( "text" ) 。
    > [!Note]  
    > 包含引號的常值文字不能用在條件陳述式中，因為常值文字內沒有引號的逸出字元。 若要對包含引號的常值文字進行比較，常值文字應放在屬性中。 例如，若要確認 SERVERNAME 屬性不包含任何引號，請在 [屬性工作表](property-table.md) 中定義名為引號的屬性，其值為 "，並將條件變更為非 SERVERNAME><引號。

     

-   不存在的屬性值會被視為空字串。
-   不支援浮點數值。
-   運算子和優先順序與基本和 SQL 語言中的相同。
-   不支援算術運算子。
-   括弧可以用來覆寫運算子優先順序。
-   運算子不區分大小寫。
-   針對字串比較，在運算子前面加上波狀符號 "~"，會執行不區分大小寫的比較。
-   具有無法轉換成整數之字串或屬性值的整數比較，一律為 **msiEvaluateConditionFalse**，但比較運算子 "<>" 除外，後者會傳回 **msiEvaluateConditionTrue**。

## <a name="access-prefixes"></a>存取首碼

下表顯示用來存取各種系統和安裝程式資訊以用於條件運算式的前置詞。



| 符號類型          | 前置詞 | 值                                                     |
|----------------------|--------|-----------------------------------------------------------|
| 安裝程式屬性   | (無) | 屬性 ([屬性](property-table.md) 的值) 資料表。 |
| 環境變數 | %      | 環境變數的值。                            |
| 元件資料表索引鍵  | $      | 元件的動作狀態。                            |
| 元件資料表索引鍵  | ?      | 元件的已安裝狀態。                         |
| 功能資料表索引鍵    | &      | 功能的動作狀態。                              |
| 功能資料表索引鍵    | !      | 功能的已安裝狀態。                           |



 

## <a name="logical-operators"></a>邏輯運算子

下表顯示條件運算式中的邏輯運算子（依高至低優先順序排列）。



| 運算子 | 意義                                                 |
|----------|---------------------------------------------------------|
| Not      | 前置詞一元運算子;反轉下列詞彙的狀態。 |
| And      | 如果這兩個詞彙都是 TRUE，則為 TRUE。                            |
| Or       | 如果任一個或兩個詞彙都是 TRUE，則為 TRUE。                  |
| Xor      | 如果兩個詞彙都不是 TRUE，則為 TRUE。             |
| Eqv      | 如果這兩個詞彙都為 TRUE 或兩個詞彙都為 FALSE，則為 TRUE。    |
| 進出口      | 如果 left 詞彙為 FALSE 或 right 詞彙為 TRUE，則為 TRUE。       |



 

## <a name="comparative-operators"></a>比較運算子

下表顯示條件運算式中使用的比較運算子。 這些比較運算子只能在兩個值之間進行。



| 運算子 | 意義                                                     |
|----------|-------------------------------------------------------------|
| =        | 如果左值等於右邊的值，則為 TRUE。                 |
| <> | 如果左值不等於右值，則為 TRUE。             |
| >     | 如果左值大於右邊的值，則為 TRUE。             |
| >=    | 如果左值大於或等於右值，則為 TRUE。 |
| <     | 如果左值小於右值，則為 TRUE。                |
| <=    | 如果左值小於或等於右值，則為 TRUE。    |



 

## <a name="substring-operators"></a>Substring 運算子

下表顯示條件運算式中使用的子字串運算子。 子字串運算子可能會在兩個字串值之間進行。



| 運算子 | 意義                                           |
|----------|---------------------------------------------------|
| >< | 如果左字串包含正確的字串，則為 TRUE。    |
| << | 如果左字串開頭為右邊的字串，則為 TRUE。 |
| >> | 如果左字串以右字串結尾，則為 TRUE。   |



 

## <a name="bitwise-numeric-operators"></a>位數值運算子

下表顯示條件運算式中的位數值運算子。 這些運算子可能會在兩個整數值之間發生。



| 運算子 | 意義                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | 位 AND，如果左和右整數的任何位都是共通的，則為 TRUE。    |
| << | 如果左整數的高16位等於右邊整數，則為 True。 |
| >> | 如果左整數的低16位等於右邊整數，則為 True。  |



 

## <a name="feature-and-component-state-values"></a>功能和元件狀態值

下表顯示使用功能和元件運算子符號的有效位置。



| 運算元 <state> | 此語法有效的位置                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component-動作      | 在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。 |
| &功能-動作        | 在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。 |
| ！功能-狀態         | 在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。 |
| ？元件-狀態       | 在 [條件](condition-table.md) 資料表中，以及在 [順序](using-a-sequence-table.md) 資料表中，于 [CostFinalize](costfinalize-action.md) 動作之後。 |



 

下表顯示條件運算式中使用的功能和元件狀態值。 在呼叫 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) （直接或透過 [CostFinalize](costfinalize-action.md) 動作）之前，不會設定這些狀態。



| 狀態                    | 值 | 意義                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ 不明    | -1    | 不需要在功能或元件上採取任何動作。              |
| INSTALLSTATE \_ 公告 | 1     | 宣告的功能。 元件無法使用此狀態。 |
| INSTALLSTATE 不 \_ 存在     | 2     | 功能或元件不存在。                            |
| INSTALLSTATE \_ 本機      | 3     | 本機電腦上的功能或元件。                     |
| INSTALLSTATE \_ 來源     | 4     | 從來源執行的功能或元件。                       |



 

例如，只有當 MyFeature 正在將其目前的狀態變更為本機電腦上所安裝的狀態時，才會評估為 True 的條件運算式 "&MyFeature = 3"，INSTALLSTATE \_ local。

請注意，您不應該相依于 $Component 1 = 3 的條件，以檢查 Component1 是否在本機安裝在電腦上。 如果有多個產品安裝 Component1，這可能會失敗。 由 Product1 在本機安裝 Component1 之後，安裝程式會在安裝 Product2 時，將條件 $Component 1 = 3 評估為 False。 這是因為安裝程式會使用元件的金鑰路徑來判斷元件的版本，並在其版本大於或等於已安裝的元件時，將元件標記為安裝。

請注意，安裝程式將不會直接比較準則語句中的 [版本](version.md) 資料類型。 例如，您無法在條件陳述式中使用比較運算子來比較版本，例如 "01.10" 和 "1.010"。 相反地，請使用有效的方法來搜尋版本，例如搜尋 [現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)中所述，然後設定屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



