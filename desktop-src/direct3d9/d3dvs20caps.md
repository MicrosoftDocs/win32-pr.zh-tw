---
description: 頂點著色器的帽常數。 D3DCAPS9 的 VS20Caps 成員會使用這些常數。
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a199fa5e98040cf100846a4773e1077da04fa43e9d9e77a615017ecb9b32ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988868"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

頂點著色器的帽常數。 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 VS20Caps 成員會使用這些常數。



| \#定義                              | 值          | 描述                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS \_ PREDICATION              |  (1 << 0)  | 支援指令 predication。 請參閱[setp \_ 複合-vs](../direct3dhlsl/setp-comp---vs.md)                                                                                                                                                                                                                   |
| D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH | 24             | 動態流程式控制制指令的最大層級 ([break-vs](../direct3dhlsl/break---vs.md)、 [break \_ 複合-](../direct3dhlsl/break-comp---vs.md)vs、 [breakp-](../direct3dhlsl/breakp---vs.md)vs，如果是 pred 和) ，則為，如果是，則為複合[ \_ ](../direct3dhlsl/if-comp---vs.md) \_ 。 [](../direct3dhlsl/if-pred---vs.md) |
| D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH | 0              | 動態流程式控制制指令的最小層級 ([break-vs](../direct3dhlsl/break---vs.md)、 [break \_ 複合-](../direct3dhlsl/break-comp---vs.md)vs、 [breakp-](../direct3dhlsl/breakp---vs.md)vs，如果是 pred 和) ，則為，如果是複合的，則為[ \_ ](../direct3dhlsl/if-comp---vs.md) \_ 。 [](../direct3dhlsl/if-pred---vs.md) |
| D3DVS20 \_ MAX \_ NUMTEMPS                | 32             | 支援的臨時暫存器數目上限。                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MIN \_ NUMTEMPS                | 12             | 支援的臨時暫存器數目下限。                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH  | 4              | 迴圈的最大深度[： vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。                                                                                           |
| D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH  | 1              | 迴圈的最小深度[-vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。                                                                                           |



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
