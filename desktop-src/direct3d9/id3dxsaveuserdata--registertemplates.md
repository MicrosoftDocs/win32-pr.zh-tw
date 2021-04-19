---
description: 用來註冊. x 檔案範本的使用者回呼。
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData：： RegisterTemplates 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000366"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>ID3DXSaveUserData：： RegisterTemplates 方法

用來註冊. x 檔案範本的使用者回呼。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pXFileApi* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFILE**](id3dxfile.md)**

使用這個指標可註冊使用者定義的. x 檔案範本。 請參閱 [**ID3DXFile**](id3dxfile.md)。 請勿使用此參數來加入資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。

## <a name="remarks"></a>備註

**ID3DXSaveUserData：： RegisterTemplates** 和 [**ID3DXSaveUserData：： SaveTemplates**](id3dxsaveuserdata--savetemplates.md) 提供一種機制，可將範本加入至用來儲存使用者資料的. x 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
