---
description: 抓取物件之範本的 GUID。 已取代。
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'IDirectXFileData：： GetType 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 564d682c606d8b6bc0001f5d430d2d93f36c25210746169af4802512c330da08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292274"
---
# <a name="idirectxfiledatagettype-method"></a>IDirectXFileData：： GetType 方法

抓取物件之範本的 GUID。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppguid* \[退出，retval\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \* \***

接收物件的範本 GUID 之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




