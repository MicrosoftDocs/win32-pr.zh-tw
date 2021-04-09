---
description: 圖元著色器功能旗標。
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111417"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

圖元著色器功能旗標。



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#定義                                     | 值          | 描述                                                                                                                                                                                                       |
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      |  (1 << 0)  | 支援任意 swizzling。                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  |  (1 << 1)  | 支援漸層指令。                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION           |  (1 << 2)  | 支援指令 predication。 請參閱 [setp \_ 的複合-ps](../direct3dhlsl/setp-comp---ps.md)。                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  |  (1 << 3)  | 每個指令的相依讀取數目沒有任何限制。                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT |  (1 << 4)  | Tex 指令數目沒有任何限制。                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | 動態流程式控制制指令的最大層級 (break、breakc、ifc) 。                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | 動態流程式控制制指令的最小層級 (break、breakc、ifc) 。                                                                                                                           |
| D3DPS20 \_ MAX \_ NUMTEMPS                       | 32             | 驅動程式最多可支援此許多暫存註冊。                                                                                                                                                     |
| D3DPS20 \_ MIN \_ NUMTEMPS                       | 12             | 驅動程式至少會支援這個許多暫存註冊。                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | 迴圈的最大深度[： vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。 |
| D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH         | 1              | 迴圈的最小深度[-vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。 |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | 驅動程式最多可支援此許多指示。                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | 驅動程式至少會支援此許多指示。                                                                                                                                                          |



 

這些常數會由 D3DCAPS9 的 D3DPSHADERCAPS2 \_ 0 成員使用[](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)。

## <a name="constant-information"></a>常數資訊



|                          |            |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
