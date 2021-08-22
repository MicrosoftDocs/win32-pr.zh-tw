---
title: ps_2_x
description: 瞭解 ps_2_x，這是一個可程式化的圖元著色器，由一組操作圖元資料的指令所組成。
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37bc9709effeb865651ca920a155094946b88753586174ecf6e1ab06eabd2fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489408"
---
# <a name="ps_2_x"></a>ps \_ 2 \_ x

可程式化的圖元著色器是由一組操作圖元資料的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

-   [ps \_ 2 \_ x 指示](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) 包含可用指令的清單。
-   [ps \_ 2 \_ x 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) 程式會列出頂點著色器 ALU 所使用的不同類型的暫存器。
-   [](dx9-graphics-reference-asm-ps-registers-modifiers.md)修飾詞用來修改指令的運作方式。
-   [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) 會決定要寫入的目的地登錄元件。
-   [圖元著色器來源暫存器](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) 修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。

## <a name="dynamic-flow-control"></a>動態 Flow 控制項

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)代表動態流程式控制制指示的嵌套深度：[如果](if-bool---ps.md)[是，則為，如果是 \_](if-comp---ps.md) [ \_ pred](if-pred---ps.md)、[斷路](break---ps.md)和 break，[則 \_](break-comp---ps.md)為。 此值等於 if comp 區塊的嵌套深度 \_ 。 如果此上限為零，則裝置不支援動態流程式控制制指示。

## <a name="number-of-temporary-registers"></a>臨時暫存器數目

裝置支援的臨時暫存器數目。 範圍是從12到32。

## <a name="static-flow-control-nesting-depth"></a>靜態 Flow 控制項的嵌套深度

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)代表兩種靜態流程式控制制指令類型的嵌套深度：[迴圈](loop---ps.md)  / [代表](rep---ps.md)和 [呼叫](call---ps.md)  / [callnz](callnz-bool---ps.md)。 迴圈/rep 指令可以嵌套至 **StaticFlowControlDepth** 深層。 呼叫/callnz 指令可以獨立地嵌套至 **StaticFlowControlDepth** 深層。

## <a name="number-of-instruction-slots"></a>指令位置數目

指令位置數目的範圍可從96到最大值512，並由 [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)指定。 **MaxPixelShaderInstructionsExecuted** 會定義可執行檔指令總數。 這可能會大於迴圈和副程式呼叫所造成的指令位置數目。

## <a name="arbitrary-swizzle"></a>任意 Swizzle

如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，則會支援任意 swizzle。 請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)。

## <a name="gradient-instructions"></a>漸層指令

如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就會支援漸層指令。 請參閱 [dsx-ps](dsx---ps.md)、 [dsy-](dsy---ps.md)ps 和 [texldd-ps](texldd---ps.md)。

## <a name="predication"></a>預測

如果已設定 [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，則支援指示 PREDICATION。 請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。

## <a name="dependent-read-limit"></a>相依讀取限制

如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就不會有相依的讀取限制。

## <a name="texture-instruction-limit"></a>材質指令限制

如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就不會有紋理指示的限制。

## <a name="sampler-count"></a>取樣器計數

可用的紋理取樣器數目是16。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 