---
description: 要求解除配置網格容器物件。
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: 'ID3DXAllocateHierarchy：:D estroyMeshContainer 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514705"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>ID3DXAllocateHierarchy：:D estroyMeshContainer 方法

要求解除配置網格容器物件。

## <a name="syntax"></a>語法


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshContainerToFree* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

要解除配置之網狀容器物件的指標。

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

 

 




