---
description: 所有位 and 部分位關鍵字都是用來測試整數型別中的位。
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: 全部位 and 部分位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594718"
---
# <a name="all-bitwise-and-some-bitwise"></a>全部位 and 部分位

**所有位** AND **部分位** 關鍵字都是用來測試整數型別中的位。 如果屬性中的所有設定位都符合遮罩，則 **所有位** 都是 true。 如果屬性中至少有一個設定位符合遮罩，則 **某些位** 為 true。

您可以將運算子套用至純量 (單一值) 屬性和向量 (多重值) 屬性。 下列程式碼範例示範如何使用 **所有位** And 和 **SOME 位** 來測試屬性值。


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>比較運算子

下表列出支援的位測試比較運算子。



| 比較運算子 | 描述  |
|---------------------|--------------|
| =                   | 等於     |
| ！ = 或 <>      | 不等於 |



 

下表列出位測試的邏輯。



| 位測試和比較運算子 | 邏輯                   |
|--------------------------------------|-------------------------|
| = 全部位                        | 屬性 & Mask = Mask  |
| = 部分位                       | 屬性 & Mask！ = 0    |
| <> 全部位                 | 屬性 & Mask！ = Mask |
| <> 部分位                | 屬性 & Mask = 0     |



 

下列事實資料表使用範例二進位和十六進位值來示範位測試的邏輯。



| Binary (hex) 中的屬性 | Binary 中的遮罩 (hex)  | 屬性 & Mask = binary (hex)  | = 部分位 | = 全部位 |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)                | 0001 (0x1)            | 0001 (0x1)                      | True           | True          |
| 0001 (0x1)                | 0011 (0x3)            | 0001 (0x1)                      | 是           | 否         |
| 0011 (0x3)                | 0001 (0x1)            | 0001 (0x1)                      | True           | True          |
| 0010 (0x2)                | 0001 (0x1)            | 0000 (0x0)                      | False          | False         |
| 11110000 (0xF0)           | 00000011 (0x03)       | 00000000 (0x00)                 | False          | False         |
| 11110010 (0xF2)           | 11110010 (0xF2)       | 11110010 (0xF2)                 | True           | True          |
| 11110010 (0xF2)           | 00000011 (0x03)       | 00000010 (0x02)                 | 是           | 否         |



 

## <a name="example"></a>範例

以下是 **所有位** 述詞的範例。


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



