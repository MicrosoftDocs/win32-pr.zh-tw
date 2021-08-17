---
description: 指定如何旋轉用來顯示全螢幕應用程式的監視器。
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: 'D3DDISPLAYROTATION 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8defdc206e88750125d88c50e86484428c0dedbd7c18575e26504d7445cd3f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804932"
---
# <a name="d3ddisplayrotation-enumeration"></a>D3DDISPLAYROTATION 列舉

指定如何旋轉用來顯示全螢幕應用程式的監視器。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION 身分 \_ 識別**
</dt> <dd>

顯示未旋轉。

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

顯示旋轉90度。

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

顯示旋轉180度。

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

顯示旋轉270度。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉用於 [**IDirect3D9Ex：： GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex)、 [**IDirect3DDevice9Ex：： GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)和 [**IDirect3DSwapChain9Ex：： GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex)。

應用程式可以選擇使用 [D3DPRESENTFLAG \_ NOAUTOROTATE](d3dpresentflag.md)來處理監視器輪替本身，在這種情況下，應用程式將需要知道監視器的旋轉方式，讓它能夠據以調整其轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




