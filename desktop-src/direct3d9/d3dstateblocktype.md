---
description: 狀態欄塊所使用的預先定義管線狀態組合 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: 'D3DSTATEBLOCKTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850181"
---
# <a name="d3dstateblocktype-enumeration"></a>D3DSTATEBLOCKTYPE 列舉

狀態欄塊所使用的預先定義管線狀態組合 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ 全部**
</dt> <dd>

捕捉目前的 [裝置狀態](saving-all-device-states-with-a-stateblock.md)。

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

捕捉目前的 [圖元狀態](saving-pixel-states-with-a-stateblock.md)。

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

捕捉目前的 [頂點狀態](saving-vertex-states-with-a-stateblock.md)。

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 請勿使用此值。

</dd> </dl>

## <a name="remarks"></a>備註

如下圖所示，頂點和圖元狀態都是裝置狀態的子集。

![裝置狀態的圖表，其頂點狀態和圖元狀態為子集](images/statesets.png)

只有幾個狀態會視為頂點和圖元狀態。 這些狀態包括：

-   轉譯狀態： D3DRS \_ FOGDENSITY
-   轉譯狀態： D3DRS \_ FOGSTART
-   轉譯狀態： D3DRS \_ FOGEND
-   材質狀態： D3DTSS \_ TEXCOORDINDEX
-   材質狀態： D3DTSS \_ TEXTURETRANSFORMFLAGS

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
