---
description: 描述 (磁片區) 的鎖定箱。
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: 'D3DLOCKED_BOX 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196312"
---
# <a name="d3dlocked_box-structure"></a>D3DLOCKED \_ BOX 結構

描述 (磁片區) 的鎖定箱。

## <a name="syntax"></a>語法


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>成員

<dl> <dt>

**RowPitch**
</dt> <dd>

類型： **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

從某個資料列的左邊緣到下一個資料列的左邊緣的位元組位移。

</dd> <dt>

**SlicePitch**
</dt> <dd>

類型： **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

從一個配量左上角到下一個最深配量左上角的位元組位移。

</dd> <dt>

**pBits**
</dt> <dd>

類型： **void \***

</dd> <dd>

磁片區方塊開頭的指標。 如果將 [**D3DBOX**](d3dbox.md) 提供給加密箱呼叫，pBits 將會從磁片區的開頭適當地位移。

</dd> </dl>

## <a name="remarks"></a>備註

您可以將磁片區視覺化成寬度 x 高度2D 表面的配量，以形成寬度 x 高度 x 深度音量。 如需詳細資訊，請參閱 [ (Direct3D 9) 的音量材質資源 ](volume-texture-resources.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9：：加密箱**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9：：加密箱**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
