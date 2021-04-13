---
description: 將資料物件和其子系儲存至磁片上的. x 檔案。
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject：： Save 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386457"
---
# <a name="id3dxfilesaveobjectsave-method"></a>ID3DXFileSaveObject：： Save 方法

將資料物件和其子系儲存至磁片上的. x 檔案。

## <a name="syntax"></a>語法


```C++
HRESULT Save();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列值： D3DXFERR \_ BADOBJECT。

## <a name="remarks"></a>備註

在這個方法成功之後，您就無法再呼叫 [**ID3DXFileSaveObject：： AddDataObject**](id3dxfilesaveobject--adddataobject.md)、 [**ID3DXFileSaveData：： AddDataObject**](id3dxfilesavedata--adddataobject.md) 和 [**ID3DXFileSaveData：： AddDataReference**](id3dxfilesavedata--adddatareference.md) ，直到建立新的 [**ID3DXFile**](id3dxfile.md) 物件為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




