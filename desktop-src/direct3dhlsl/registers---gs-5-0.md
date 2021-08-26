---
title: 註冊-gs_5_0
description: 下列輸入和輸出暫存器會在幾何著色器版本 5 0 中實作為 \_ 。
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023498"
---
# <a name="registers---gs_5_0"></a>註冊-gs \_ 5 \_ 0

下列輸入和輸出暫存器會在幾何著色器版本 5 0 中實作為 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊類型                                     | 計數              | R/W | 尺寸         | R 可編制索引\# | Defaults | 需要 DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| 32位 Temp (r \#)                                  | 4096 (r \# + x \# \[ n \])  | R/W | 4                 | 否               | None     | Yes          |
| 32位可編制索引的暫存陣列 (x \# \[ n \])             | 4096 (r \# + x \# \[ n \])  | R/W | 4                 | 是              | 無     | Yes          |
| 32位輸入 (v \[ 頂點 \] \[ 元素 \])              | 32                 | R   | 4 (複合) \* 32 (垂直)  | Yes              | 無     | Yes          |
| 32位輸入基本識別碼 (vPrim)                  | 1                  | R   | 1                 | 否               | None     | Yes          |
| 32位輸入實例識別碼 (vInstanceID)             | 1                  | R   | 1                 | 否               | None     | Yes          |
| 輸入資源中的元素 (t \#)                 | 128                | R   | 1                 | 否               | None     | Yes          |
| 取樣器 (s \#)                                      | 16                 | R   | 1                 | 否               | None     | Yes          |
| ConstantBuffer 參考 (cb \# \[ 索引 \])           | 15                 | R   | 4                 | 是 (內容)     | 無     | Yes          |
|  (icb \[ 索引) 的立即 ConstantBuffer 參考 \] | 1                  | R   | 4                 | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊類型                                               | 計數 | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Null (捨棄結果，適用于具有多個結果的 ops)  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 32位輸出頂點資料元素 (o \#)                      | 32    | W   | N/A       | N/A              | 4        | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




