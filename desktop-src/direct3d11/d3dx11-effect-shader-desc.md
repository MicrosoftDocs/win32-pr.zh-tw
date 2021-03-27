---
title: 'D3DX11_EFFECT_SHADER_DESC 結構 (D3dx11effect .h) '
description: 描述效果著色器。
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854067"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>D3DX11 \_ 效果 \_ 著色器 \_ DESC 結構

描述效果著色器。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**pInputSignature**
</dt> <dd>

類型： **Const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

傳遞至 CreateInputLayout。 只適用于頂點著色器或幾何著色器。 請參閱 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)。

</dd> <dt>

**IsInline**
</dt> <dd>

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**TRUE** 表示著色器是以內嵌方式定義的。否則 **為 FALSE**。

</dd> <dt>

**pBytecode**
</dt> <dd>

類型： **Const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

著色器位元組的位元組。

</dd> <dt>

**BytecodeLength**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

PBytecode 的長度。

</dd> <dt>

**SODecls**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

使用) 將幾何著色器的宣告字串 (資料流程。

</dd> <dt>

**RasterizedStream**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出哪些資料流程是柵格化的。 D3D11 幾何著色器最多可以輸出四個數據流，其中一個可以進行柵格化。

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輸入簽章中的專案數。

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輸出特徵標記中的專案數。

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Patch 常數簽章中的專案數。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ 效果 \_ 著色器 \_ DESC 適用于 [**ID3DX11EffectShaderVariable：： GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

