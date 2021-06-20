---
title: '相對定址 (HLSL PS 參考) '
description: 若是圖元著色器，\ \ 語法只能用在某些著色器模型中可以相對定址的暫存器類型。
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405481"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>相對定址 (HLSL PS 參考) 

此 \[ \] 語法只能用在某些著色器模型中可以相對定址的暫存器類型。 支援的語法格式如下所示 \[ \] ：

其中：

-   "R" 代表任何可以相對定址的註冊類型。
-   "A" 代表任何可用來做為索引的暫存器，以相對於其他暫存器的位址。
-   n0-ni、m0-mj 和 k 為整數 >= 0。



| \[\]語法                              | 有效索引                       | 範例                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c. \[ x + 3 + 7 \]              |
| R \[ k \] ( = Rk )                          | k                                     | c \[ 10 \] ( = c10 )               |
| R \[ A \]                                  | A                                     | c. \[ y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[\]                                 | A + k                                 | c12 \[ aL \] ，c0 \[ a0. z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

這些暫存器適用于下列版本：



| 註冊類型                                                                                   | 圖元著色器版本 |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [迴圈計數器](dx9-graphics-reference-asm-ps-registers-loop-counter.md)：輸入暫存器上的 aL | ps \_ 3 \_ 0 和更新版本   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




