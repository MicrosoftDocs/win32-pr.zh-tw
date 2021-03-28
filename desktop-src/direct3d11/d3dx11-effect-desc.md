---
title: 'D3DX11_EFFECT_DESC 結構 (D3dx11effect .h) '
description: 描述效果。
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974717"
---
# <a name="d3dx11_effect_desc-structure"></a>D3DX11 \_ 效果 \_ DESC 結構

描述效果。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此效果中的常數緩衝區數目。

</dd> <dt>

**GlobalVariables**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此效果中的全域變數數目。

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此效果中的全域介面數目。

</dd> <dt>

**技術**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此效果中的技巧數目。

</dd> <dt>

**群組**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此效果中的群組數目。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ 效果 \_ DESC 適用于 [**ID3DX11Effect：： GetDesc**](id3dx11effect-getdesc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

