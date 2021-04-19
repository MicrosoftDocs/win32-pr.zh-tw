---
description: 讓偵錯工具檢查動態函數資料表資訊。
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979456"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>RtlGetFunctionTableListHead 函式

\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]

讓偵錯工具檢查動態函數資料表資訊。

## <a name="syntax"></a>語法


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

傳回函式資料表清單開頭的指標。

## <a name="remarks"></a>備註

請注意，某些定義必須有 Windows 驅動程式套件 (WDK) 標頭檔 Ntdef。 相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
