---
description: 取得建立這個 ID3DXFileSaveObject 物件之物件的 ID3DXFile 介面。
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject：： GetFile 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3f46344244405aca80789ae45db172e7693c6a01f77a014737a90080c1e3f21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121192"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a>ID3DXFileSaveObject：： GetFile 方法

取得建立這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)物件之物件的 [**ID3DXFile**](id3dxfile.md)介面。

## <a name="syntax"></a>語法


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppFile* \[在\]
</dt> <dd>

類型： **[ **ID3DXFile**](id3dxfile.md)**

[**ID3DXFile**](id3dxfile.md)物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE、e \_ NOINTERFACE、e \_ 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




