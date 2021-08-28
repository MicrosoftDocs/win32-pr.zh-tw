---
description: 解析資料參考。 已取代。
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'IDirectXFileDataReference：： Resolve 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a20612eec88e2370914a93d851b0ce9047823b415951a8f5558cafb6dfaf1eb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985138"
---
# <a name="idirectxfiledatareferenceresolve-method"></a>IDirectXFileDataReference：： Resolve 方法

解析資料參考。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDataObj* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileDataReference](idirectxfiledatareference.md)
</dt> </dl>

 

 




