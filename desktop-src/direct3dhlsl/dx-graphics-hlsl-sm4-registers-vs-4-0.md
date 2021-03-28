---
title: 註冊-vs_4_0
description: 本章節包含頂點著色器 4 0 所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990615"
---
# <a name="registers---vs_4_0"></a>暫存器-vs \_ 4 \_ 0

本章節包含頂點著色器 4 0 所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊      | Name | Count              | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 否               | None     | Yes          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 是              | 無     | Yes          |
| V\#           |      | 16                 | R   | 4         | 是              | 無     | Yes          |
| 10gbase-t\#           |      | 128                | R   | 1         | 否               | None     | Yes          |
| s\#           |      | 16                 | R   | 1         | 否               | None     | Yes          |
| cb \# \[ 索引\] |      | 15                 | R   | 4         | 是 (內容)     | 無     | Yes          |
| icb \[ 索引\]  |      | 1                  | R   | 4         | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊 | Name            | Count | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | 捨棄結果  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 輸出\#      | 輸出暫存器 | 16    | W   | N/A       | N/A              | 4        | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




