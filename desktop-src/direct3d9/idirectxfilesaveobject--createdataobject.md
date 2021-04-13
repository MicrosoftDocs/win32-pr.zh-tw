---
description: 建立資料物件。 已取代。
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject：： CreateDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322847"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>IDirectXFileSaveObject：： CreateDataObject 方法

建立資料物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rguidTemplate* \[在\]
</dt> <dd>

類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

代表資料物件之範本的 GUID。

</dd> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

資料物件名稱的指標。 如果物件沒有名稱，請指定 **Null** 。

</dd> <dt>

*pguid* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

代表資料物件之 GUID 的指標。 如果物件沒有 GUID，請指定 **Null** 。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

資料物件的大小（以位元組為單位）。

</dd> <dt>

*pvData* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

包含所有必要成員資料之緩衝區的指標。

</dd> <dt>

*ppDataObj* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示所建立的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>備註

如果資料參考物件將參考資料物件，則 >szname 或 pguid 參數都必須為非 **Null**。

儲存這個方法所建立的資料之前，請先使用 [**IDirectXFileSaveObject：： SaveTemplates**](idirectxfilesaveobject--savetemplates.md) 方法儲存任何範本。 使用 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md) 方法儲存建立的資料。

如果您需要儲存選擇性資料，請在使用此方法之後，以及使用 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md)之前，使用 [**IDirectXFileData：： AddDataObject**](idirectxfiledata--adddataobject.md)方法。 如果物件有子物件，請在呼叫 **IDirectXFileSaveObject：： SaveData** 之前加入它們。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
