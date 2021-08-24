---
title: 'D3DX11_EFFECT_VARIABLE_DESC 結構 (D3dx11effect .h) '
description: 描述效果變數。
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a5362af8ea55abef2d8f29b3c464436938f33d138448d9affa2b29fe0cf1f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119378308"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>D3DX11 \_ 效果 \_ 變數 \_ DESC 結構

描述效果變數。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此變數、注釋或結構成員的名稱。

</dd> <dt>

**語義**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此變數或結構成員的語義字串 (注釋的 Null 或不存在) 。

</dd> <dt>

**旗標**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

適用于效果變數的選擇性旗標。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此變數的注釋數目 (永遠為0，表示注釋) 。

</dd> <dt>

**BufferOffset**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

包含 cbuffer 或 tbuffer 的位移 (永遠為0，適用于不在常數緩衝區) 的注釋或變數。

</dd> <dt>

**ExplicitBindPoint**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

如果已使用 register 關鍵字明確系結變數，則使用。 檢查 D3DX11 \_ 效果 \_ 變數 \_ 明確 \_ 綁定 \_ 點的旗標。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ 效果 \_ 變數 \_ DESC 可與 [**ID3DX11EffectVariable：： GetDesc**](id3dx11effectvariable-getdesc.md)搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

