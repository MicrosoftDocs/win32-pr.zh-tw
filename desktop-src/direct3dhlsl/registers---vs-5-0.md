---
title: 註冊-vs_5_0
description: 下列輸入和輸出暫存器會在頂點著色器版本 5 0 中實作為 \_ 。
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9c80125a4640e558872e29e435d48e7420bbd6c504577a5e0c84781f8a47d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853898"
---
# <a name="registers---vs_5_0"></a>註冊-vs \_ 5 \_ 0

下列輸入和輸出暫存器會在頂點著色器版本 5 0 中實作為 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊類型                                      | 計數              | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32位 Temp (r \#)                                   | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 否               | None     | Yes          |
| 32位可編制索引的暫存陣列 (x \# \[ n \])              | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 是              | 無     | Yes          |
| 32位輸入 (v \#)                                  | 32                 | R   | 4         | 是              | 無     | Yes          |
| 輸入資源中的元素 (t \#)                  | 128                | R   | 1         | 否               | None     | Yes          |
| 取樣器 (s \#)                                       | 16                 | R   | 1         | 否               | None     | Yes          |
| ConstantBuffer 參考 (cb \# \[ 索引 \])            | 15                 | R   | 4         | 是 (內容)     | 無     | Yes          |
| iImmediate ConstantBuffer 參考 (的 icb \[ 索引 \])  | 1                  | R   | 4         | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊類型                                                      | 計數 | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Null (捨棄結果，適用于具有多個結果的作業)  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 32位輸出頂點資料元素 (o \#)                             | 32    | W   | 4         | N/A              | N/A      | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




