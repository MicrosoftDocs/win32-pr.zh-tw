---
description: 將資料物件和其子系儲存至 DirectX 檔案。 已取代。
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'IDirectXFileSaveObject：： SaveData 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 293525d570540e00da4e8ac7680cf850b253c7e3ccbe3ffd152b639d0bc139cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747268"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>IDirectXFileSaveObject：： SaveData 方法

將資料物件和其子系儲存至 DirectX 檔案。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataObj* \[在\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

[**IDirectXFileData**](idirectxfiledata.md)介面的指標，代表要儲存的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADARRAYSIZE，DXFILEERR \_ BADVALUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




