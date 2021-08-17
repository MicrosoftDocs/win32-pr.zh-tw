---
description: 效果預設參數。
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: 'D3DXEFFECTDEFAULT 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 41beda43807ace6b0f335dc1937f8843cbc11544e4842f86af98eb0e0bb0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731877"
---
# <a name="d3dxeffectdefault-structure"></a>D3DXEFFECTDEFAULT 結構

效果預設參數。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>成員

<dl> <dt>

**pParamName**
</dt> <dd>

類型： **LPSTR**

</dd> <dd>

參數名稱。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

PValue 中的資料類型。 如需詳細資訊，請參閱 [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

PValue 所指向之資料的大小（以位元組為單位）。

</dd> <dt>

**pValue**
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

包含資料之記憶體位置的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
