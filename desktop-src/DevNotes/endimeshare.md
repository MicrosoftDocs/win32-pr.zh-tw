---
description: 終止 IME 共用。
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 079a8719aa8e48e8ae880f2ce2a83d5e4d0f89fda85298ec015a3f77acebeb9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653438"
---
# <a name="endimeshare-function"></a>EndIMEShare 函式

終止 IME 共用。

## <a name="syntax"></a>語法


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

呼叫最後一個 IME 共用函式之後，應該呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FInitIMEShare**](finitimeshare.md)
</dt> </dl>

 

 
