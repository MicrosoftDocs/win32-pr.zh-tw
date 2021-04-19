---
description: 指定要在單色介面中複製字元的來源字元和位置。
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: 'D3DCOMPOSERECTDESTINATION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982199"
---
# <a name="d3dcomposerectdestination-structure"></a>D3DCOMPOSERECTDESTINATION 結構

指定要在單色介面中複製字元的來源字元和位置。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>成員

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

從包含 [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) 結構的頂點緩衝區索引特定圖像。

</dd> <dt>

**已保留**
</dt> <dd>

類型： **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

保留以供對齊之用。

</dd> <dt>

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

</dd> </dl>

## <a name="remarks"></a>備註

此結構是用來呼叫 [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) ，以指出應該將位置圖像複製到的位置，以及應該複製的特定圖像。 頂點緩衝區 (看到以這些結構填入的 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) 會建立成包含字元位置。 USHORT 成員是用來盡可能減少記憶體使用量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
