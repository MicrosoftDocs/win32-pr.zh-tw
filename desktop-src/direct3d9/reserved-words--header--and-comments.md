---
description: 下表顯示已保留且不得使用的單字。
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: 保留字、標頭和批註
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f583084b3faa4777a5fe6031cc247fdb99c27cc1fb23c6a5676e60afe00aba20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044277"
---
# <a name="reserved-words-header-and-comments"></a>保留字、標頭和批註

下表顯示已保留且不得使用的單字。

| 保留字 | 保留字 | 保留字|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| 二進位 \_ 資源 | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

可變長度的標頭是強制的，且必須在資料流程的開頭。 標頭包含下列資料。



| 類型           | 必要 | 大小 (以位元組為單位) | 值 | 描述                  |
|----------------|----------|-----------------|-------|------------------------------|
| 魔術數位   | x        | 4               | xof   |                              |
| 版本號碼 | x        | 2               | 03    | 主要版本3              |
|                |          |                 | 03    | 次要版本3              |
| 格式類型    | x        | 4               | txt   | 文字檔                    |
|                |          |                 | bin   | 二進位檔案                  |
|                |          |                 | tzip  | MSZip 壓縮的文字檔   |
|                |          |                 | bzip  | MSZip 壓縮的二進位檔案 |
| 浮點數大小     | x        | 0064            |       | 64位浮點數                |
|                | x        | "0032"          |       | 32位浮點數                |



 

資料表中的值會以引號分隔，以呼叫每個值中的字元數。 具有4個位元組的那些字元包含四個字元，其中2個位元組的字元包含兩個字元。

批註只適用于文字檔。 批註可以出現在資料流程中的任何位置。 批註的開頭是 c + + 樣式的雙斜線 (//) ，或 () 的井字型大小 \# 。 批註會執行到下一個新行。 下列範例會顯示有效的批註。


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字編碼方式](text-encoding.md)
</dt> </dl>

 

 



