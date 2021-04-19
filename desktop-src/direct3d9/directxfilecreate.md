---
description: 建立 DirectXFile 物件的實例。 已取代。
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: 'DirectXFileCreate 函式 (DXFile) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981816"
---
# <a name="directxfilecreate-function"></a>DirectXFileCreate 函式

建立 DirectXFile 物件的實例。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

類型： **[ **LPDIRECTXFILE**](idirectxfile.md)\***

[**IDirectXFile**](idirectxfile.md)介面指標的位址，表示已建立的 DirectXFile 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC，DXFILEERR \_ BADVALUE。

## <a name="remarks"></a>備註

使用此函式之後，請使用 [**RegisterTemplates**](idirectxfile--registertemplates.md) 來註冊範本、使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 來建立列舉值物件，或使用 [**CreateSaveObject**](idirectxfile--createsaveobject.md) 來建立儲存物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[X 檔案函數](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




