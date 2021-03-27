---
title: 'D3DX11_TECHNIQUE_DESC 結構 (D3dx11effect .h) '
description: 描述效果技巧。
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696731"
---
# <a name="d3dx11_technique_desc-structure"></a>D3DX11 \_ 技術 \_ DESC 結構

描述效果技巧。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

這項技術的名稱 (Null （如果不是匿名) ）。

</dd> <dt>

**通過**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

技術中包含的傳遞數目。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

這項技術的附注數目。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ 技術 \_ DESC 適用于 [**ID3DX11EffectTechnique：： GetDesc**](id3dx11effecttechnique-getdesc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

