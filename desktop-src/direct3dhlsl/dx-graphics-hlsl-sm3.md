---
title: 著色器模型3
description: 著色器模型3將其他功能新增至著色器模型2。
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed2d64ccfb06fc0fe50e5bd0075732c1fd9cbb70ca1e05bda5afd24cd5c5f98f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789538"
---
# <a name="shader-model-3-hlsl-reference"></a>著色器模型 3 (HLSL 參考) 

著色器模型3將其他功能新增至 [著色器模型 2](dx-graphics-hlsl-sm2.md)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>功能</td>
<td>功能</td>
</tr>
<tr class="even">
<td>指令集</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></li>
<li>元件指示 (請參閱 <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">Ps_3_0 指示</a>、 <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">指示-vs_3_0</a>) </li>
</ul></td>
</tr>
<tr class="odd">
<td>註冊集</td>
<td><ul>
<li>圖元著色器暫存器 (查看 <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">Ps_3_0 註冊</a>) </li>
<li>頂點著色器註冊 (請參閱暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">-vs_3_0</a>) </li>
</ul></td>
</tr>
<tr class="even">
<td>圖元著色器最大值</td>
<td>最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxPixelShader30InstructionSlots (請參閱 <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>) 。</td>
</tr>
<tr class="odd">
<td>頂點著色器最大值</td>
<td>最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxVertexShader30InstructionSlots (參閱 <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) 。</td>
</tr>
<tr class="even">
<td>著色器設定檔</td>
<td>ps_3_0，vs_3_0</td>
</tr>
</tbody>
</table>



 

如需模型3著色器的詳細資訊，請參閱：

-   [圖元著色器3。0](dx9-graphics-reference-asm-ps-3-0.md)
-   [頂點著色器3。0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 