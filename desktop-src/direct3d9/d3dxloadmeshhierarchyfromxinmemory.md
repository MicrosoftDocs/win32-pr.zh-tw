---
description: D3DXLoadMeshHierarchyFromXInMemory 函式-從. x 檔案載入第一個框架階層。
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: 'D3DXLoadMeshHierarchyFromXInMemory 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85929a4cca88d9547ac0f00861f694932c7566cb3b6f5db6d4e6da189842e712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564808"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>D3DXLoadMeshHierarchyFromXInMemory 函式

從. x 檔案載入第一個框架階層。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMemory* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含網格階層之緩衝區的指標。

</dd> <dt>

*SizeOfMemory* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

PMemory 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*MeshOptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，可指定網格的建立選項。

</dd> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。

</dd> <dt>

*pAlloc* \[在\]
</dt> <dd>

類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

[**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)介面的指標。

</dd> <dt>

*pUserDataLoader* \[在\]
</dt> <dd>

類型： **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

應用程式提供的介面，可讓使用者資料載入。 請參閱 [**ID3DXLoadUserData**](id3dxloaduserdata.md)。

</dd> <dt>

*ppFrameHeirarchy* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)\***

傳回已載入框架階層的指標。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

</dd> <dt>

*ppAnimController* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

傳回與. x 檔案中的動畫相對應的動畫控制器指標。 這會使用預設的追蹤和事件來建立。 請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

檔案中的所有網格都將折迭成一個輸出網格。 如果檔案包含框架階層，則所有轉換都會套用至網格。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
