---
description: 識別指定的非色彩樣式是否有底線。
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001921"
---
# <a name="idulimestyle-function"></a>IdUlIMEStyle 函式

識別指定的非色彩樣式是否有底線。

## <a name="syntax"></a>語法


```C++
UINT __cdecl IdUlIMEStyle(
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

此函數可以傳回下列其中一個值。

<dl> <dt>

**IMESTY \_UL \_ MIN** (2002) 
</dt> <dt>

**IMESTY \_UL \_ 無** (2002) 
</dt> <dt>

**IMESTY \_UL \_ SINGLE** (2003) 
</dt> <dt>

**IMESTY \_UL \_ 虛線** (2005) 
</dt> <dt>

**IMESTY \_UL \_ 厚** (2006) 
</dt> <dt>

**IMESTY \_UL \_ 低** (2011) 
</dt> <dt>

**IMESTY \_UL \_ THICKLOWER** (2012) 
</dt> <dt>

**IMESTY \_UL \_ THICKDITHLOWER** (2013) 
</dt> <dt>

**IMESTY \_UL \_ DITHLOWER** (2014) 
</dt> <dt>

**IMESTY \_UL \_ MAX** (2014) 
</dt> </dl>

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

 

 
