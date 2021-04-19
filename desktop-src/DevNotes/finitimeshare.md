---
description: 初始化 IME 共用。
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993421"
---
# <a name="finitimeshare-function"></a>FInitIMEShare 函式

初始化 IME 共用。

## <a name="syntax"></a>語法


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函數會在成功時傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

呼叫任何其他 IME 共用函式之前，應該先呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EndIMEShare**](endimeshare.md)
</dt> </dl>

 

 
