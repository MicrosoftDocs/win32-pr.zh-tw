---
title: vs_2_x
description: 可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463464"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

頂點著色器版本與 \_ 2 \_ x 擴充 vs 2 0 所支援的功能集 \_ \_ 。 每個額外的功能都會以 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)中 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)結構的對應端點表示。 若要使用這些 caps 所表示的任何增強功能，必須將頂點著色器版本指定為 vs \_ 2 \_ x。

-   [指示-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) 包含可用指令的清單。
-   暫存器[-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md)列出頂點著色器 ALU 所使用的不同類型的暫存器。
-   [頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。
-   [頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。
-   [目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。

## <a name="new-features"></a>新功能

新功能如下：

### <a name="dynamic-flow-control"></a>動態流程式控制制

如果 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0，則支援下列動態流程式控制制指示：

-   [如果是 \_ 複合-vs](if-comp---vs.md)
-   [中斷-vs](break---vs.md)
-   [中斷 \_ 複合-vs](break-comp---vs.md)

如果也設定了 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ，則支援下列額外的流程式控制制指示：

-   [setp \_ 複合-vs](setp-comp---vs.md)
-   [如果 pred-vs](if-pred---vs.md)
-   [callnz pred-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

動態流程式控制制深度的值範圍是0到24，等於動態流程式控制制指示的嵌套深度 (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)) 。 如果此上限為零，則裝置不支援動態流程式控制制指示。

### <a name="number-of-temporary-registers"></a>臨時暫存器數目

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) 代表裝置所支援的 [暫存](dx9-graphics-reference-asm-vs-registers-temporary.md)登錄數目。 此上限的值範圍是12到32。

### <a name="static-flow-control-nesting-depth"></a>靜態流程式控制制的嵌套深度

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)代表兩種靜態流程式控制制指令類型的嵌套深度：[迴圈-vs](loop---vs.md) / [rep-vs](rep---vs.md)和[call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md)， / [如果 bool-vs](if-bool---vs.md). 迴圈-vs/rep-vs 指令可以嵌套到 D3DVS20CAPS 深層。 相對地，call-vs/callnz bool-vs 指令可以嵌套至 D3DVS20CAPS 深層。 如果同時設定了 D3DVS20CAPS，則 [callnz pred-vs](callnz-pred---vs.md) 會計算呼叫-vs/callnz bool-vs/if bool-vs (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)) 。

### <a name="predication"></a>預測

如果設定了 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ，則裝置支援 [setp 的 \_ comp](setp-comp---vs.md) 與指令 predication。 如果 D3DVS20CAPS 也大於0，則支援下列額外的動態流程式控制制指示：

-   [如果 pred-vs](if-pred---vs.md)
-   [callnz pred-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

### <a name="instruction-count"></a>指令計數

每個頂點著色器最多可以儲存256指令。 執行的指令數目可能會更高 (因為迴圈/rep 支援) ，且受限於 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)的上限，其應至少為0xffff。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 