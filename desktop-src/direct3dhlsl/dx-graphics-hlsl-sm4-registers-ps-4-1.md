---
title: 註冊-ps_4_1
description: 本章節包含圖元著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932212"
---
# <a name="registers---ps_4_1"></a>註冊-ps \_ 4 \_ 1

本章節包含圖元著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊      | Name | Count              | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 否               | None     | Yes          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 是              | 無     | Yes          |
| V\#           |      | 32                 | R   | 4         | 是              | 無     | Yes          |
| 10gbase-t\#           |      | 128                | R   | 1         | 否               | None     | Yes          |
| s\#           |      | 16                 | R   | 1         | 否               | None     | Yes          |
| cb \# \[ 索引\] |      | 15                 | R   | 4         | 是 (內容)     | 無     | Yes          |
| icb \[ 索引\]  |      | 1                  | R   | 4         | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊 | Name             | Count | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | 捨棄結果   | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 輸出\#      | 輸出暫存器  | 8     | W   | N/A       | N/A              | 4        | 否           |
| oDepth   | 輸出深度     | 1     | W   | N/A       | N/A              | 1        | N/A          |
| oMask    | 輸出 MSAA 遮罩 | 1     | W   | N/A       | N/A              | 1        | N/A          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




