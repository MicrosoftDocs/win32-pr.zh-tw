---
description: 描述效果物件的傳遞。
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: 'D3DXPASS_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322636"
---
# <a name="d3dxpass_desc-structure"></a>D3DXPASS \_ DESC 結構

描述效果物件的傳遞。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

用於傳遞的字串值。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

批註是使用者特定的資料，可附加至任何技術、傳遞或參數。 請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

頂點著色器函式的指標。 如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，此結構會在由 [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)呼叫時傳回 **Null** 指標。

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

圖元著色器函式的指標。 如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，此結構會在由 [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)呼叫時傳回 **Null** 指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
