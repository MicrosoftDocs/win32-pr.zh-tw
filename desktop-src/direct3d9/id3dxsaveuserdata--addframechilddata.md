---
description: 將子資料新增至框架。
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData：： AddFrameChildData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196430"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>ID3DXSaveUserData：： AddFrameChildData 方法

將子資料新增至框架。

## <a name="syntax"></a>語法


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrame* \[在\]
</dt> <dd>

Type： **Const [**D3DXFRAME**](d3dxframe.md) \***

網格容器的指標。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

</dd> <dt>

*pXofSave* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

. X 檔儲存物件的指標。 使用指標來呼叫 [**ID3DXFileSaveObject：： AddDataObject**](id3dxfilesaveobject--adddataobject.md) ，以加入子資料物件。 請勿使用 [**ID3DXFileSaveObject：： save**](id3dxfilesaveobject--save.md)來儲存資料。

</dd> <dt>

*pXofFrameData* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

. X 檔案資料節點的指標。 使用指標來呼叫 [**ID3DXFileSaveData：： AddDataObject**](id3dxfilesavedata--adddataobject.md) ，以加入子資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。

## <a name="remarks"></a>備註

[**ID3DXSaveUserData：： RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) 和 [**ID3DXSaveUserData：： SaveTemplates**](id3dxsaveuserdata--savetemplates.md) 提供一種機制，可將範本加入至用來儲存使用者資料的. x 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
