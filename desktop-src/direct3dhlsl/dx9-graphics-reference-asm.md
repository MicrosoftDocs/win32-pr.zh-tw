---
title: Asm 著色器參考
description: 著色器會驅動可程式化圖形管線。
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104971644"
---
# <a name="asm-shader-reference"></a>Asm 著色器參考

著色器會驅動可程式化圖形管線。

## <a name="vertex-shader-reference"></a>頂點著色器參考

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[頂點著色器差異](dx9-graphics-reference-asm-vs-differences.md) 摘要說明頂點著色器版本之間的差異。

## <a name="pixel-shader-reference"></a>圖元著色器參考

-   [ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [ps \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [ps \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [ps \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[圖元著色器差異](dx9-graphics-reference-asm-ps-differences.md) 摘要說明圖元著色器版本之間的差異。

## <a name="shader-model-4-and-5-reference"></a>著色器模型4和5參考

[著色器模型4元件](dx-graphics-hlsl-sm4-asm.md)和[著色器模型5元件](shader-model-5-assembly--directx-hlsl-.md)章節描述著色器模型4和5支援的指示。

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>元件著色器中常數暫存器的行為

有兩種方式可以在元件著色器中設定常數暫存器：

-   使用其中一個 def 指令來宣告元件程式碼中的著色器常數 \* 。
-   使用其中一個 Set \* \* \* ShaderConstant \* API 方法。

### <a name="direct3d-9-shader-constants"></a>Direct3D 9 著色器常數

在 Direct3D 9 中，指定著色器中已定義常數的存留期僅限於執行該著色器 (且不可覆寫) 。 在 Direct3D 9 中定義的常數在著色器以外沒有任何副作用。

以下是使用 Direct3D 9 的範例：


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



在 Direct3D 9 中，呼叫 Get \* \* \* ShaderConstant \* 只會取得透過 set ShaderConstant 所設定的常數值 \* \* \* \* 。

### <a name="direct3d-8-shader-constants"></a>Direct3D 8 著色器常數

此行為在 Direct3D 8.x 中不同。


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



在 Direct3D 8.x 中，Set \* \* \* ShaderConstant 會立即生效。 假設有下列情況：


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



不想要的結果是設定著色器的順序可能會影響個別著色器觀察到的行為。

## <a name="shader-driver-model-requirements"></a>著色器驅動程式模型需求

Direct3D 9 介面受限於 DirectX 7 層級和更新版本的設備磁碟機介面 (DDI) 驅動程式。 若要檢查 DDI 層級，請執行 [DirectX 診斷工具](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) ，並檢查儲存的文字檔。

針對參考，Direct3D 8 介面只適用于 DirectX 6 層級和更新版本的 DDI 驅動程式。

## <a name="shader-binary-format"></a>著色器二進位格式

著色器指令資料流程的位配置是在 D3d9types 中定義。 如果您想要設計自己的著色器編譯器或建築工具，並且想要更多有關著色器權杖資料流程的詳細資訊，請參閱 Direct3D 9 驅動程式開發工具組 (DDK) 。

## <a name="c-like-shader-language"></a>類似 C 著色器語言

請參閱 [HLSL 參考](dx-graphics-hlsl-reference.md) ，以體驗類似 C 的著色器語言。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的參考](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




