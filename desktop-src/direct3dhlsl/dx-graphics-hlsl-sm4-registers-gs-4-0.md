---
title: 註冊-gs_4_0
description: 本章節包含幾何著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a27cbd13cba06ebb05fe1155bc97d13debe3154da48c05cf97a31d889ba88fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513621"
---
# <a name="registers---gs_4_0"></a>註冊-gs \_ 4 \_ 0

本章節包含幾何著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊                 | 名稱 | 計數              | R/W | 尺寸        | R 可編制索引\# | Defaults | 需要 DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096 (r \# + x \# \[ n \])  | R/W | 4                | 否               | None     | 是          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \])  | R/W | 4                | 是              | 無     | 是          |
| v \# \[ 頂點 \] \[ 元素\] |      | 32                 | R   | 4 (複合) \* 6 (垂直)  | 是              | 無     | 是          |
| vprim                    |      | 1                  | R   | 1                | 否               | None     | 是          |
| 10gbase-t\#                      |      | 128                | R   | 1                | 否               | None     | 是          |
| s\#                      |      | 16                 | R   | 1                | 否               | None     | 是          |
| cb \# \[ 索引\]            |      | 15                 | R   | 4                | 是 (內容)     | 無     | 是          |
| icb \[ 索引\]             |      | 1                  | R   | 4                | 是 (內容)     | 無     | 是          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊 | 名稱            | 計數 | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | 捨棄結果  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 輸出\#      | 輸出暫存器 | 32    | W   | N/A       | N/A              | 4        | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




