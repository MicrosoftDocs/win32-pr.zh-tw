---
description: 包含紅色、綠色和藍色的斜坡資料。
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: 'D3DGAMMARAMP 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979879"
---
# <a name="d3dgammaramp-structure"></a>D3DGAMMARAMP 結構

包含紅色、綠色和藍色的斜坡資料。

## <a name="syntax"></a>語法


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>成員

<dl> <dt>

**紅**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述 red gamma 曲線的 256 WORD 元素陣列。

</dd> <dt>

**綠色**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述綠色 gamma 曲線的 256 WORD 元素陣列。

</dd> <dt>

**藍色**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述藍色 gamma 曲線的 256 WORD 元素陣列。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
