---
title: 'D3DX11_PASS_DESC 結構 (D3dx11effect .h) '
description: 描述包含管線狀態的效果階段。
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f00cc28e6ab901073e30abd2554046d61144c42af2217869c0b87dc6c19d29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124943"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ PASS \_ DESC 結構

描述包含管線狀態的效果階段。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

如果不是匿名) ，此傳遞的名稱 (**為 Null** 。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此傳遞的注釋數目。

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

從頂點著色器或幾何著色器 (的簽章（如果沒有頂點著色) 器，則為 Null），如果不存在則 **為 Null** 。

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Singature 大小（以位元組為單位）。

</dd> <dt>

**StencilRef**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

深度樣板狀態中所使用的樣板參考值。

</dd> <dt>

**SampleMask**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Blend 狀態的範例遮罩。

</dd> <dt>

**BlendFactor**
</dt> <dd>

類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Blend 狀態 (RGBA) 的每個元件 blend 因數。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ PASS \_ DESC 適用于 [**ID3DX11EffectPass：： GetDesc**](id3dx11effectpass-getdesc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

