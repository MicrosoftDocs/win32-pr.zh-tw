---
description: 從 DLL 取得函數的位址。
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000948"
---
# <a name="_getprocaddress_-function"></a>\_GetProcAddress \_ 函數

\[此函式是在 **GetProcAddress** 函數上的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **GetProcAddress** 。\]

從 DLL 取得函數的位址。 請參閱 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)。

## <a name="syntax"></a>語法


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
