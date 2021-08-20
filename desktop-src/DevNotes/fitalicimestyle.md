---
description: 指定非色彩樣式是否具有斜體樣式。
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c8160edf46b97544ef27558bf15a8a58e447e78a0e0709432aea840f4567bc0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076112"
---
# <a name="fitalicimestyle-function"></a>FItalicIMEStyle 函式

指定非色彩樣式是否具有斜體樣式。

## <a name="syntax"></a>語法


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pimestyle* \[在\]
</dt> <dd>

從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果樣式具有斜體樣式，**則為 TRUE** 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
