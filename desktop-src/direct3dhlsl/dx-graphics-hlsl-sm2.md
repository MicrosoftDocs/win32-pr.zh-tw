---
title: 著色器模型2
description: 著色器模型2將其他功能新增至著色器模型1。
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed402b34bdb8ba8caed8dc7cd5b66126d242c9ad
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988021"
---
# <a name="shader-model-2"></a>著色器模型2

著色器模型2將其他功能新增至 [著色器模型 1](dx-graphics-hlsl-sm1.md)。





|--------|-------| |功能 |功能 | |指令集 | <ul><li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></li><li>元件指示 (請參閱 <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">指示-vs_2_0</a>、 <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">指示 Vs_2_x</a>、 <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 指示</a>、 <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x 指示</a>) </li></ul> | |註冊集 | <ul><li>圖元著色器暫存器 (查看 <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0</a>暫存器、 <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x 註冊</a>) </li><li>頂點著色器暫存器 (請參閱暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">-vs_2_0</a>、暫存器 <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">vs_2_x</a>) </li></ul> | |圖元著色器最大值 | <ul><li>ps_2_0-32 材質 + 64 算術</li><li>ps_2_x-96 的最小值，最多可達 D3DCAPS9 中的插槽數目。D3DPSHADERCAPS2_0. NumInstructionSlots。 請參閱 D3DPSHADERCAPS2_0</li></ul> | |頂點著色器最大值 |256指示 | |著色器設定檔 |ps_2_0、ps_2_x、vs_2_0 vs_2_x | 




 

如需著色器模型2的詳細資訊，請參閱：

-   [圖元著色器 2.0](dx9-graphics-reference-asm-ps-2-0.md)、[圖元著色器](dx9-graphics-reference-asm-ps-2-x.md)2。x
-   [頂點著色器 2.0](dx9-graphics-reference-asm-vs-2-0.md)、[頂點著色器](dx9-graphics-reference-asm-vs-2-x.md)2。x

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




