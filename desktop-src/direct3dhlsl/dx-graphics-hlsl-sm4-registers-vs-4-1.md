---
title: 註冊-vs_4_1
description: 本章節包含頂點著色器第4版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119922"
---
# <a name="registers---vs_4_1"></a>暫存器-vs \_ 4 \_ 1

本章節包含頂點著色器第4版所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊      | 名稱 | 計數              | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 否               | None     | Yes          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 是              | 無     | Yes          |
| v\#           |      | 32                 | R   | 4         | 是              | 無     | Yes          |
| 10gbase-t\#           |      | 128                | R   | 1         | 否               | None     | Yes          |
| s\#           |      | 16                 | R   | 1         | 否               | None     | Yes          |
| cb \# \[ 索引\] |      | 15                 | R   | 4         | 是 (內容)     | 無     | Yes          |
| icb \[ 索引\]  |      | 1                  | R   | 4         | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊 | 名稱            | 計數 | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | 捨棄結果  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 輸出\#      | 輸出暫存器 | 32    | W   | N/A       | N/A              | 4        | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




