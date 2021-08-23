---
description: Filename 資料類型是包含檔案名或資料夾的文字字串。
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: 檔案名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d125a1151520fb4d3b885bd815b0a5bf58d2b00ec61581fc7773f1da1bd29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636202"
---
# <a name="filename"></a>檔案名稱

Filename 資料類型是包含檔案名或資料夾的文字字串。 根據預設，檔案名會假設使用簡短的檔案名語法;也就是八個字元的名稱、句號 ( ) 和3個字元的副檔名。 因為可以設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性，或安裝的目標磁片區可能只支援簡短的檔案名，所以一定要提供簡短的檔案名。

若要包含簡短檔案名的長檔名，請使用分隔號將它與短的檔案名分開， (\|) 。

例如，下列兩個字串是有效的：

-   status.txt
-   project ~1.txt\| Project Status.txt

簡短和完整檔案名不得包含下列字元：

-   斜線 (/) 或 (\\) 
-   問號 (？ ) 
-   垂直橫條 (\|) 
-   右角括弧 (>) 
-   左角括弧 (<) 
-   冒號 (:)
-   星號 (\*) 
-   引號 (")

此外，簡短的檔案名不能包含下列字元：

-   加號 (+)
-   逗號 (,)
-   分號 (;)
-   等號 (=) 
-   左方括弧 (\[) 
-   右方括弧 (\]) 

在分隔號之前不允許有空格 (\| 短檔案名/完整檔案名語法的) 分隔符號。 簡短檔案名不能包含空格，雖然可能會有很長的檔案名。 只有當檔案名的完整檔案名開頭為空格時，才可以在分隔符號之後存在空間。 不允許使用完整路徑語法。

> [!Note]  
> [MsiEmbeddedUI](msiembeddedui-table.md)資料表的 FileName 資料行格式類似于 filename 資料類型，不同之處在于 \| 不提供簡短的檔案名/完整檔案名語法的垂直列 () 分隔符號。

 

 

 



