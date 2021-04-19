---
description: 本節說明每個記錄相關權杖的記錄格式。 資訊分成下列各節。
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: 權杖記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991612"
---
# <a name="token-records"></a>權杖記錄

本節說明每個記錄相關權杖的記錄格式。 資訊分成下列各節。

-   [標記 \_ 名稱](/windows)
-   [標記 \_ 字串](/windows)
-   [TOKEN \_ 整數](/windows)
-   [權杖 \_ GUID](/windows)
-   [TOKEN \_ 整數 \_ 清單](/windows)
-   [TOKEN \_ FLOAT \_ 清單](/windows)

## <a name="token_name"></a>標記 \_ 名稱

可變長度的記錄。 標記後面會接著一個計數值，指定 [名稱] 欄位中接下來的位元組數目。 長度計數的 ASCII 名稱會完成記錄。



| 欄位 | 類型       | 大小 (位元組) | 目錄                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | 標記 \_ 名稱                    |
| count | DWORD      | 4            | 名稱欄位的長度（以位元組為單位） |
| NAME  | 位元組陣列 | count        | ASCII 名稱                     |



 

## <a name="token_string"></a>標記 \_ 字串

可變長度的記錄。 標記後面會接著一個計數值，此值會指定字串欄位中所遵循的位元組數目。 長度計數的 ASCII 字串會繼續記錄，該記錄是由終止權杖所完成。 結束字元的選擇取決於其他地方所討論的語法問題。



| 欄位      | 類型       | 大小 (位元組) | 目錄                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | 標記 \_ 字串                    |
| count      | DWORD      | 4            | 字串欄位的長度（以位元組為單位）  |
| 字串     | 位元組陣列 | count        | ASCII 字串                     |
| 終結 | DWORD      | 4            | 標記 \_ 分號或標記 \_ 逗號 |



 

## <a name="token_integer"></a>TOKEN \_ 整數

固定長度記錄。 標記後面接著需要的整數值。



| 欄位 | 類型  | 大小 (位元組) | 目錄       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | tOKEN \_ 整數 |
| 價值 | DWORD | 4            | 單一整數 |



 

## <a name="token_guid"></a>權杖 \_ GUID

固定長度的記錄。 權杖後面會接著憑證 DCE 標準所定義的四個資料欄位。



| 欄位 | 類型       | 大小 (位元組) | 目錄          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | 權杖 \_ GUID       |
| Data1 | DWORD      | 4            | UUID 資料欄位1 |
| Data2 | WORD       | 2            | UUID 資料欄位2 |
| Data3 | WORD       | 2            | UUID 資料欄位3 |
| Data4 | 位元組陣列 | 8            | UUID 資料欄位4 |



 

## <a name="token_integer_list"></a>TOKEN \_ 整數 \_ 清單

可變長度的記錄。 標記後面會接著一個計數值，指定清單欄位中的整數數目。 為了提高效率，連續的整數清單應複合成單一清單。



| 欄位 | 類型  | 大小 (位元組) | 目錄                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | tOKEN \_ 整數 \_ 清單             |
| count | DWORD | 4            | 清單欄位中的整數數目 |
| list  | DWORD | 4 x 計數    | 整數清單                     |



 

## <a name="token_float_list"></a>TOKEN \_ FLOAT \_ 清單

可變長度的記錄。 標記後面會接著一個計數值，可指定清單欄位中接下來的浮點數或雙精度浮點數。 浮點數 (float 或 double) 的大小是由檔案標頭中的 float sizespecified 值所決定。 為了提高效率，連續的 TOKEN \_ FLOAT \_ 清單應複合成單一清單。



| 欄位 | 類型               | 大小 (位元組)   | 目錄                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | tOKEN \_ FLOAT \_ 清單                        |
| count | DWORD              | 4              | 清單欄位中的浮點數或雙精度浮點數 |
| list  | float/double 陣列 | 4或 8 x 計數 | Float 或 double 清單                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[二進位編碼方式](binary-encoding.md)
</dt> </dl>

 

 
