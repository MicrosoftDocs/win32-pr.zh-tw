---
title: 'D3DX11_PASS_SHADER_DESC 結構 (D3dx11effect .h) '
description: 描述效果傳遞。
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974707"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>D3DX11 \_ PASS \_ 著色器 \_ DESC 結構

描述效果傳遞。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**pShaderVariable**
</dt> <dd>

類型： **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

此著色器來源的變數。

</dd> <dt>

**ShaderIndex**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

如果陣列) ，則為 pShaderVariable 的元素 (如果不適用則為0。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ PASS \_ 著色器 \_ DESC 適用于 [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc 方法。

如果這是內嵌著色器指派，則傳回的介面將會是匿名著色器變數，但無法以任何其他方式抓取。 變數描述中的名稱將會是 "$Anonymous"。 如果在 pass 區塊中沒有這個型別的指派，pShaderVariable！ = **Null**，但是 pShaderVariable->IsValid () = = **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

