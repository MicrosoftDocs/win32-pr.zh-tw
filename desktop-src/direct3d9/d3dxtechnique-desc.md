---
description: 描述效果所使用的技術。
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: 'D3DXTECHNIQUE_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035342"
---
# <a name="d3dxtechnique_desc-structure"></a>D3DXTECHNIQUE \_ DESC 結構

描述效果所使用的技術。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

包含技術名稱的字串。

</dd> <dt>

**通過**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此技術所需的轉譯行程數目。 請參閱＜備註＞。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

注釋的數目。 請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。

</dd> </dl>

## <a name="remarks"></a>備註

有些視訊卡可以在單一階段中轉譯兩個材質。 但是，如果卡片沒有這項功能，通常可以在兩個階段中轉譯相同的效果，每次行程都使用一個材質。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
