---
description: 資料夾深度述詞會指定路徑，以及是否要執行深層或淺層遍歷，來控制搜尋的範圍。
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: 範圍和目錄述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112432"
---
# <a name="scope-and-directory-predicates"></a>範圍和目錄述詞

資料夾深度述詞會指定路徑，以及是否要執行深層或淺層遍歷，來控制搜尋的範圍。 以下顯示資料夾深度述詞的語法：


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



述詞後面接著等號。 路徑 exclosed 以單引號括住，且開頭必須是通訊協定和冒號 (例如，、 `file:` `mapi:` 或 `csc:`) 。 範圍述詞會執行路徑的深度遍歷（包括所有子資料夾），而目錄述詞只會執行指定之資料夾的淺層遍歷。 如同其他結構化查詢語言 (SQL)  (SQL) 限制，您可以在單一查詢中指定一個以上的資料夾深度限制。

若要查詢遠端電腦的本機目錄，請在類別目錄和目錄子句中的遠端電腦上，將電腦名稱稱包含在目錄之前，以及通用命名慣例 (UNC) 路徑。

## <a name="examples"></a>範例


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



第一個範圍範例會搜尋 C： \\ Files \\ Reports 資料夾及其所有子資料夾。 目錄範例只會搜尋根資料夾 C： \\ Files \\ 報表。

> [!Note]  
> 檔案系統反斜線 (\\) 會成為 URL 樣式的斜線， (有時也稱為正斜線)  (/) 。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FROM 子句](-search-sql-from.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> </dl>

 

 



