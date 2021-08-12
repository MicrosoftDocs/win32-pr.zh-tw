---
description: 使用者用來儲存. x 檔案範本的回呼。
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'ID3DXSaveUserData：： SaveTemplates 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00695f11f267c77838bc2d9a3d2932df108c7323f3751b385c009abe2b21f540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293104"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a>ID3DXSaveUserData：： SaveTemplates 方法

使用者用來儲存. x 檔案範本的回呼。

## <a name="syntax"></a>語法


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pXofSave* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

. X 檔儲存物件的指標。 請勿使用此參數來加入資料物件。 請參閱 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。

## <a name="remarks"></a>備註

[**ID3DXSaveUserData：： RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) 和 **ID3DXSaveUserData：： SaveTemplates** 提供一種機制，可將範本加入至用來儲存使用者資料的. x 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
