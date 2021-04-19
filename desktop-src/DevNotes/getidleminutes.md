---
description: 取得使用者的最後一個活動之後的時間長度（以分鐘為單位）。
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978663"
---
# <a name="getidleminutes-function"></a>GetIdleMinutes 函式

\[這項功能不受支援，而且可能會在未來變更或無法使用。 請改用 **GetLastInputInfo** 函數。\]

取得使用者的最後一個活動之後的時間長度（以分鐘為單位）。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>dwreserved* 
</dt> <dd>

此參數必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回使用者的最後一個活動之後的分鐘數。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。 此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數8。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
