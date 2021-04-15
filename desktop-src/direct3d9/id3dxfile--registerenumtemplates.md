---
description: 在給定 ID3DXFileEnumObject 列舉物件的情況下註冊自訂範本。
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile：： RegisterEnumTemplates 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386484"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>ID3DXFile：： RegisterEnumTemplates 方法

在給定 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的情況下註冊自訂範本。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEnum* \[在\]
</dt> <dd>

類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

包含範本之 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。

如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。

## <a name="remarks"></a>備註

當呼叫這個方法時，它會將以 ID3DXFileEnumObject 儲存的範本（代表檔案）複製到 [**ID3DXFile**](id3dxfile.md) 物件的本機範本存放區。

如果無法使用 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 指標，請改為呼叫 [**RegisterTemplates**](id3dxfile--registertemplates.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




