---
description: 指定非色彩樣式是否具有粗體樣式。
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984814"
---
# <a name="fboldimestyle-function"></a>FBoldIMEStyle 函式

指定非色彩樣式是否具有粗體樣式。

## <a name="syntax"></a>語法


```C++
BOOL FBoldIMEStyle(
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

如果樣式具有粗體樣式，**則為 TRUE** 。

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

 

 
