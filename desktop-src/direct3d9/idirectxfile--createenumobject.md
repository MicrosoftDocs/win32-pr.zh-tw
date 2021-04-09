---
description: 建立列舉值物件。 已取代。
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile：： CreateEnumObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696776"
---
# <a name="idirectxfilecreateenumobject-method"></a>IDirectXFile：： CreateEnumObject 方法

建立列舉值物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvSource* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

其內容相依于 dwLoadOptions 值的資料指標

</dd> <dt>

*dwLoadOptions* \[在\]
</dt> <dd>

類型： **[ **DXFILELOADOPTIONS**](dxfile.md)**

指定資料來源的值。 這個值可以是 \_ [DXFILE 常數](dxfile.md)中的其中一個 DXFILELOAD xxx 旗標。

</dd> <dt>

*ppEnumObj* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

[**IDirectXFileEnumObject**](idirectxfileenumobject.md)介面指標的位址，表示已建立的枚舉器物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC、DXFILEERR \_ BADFILEFLOATSIZE、DXFILEERR \_ BADFILETYPE、DXFILEERR \_ BADFILEVERSION、DXFILEERR \_ BADRESOURCE、DXFILEERR \_ BADVALUE、DXFILEERR \_ FILENOTFOUND、DXFILEERR \_ RESOURCENOTFOUND、DXFILEERR \_ URLNOTFOUND。

## <a name="remarks"></a>備註

使用這個方法之後，請使用其中一個 IDirectXFileEnumObject 方法來取出資料物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
