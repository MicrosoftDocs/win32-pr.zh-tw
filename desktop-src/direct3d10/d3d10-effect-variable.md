---
description: 這些常數適用于效果變數。
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE 常數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736067"
---
# <a name="d3d10_effect_variable-constants"></a>D3D10 \_ 效果 \_ 變數常數

這些常數適用于效果變數。



| \#定義                                       | 描述  | 值                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ 效果 \_ 變數 \_ 注釋            | 1 << 0 | 表示這是批註或全域變數。                                                                                                                                                                                                        |
| D3D10 \_ 效果 \_ 變數集區 \_                | 1 << 1 | 指出這個變數或常數緩衝區位於效果集區中。 如果未設定此旗標，則變數會處於獨立效果或子效果 (獨立效果會從 [**ID3D10Effect：： IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)傳回 false。 |
| D3D10 \_ 效果 \_ 變數 \_ 明確 \_ 綁定 \_ 點 | 1 << 2 | 表示已使用 register 關鍵字明確地系結變數。                                                                                                                                                                                 |



 

這些旗標在 d3d10effect 中會定義為宏。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的效果常數 ](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



