---
title: 'D3DX11_GROUP_DESC 結構 (D3dx11effect .h) '
description: 描述效果群組。
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035434"
---
# <a name="d3dx11_group_desc-structure"></a>D3DX11 \_ 群組 \_ DESC 結構

描述效果群組。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此群組的名稱 (只有在全域) 時才會是 **Null** 。

</dd> <dt>

**技術**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

群組中包含的技術數目。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

此群組的注釋數目。

</dd> </dl>

## <a name="remarks"></a>備註

D3DX11 \_ GROUP \_ DESC 可與 [**ID3DX11EffectTechnique：： GetDesc**](id3dx11effecttechnique-getdesc.md)搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

