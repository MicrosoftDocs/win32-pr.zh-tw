---
title: 著色器模型4元件
description: 著色器模型4元件
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 805ffe89b1f9d14ca70da0a8121353e6bf766b8b6e433441350d1b55c4531415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119952"
---
# <a name="shader-model-4-assembly"></a>著色器模型4元件

著色器模型4需要您在 HLSL 中編寫著色器。 不過，著色器編譯器會將 HLSL 程式碼編譯為在裝置上執行的元件。 如果您使用 PIX 進行 Windows 來對著色器進行偵錯工具，您可以選擇在 HLSL 或元件中顯示著色器程式碼。 本節列出在您對著色器進行偵錯工具時，可能會遇到的著色器模型4和著色器模型4.1 元件指示。

<dl>

[指令修飾詞](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[繼續](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[削減](cut--sm4---asm-.md)  
[dcl \_ constantBuffer](dcl-constantbuffer.md)  
[dcl \_ globalFlags](dcl-globalflags.md)  
[dcl \_ immediateConstantBuffer](dcl-immediateconstantbuffer.md)  
[dcl \_ indexableTemp](dcl-indexabletemp.md)  
[dcl \_ indexRange](dcl-indexrange.md)  
[dcl \_ 輸入](dcl-input.md)  
[dcl \_ 輸入 \_ sv](dcl-input-sv.md)  
[dcl \_ 輸入 vPrim](dcl-input-vprim.md)  
[dcl \_ maxOutputVertexCount](dcl-maxoutputvertexcount.md)  
[dcl \_ 輸出](dcl-output.md)  
[dcl \_ 輸出 \_ oDepth](dcl-output-odepth.md)  
[dcl \_ 輸出 \_ sgv](dcl-output-sgv.md)  
[dcl \_ 輸出 \_ siv](dcl-output-siv.md)  
[dcl \_ outputTopology](dcl-outputtopology.md)  
[dcl \_ 資源](dcl-resource.md)  
[dcl \_ 取樣器](dcl-sampler.md)  
[dcl \_ 溫度](dcl-temps.md)  
[預設值](default--sm4---asm-.md)  
[deriv \_ rtx](deriv-rtx--sm4---asm-.md)  
[deriv \_ rty](deriv-rty--sm4---asm-.md)  
[丟棄](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[發出](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[endloop](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[Frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[iadd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[Ige](ige--sm4---asm-.md)  
[ilt](ilt--sm4---asm-.md)  
[imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[視窗](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[Ld](ld--sm4---asm-.md)  
[日誌](log--sm4---asm-.md)  
[環](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[瘋狂](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[平均線](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[nop](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[resinfo](resinfo--sm4---asm-.md)  
[Ret](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[四捨五入 \_](round-ne--sm4---asm-.md)  
[四捨五入 \_](round-ni--sm4---asm-.md)  
[四捨五入 \_ pi](round-pi--sm4---asm-.md)  
[圓形 \_ z](round-z--sm4---asm-.md)  
[rsq](rsq--sm4---asm-.md)  
[樣品](sample--sm4---asm-.md)  
[範例 \_ b](sample-b--sm4---asm-.md)  
[範例 \_ c](sample-c--sm4---asm-.md)  
[範例 \_ c \_ lz](sample-c-lz--sm4---asm-.md)  
[範例 \_ d](sample-d--sm4---asm-.md)  
[範例 \_ l](sample-l--sm4---asm-.md)  
[sincos](sincos--sm4---asm-.md)  
[sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[u）](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[umax](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[Xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>著色器模型4.1 元件

著色器模型4.1 支援所有著色器模型4.0 指令和下列其他指示：

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[Lod](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Asm 著色器參考](dx9-graphics-reference-asm.md)
</dt> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




