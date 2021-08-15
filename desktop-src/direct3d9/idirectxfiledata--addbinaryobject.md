---
description: 建立二進位物件，並將它新增為子物件。 已取代。
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'IDirectXFileData：： AddBinaryObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d619fde6cd5d22f161188d46f710caeadfaedba2fbcf1167486e05dee539fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728974"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>IDirectXFileData：： AddBinaryObject 方法

建立二進位物件，並將它新增為子物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

物件名稱的指標。 如果物件不需要名稱，請指定 **Null** 。

</dd> <dt>

*pguid* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

代表物件之 GUID 的指標。 如果物件不需要 GUID，請指定 **Null** 。

</dd> <dt>

*szMimeType* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

物件之 MIME 類型的指標。

</dd> <dt>

*pvData* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

物件資料的指標。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

PvData 所指向的緩衝區大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary::GetMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
