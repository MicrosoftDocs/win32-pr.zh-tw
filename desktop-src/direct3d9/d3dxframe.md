---
description: 封裝轉換框架階層中的轉換框架。
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: 'D3DXFRAME 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196258"
---
# <a name="d3dxframe-structure"></a>D3DXFRAME 結構

封裝轉換框架階層中的轉換框架。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **LPSTR**

</dd> <dd>

框架的名稱。

</dd> <dt>

**TransformationMatrix**
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

轉換矩陣。

</dd> <dt>

**pMeshContainer**
</dt> <dd>

類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

網格容器的指標。

</dd> <dt>

**pFrameSibling**
</dt> <dd>

類型： * * * * D3DXFRAME **\***

</dd> <dd>

指向同級框架的指標。

</dd> <dt>

**pFrameFirstChild**
</dt> <dd>

類型： * * * * D3DXFRAME **\***

</dd> <dd>

子框架的指標。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式可以從此結構衍生，以新增其他資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




