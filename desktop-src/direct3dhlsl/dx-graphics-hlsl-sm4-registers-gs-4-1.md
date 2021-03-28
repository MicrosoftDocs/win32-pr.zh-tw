---
title: 註冊-gs_4_1
description: 本章節包含幾何著色器 4 \_ 0 和 4 1 所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183691"
---
# <a name="registers---gs_4_1"></a>註冊-gs \_ 4 \_ 1

本章節包含幾何著色器 4 \_ 0 和 4 1 所執行之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊                 | Name | Count              | R/W | 維度        | R 可編制索引\# | Defaults | 需要 DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096 (r \# + x \# \[ n \])  | R/W | 4                | 否               | None     | Yes          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \])  | R/W | 4                | 是              | 無     | Yes          |
| v \# \[ 頂點 \] \[ 元素\] |      | 32                 | R   | 4 (複合) \* 6 (垂直)  | Yes              | 無     | Yes          |
| vprim                    |      | 1                  | R   | 1                | 否               | None     | Yes          |
| 10gbase-t\#                      |      | 128                | R   | 1                | 否               | None     | Yes          |
| s\#                      |      | 16                 | R   | 1                | 否               | None     | Yes          |
| cb \# \[ 索引\]            |      | 15                 | R   | 4                | 是 (內容)     | 無     | Yes          |
| icb \[ 索引\]             |      | 1                  | R   | 4                | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊 | Name            | Count | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | 捨棄結果  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 輸出\#      | 輸出暫存器 | 32    | W   | N/A       | N/A              | 4        | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




