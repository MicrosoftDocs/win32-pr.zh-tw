---
title: '相對定址 (HLSL 與參考) '
description: 針對頂點著色器，\\ 語法只能用在某些著色器模型中可以相對定址的暫存器類型。
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 82fe97a6b78a2257208f3072d5932523d5cd04ba1d044b8a57fad5f3c212b94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744338"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>相對定址 (HLSL 與參考) 

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



| 註冊類型 | 頂點著色器版本 |
|---------------|------------------------|
| a0            | 全部                    |
| 鋁            | vs \_ 2 \_ 0 和更新版本    |
| cn            | vs \_ 1 \_ 1 和更新版本    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




