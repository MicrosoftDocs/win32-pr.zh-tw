---
description: 描述效果所使用的函數。
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: 'D3DXFUNCTION_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000593"
---
# <a name="d3dxfunction_desc-structure"></a>D3DXFUNCTION \_ DESC 結構

描述效果所使用的函數。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

函式名稱。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

未使用的。 [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)一律會將這個成員設定為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
