---
title: 如何建立輪廓著色器
description: 本主題說明如何建立輪廓著色器。
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa9fe55a11c68e4cbc247f6509c52b6bac1d01b823d48637ee51073437316f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608988"
---
# <a name="how-to-create-a-hull-shader"></a>如何：建立輪廓著色器

輪廓著色器是三個階段中的第一個，可共同運作以實行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md)式。 輪廓著色器輸出會驅動鑲嵌階段以及網域著色器階段。 本主題說明如何建立輪廓著色器。

輪廓著色器會將一組輸入控制點 (從頂點著色器) 轉換為一組輸出控制點。 輸入和輸出點的數目可能會隨著轉換而有所不同， (一般轉換會是基礎轉換) 。

輪廓著色器也會輸出網域著色器和鑲嵌的 patch 常數資訊，例如鑲嵌式因素。 固定函式鑲嵌階段會使用鑲嵌式因素以及在輪廓著色器中宣告的其他狀態，來決定要 tessellate 多少。

**若要建立輪廓著色器**

1.  設計輪廓著色器。 請參閱 [如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)。
2.  編譯著色器程式碼
3.  使用 [**ID3D11Device：： CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)建立輪廓著色器物件。
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  使用 [**>id3d11devicecoNtext：： HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)初始化管線階段。
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

如果已系結輪廓著色器，則必須將網域著色器系結至管線。 尤其是，使用幾何著色器直接串流出輪廓著色器的控制點是不正確。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




