---
title: ps_3_0
description: 瞭解 ps_3_0，這是一個可程式化的圖元著色器，由一組操作圖元資料的指令所組成。
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79145936709e43fab9b87602233225567a0067528a31036aacc11c5b425c0dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512890"
---
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

可程式化的圖元著色器是由一組操作圖元資料的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

-   [ps \_ 3 \_ 0 指示](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) 包含可用指令的清單。
-   [ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) 程式會列出圖元著色器 ALU 所使用的不同類型的暫存器。
-   [](dx9-graphics-reference-asm-ps-registers-modifiers.md)修飾詞用來修改指令的運作方式。
-   [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) 會決定要寫入的目的地登錄元件。
-   [圖元著色器來源暫存器](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) 修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。

## <a name="new-features"></a>新功能

新增臉部暫存器。 新增位置註冊。 色彩暫存器 (v \#) 現在是完全浮點數，而且已合併 (t) 的材質座標暫存器 \# 。 輸入宣告採用使用名稱，而指定暫存器的元件可以使用多個用法。

## <a name="dynamic-flow-control"></a>動態 Flow 控制項

[如果 bool-ps](if-bool---ps.md)、[斷路](break---ps.md)和[break \_ ](break-comp---ps.md)) ，則裝置支援動態流量控制 (。 嵌套的深度範圍從0到24。

## <a name="number-of-temporary-registers"></a>臨時暫存器數目

支援的臨時暫存器數目是32。

## <a name="static-flow-control-nesting-depth"></a>靜態 Flow 控制項的嵌套深度

[呼叫 ps](call---ps.md) / [callnz](callnz-bool---ps.md)  / [呼叫 \_ pred](callnz-pred---ps.md)可以嵌套到最大深度4。 獨立的[迴圈-ps](loop---ps.md) / [](rep---ps.md)指示可以嵌套到最大深度4。

## <a name="arbitrary-swizzle"></a>任意 Swizzle

支援任意 swizzle。 請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)。

## <a name="gradient-instructions"></a>漸層指令

支援漸層指令。 請參閱 [dsx-ps](dsx---ps.md)、 [dsy-](dsy---ps.md)ps 和 [texldd-ps](texldd---ps.md)。

## <a name="predication"></a>預測

支援指令 predication。 請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。

## <a name="dependent-read-limit"></a>相依讀取限制

沒有相依的讀取限制。

## <a name="texture-instruction-limit"></a>材質指令限制

材質指令沒有任何限制。

## <a name="instruction-count"></a>指令計數

每個圖元著色器都允許從512到 MaxPixelShader30InstructionSlots 中的插槽數目， (不超過 32768) 。 因為迴圈支援，所以執行的指令數目可能會更高。 MaxPShaderInstructionsExecuted 至少應為 2 ^ 16。

## <a name="sampler-count"></a>取樣器計數

可用的紋理取樣器數目是16。

## <a name="device-caps"></a>裝置 Cap

如果 \_ 支援 ps 3 \_ 0，硬體 (中最小的) 支援下列上限：



| 筆蓋                                                                                                          | 值                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 每個                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| 以下是設定的基本 cap：                                                                        | D3DPMISCCAPS \_ BLENDOP、D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS、D3DPMISCCAPS \_ CLIPTLVERTS、D3DPMISCCAPS \_ CULLCCW、D3DPMISCCAPS \_ CULLCW、D3DPMISCCAPS \_ CULLNONE、D3DPMISCCAPS \_ FOGINFVF、D3DPMISCCAPS \_ MASKZ                                                                                               |
| 下列是設定的點陣端點：                                                                           | \_D3DPRASTERCAPS 中的 D3DPRASTERCAPS MIPMAPLODBIAS、D3DPRASTERCAPS \_ ANISOTROPY、COLORPERSPECTIVE \_ D3DPRASTERCAPS、SCISSORTEST \_ D3DCAPS9                                                                                                                                                                  |
| 深度偏差的完整支援，包括：                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS、D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| 深度和 Alpha 測試的完整比較集，包括：                                                  | D3DCAPS9 中的所有 D3DPCMPCAPS。                                                                                                                                                                                                                                                                      |
| 來源混合模式                                                                                        | 除了 D3DPBLENDCAPS \_ SRCALPHASAT、D3DPBLENDCAPS \_ BOTHSRCALPHA 和 D3DPBLENDCAPS BOTHINVSRCALPHA) 之外，所有的混合模式都支援作為來源 (\_ 。                                                                                                                                                    |
| 以下是支援的材質帽：                                                                    | D3DPTEXTURECAPS \_ 立方體貼圖、D3DPTEXTURECAPS \_ MIPCUBEMAP、D3DPTEXTURECAPS \_ MIPMAP、D3DPTEXTURECAPS \_ MIPVOLUMEMAP、D3DPTEXTURECAPS \_ 透視圖、D3DPTEXTURECAPS \_ 投射、D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE、D3DPTEXTURECAPS \_ [volumemap                                                        |
| 材質篩選器端點、磁片區材質篩選器和立方體材質篩選器的材質支援如下： | \_ \_ \_ D3DPTFILTERCAPS 和 MINFANISOTROPIC ) 、VOLUMETEXTUREFILTERCAPS \_ CubeTextureFilterCaps、D3DPTFILTERCAPS \_ MIPFPOINT、D3DPTFILTERCAPS \_ MIPFLINEAR、D3DPTFILTERCAPS \_ MAGFPOINT 不需要 D3DPTFILTERCAPS MINFPOINT、D3DPTFILTERCAPS MINFLINEAR、D3DPTFILTERCAPS MAGFLINEAR (             |
| 以下是在頂點和圖元階段支援的材質位址模式：                                | D3DPTADDRESSCAPS \_ WRAP、D3DPTADDRESSCAPS \_ 鏡像、D3DPTADDRESSCAPS \_ 夾具、D3DPTADDRESSCAPS \_ BORDER、D3DPTADDRESSCAPS \_ INDEPENDENTUV、D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| 支援所有圖元著色器 caps。                                                                     | DynamicFlowControlDepth = 24、NumTemps = 32、StaticFlowControlDepth = 4、NumInstructionSlots = 512。 支援下列功能： predication、任意 swizzles 和漸層指令。 沒有相依的讀取限制，且不會限制材質和數學指令的組合。 |
| 支援所有樣板作業。 這包括兩個側邊樣板。                                   | 請參閱 [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| 每個頂點的裝置支援點大小                                                                         | \_D3DCAPS9 中的 D3DFVFCAPS PSIZE                                                                                                                                                                                                                                                                         |
| 2紋理支援的非乘冪。                                                                              | 完整支援或條件式非 pow-2 支援;裝置在 D3DPTEXTURECAPS SQUAREONLY 中不應只有正方形材質的限制 \_ 。                                                                                                                                                    |
| 如果裝置支援多個 rendertargets，則支援下列 cap：                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS、D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| 如果 \_ 支援 vs 3 \_ 0                                                                                     | D3DCAPS9 中的 MaxUserClipPlanes 為6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 