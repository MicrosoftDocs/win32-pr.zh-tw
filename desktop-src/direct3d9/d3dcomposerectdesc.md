---
description: 指定在單色介面上用來括住字元的矩形。
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: 'D3DCOMPOSERECTDESC 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386434"
---
# <a name="d3dcomposerectdesc-structure"></a>D3DCOMPOSERECTDESC 結構

指定在單色介面上用來括住字元的矩形。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>成員

<dl> <dt>

**X**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

開始複製的左座標。

</dd> <dt>

**Y**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

開始複製的上座標。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

從左座標的材質數目。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

從上座標開始的材質數目。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是用來呼叫 [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) ，以括住來源介面上的字元。 頂點緩衝區 (看到以這些結構填入的 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) 會建立成包含字元位置。 USHORT 成員是用來盡可能減少記憶體使用量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
