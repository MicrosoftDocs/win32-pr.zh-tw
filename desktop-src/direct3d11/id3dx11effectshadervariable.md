---
title: 'ID3DX11EffectShaderVariable 介面 (D3dx11effect .h) '
description: 著色器變數介面會存取著色器變數。
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- ID3DX11EffectShaderVariable 介面 Direct3D 11
- ID3DX11EffectShaderVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75db5950f485cb15701b4963b24f9a0478b716b8ab61ed6de0df9ce1f0f5cecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408138"
---
# <a name="id3dx11effectshadervariable-interface"></a>ID3DX11EffectShaderVariable 介面

著色器變數介面會存取著色器變數。

## <a name="members"></a>成員

**ID3DX11EffectShaderVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectShaderVariable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectShaderVariable** 介面具有這些方法。



| 方法                                                                                                           | 描述                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**GetComputeShader**](id3dx11effectshadervariable-getcomputeshader.md)                                         | 取得計算著色器。<br/>                       |
| [**GetDomainShader**](id3dx11effectshadervariable-getdomainshader.md)                                           | 取得網域著色器。<br/>                        |
| [**GetGeometryShader**](id3dx11effectshadervariable-getgeometryshader.md)                                       | 取得幾何著色器。<br/>                      |
| [**GetHullShader**](id3dx11effectshadervariable-gethullshader.md)                                               | 取得輪廓著色器。<br/>                          |
| [**GetInputSignatureElementDesc**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | 取得輸入簽名描述。<br/>         |
| [**GetOutputSignatureElementDesc**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | 取得輸出特徵標記描述。<br/>        |
| [**GetPatchConstantSignatureElementDesc**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | 取得修補程式常數簽章描述。<br/> |
| [**GetPixelShader**](id3dx11effectshadervariable-getpixelshader.md)                                             | 取得圖元著色器。<br/>                         |
| [**GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)                                               | 取得著色器描述。<br/>                   |
| [**GetVertexShader**](id3dx11effectshadervariable-getvertexshader.md)                                           | 取得頂點著色器。<br/>                        |



 

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





