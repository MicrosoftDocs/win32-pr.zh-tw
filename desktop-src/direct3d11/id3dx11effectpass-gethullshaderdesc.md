---
title: 'ID3DX11EffectPass GetHullShaderDesc 方法 (D3dx11effect .h) '
description: 取得輪廓-著色器描述。
ms.assetid: 1a683e61-da9a-4d78-8073-a6104625852b
keywords:
- GetHullShaderDesc 方法 Direct3D 11
- GetHullShaderDesc 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，GetHullShaderDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetHullShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2fb35ddd251b6f25163b5ee4ac15ed448dc7884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696763"
---
# <a name="id3dx11effectpassgethullshaderdesc-method"></a>ID3DX11EffectPass：： GetHullShaderDesc 方法

取得輪廓-著色器描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetHullShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* 
</dt> <dd>

類型： **[ **D3DX11 \_ PASS \_ 著色器 \_ DESC**](d3dx11-pass-shader-desc.md)\***

輪廓著色器描述的指標 (參閱 [**D3DX11 \_ 傳遞 \_ 著色器 \_ DESC**](d3dx11-pass-shader-desc.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





