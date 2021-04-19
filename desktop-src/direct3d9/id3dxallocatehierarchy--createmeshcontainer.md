---
description: 要求配置網格容器物件。
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy：： CreateMeshContainer 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988164"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>ID3DXAllocateHierarchy：： CreateMeshContainer 方法

要求配置網格容器物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

網格的名稱。

</dd> <dt>

*pMeshData* \[在\]
</dt> <dd>

Type： **Const [**D3DXMESHDATA**](d3dxmeshdata.md) \***

網格資料結構的指標。 請參閱 [**D3DXMESHDATA**](d3dxmeshdata.md)。

</dd> <dt>

*pMaterials* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATERIAL**](d3dxmaterial.md) \***

網格中所使用的材質陣列。

</dd> <dt>

*pEffectInstances* \[在\]
</dt> <dd>

Type： **Const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

網格中使用的效果實例陣列。 請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。

</dd> <dt>

*NumMaterials* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

材質陣列中的材質數目。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

網格的相鄰陣列。

</dd> <dt>

*pSkinInfo* \[在\]
</dt> <dd>

類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

如果找到面板資料，則為外觀網格物件的指標。 請參閱 [**ID3DXSkinInfo**](id3dxskininfo.md)。

</dd> <dt>

*ppNewMeshContainer* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

傳回已建立的網狀容器。 請參閱 [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
