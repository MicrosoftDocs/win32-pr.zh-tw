---
description: 描述鎖定的矩形區域。
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: 'D3DLOCKED_RECT 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514629"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ RECT 結構

描述鎖定的矩形區域。

## <a name="syntax"></a>語法


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>成員

<dl> <dt>

**瀝青**
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

介面中一個資料列的位元組數目。

</dd> <dt>

**pBits**
</dt> <dd>

類型： **void \***

</dd> <dd>

鎖定位的指標。 如果將 [**RECT**](/previous-versions//dd162897(v=vs.85)) 提供給 [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 呼叫，pBits 將會從表面的開頭開始進行適當的位移。

</dd> </dl>

## <a name="remarks"></a>備註

DXTn 格式的音調與 DirectX 7 中所傳回的格式不同。 它現在是指區塊資料列中的位元組數目。 例如，如果您的寬度是16，則會有4個區塊 (4 \* 個 DXT1，4 \* 16 DXT2-5。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
