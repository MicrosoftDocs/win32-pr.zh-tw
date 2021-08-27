---
description: 啟用傾印程式碼，從 Ntdll.dll 取得傾印中儲存的已卸載模組資訊。
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058588"
---
# <a name="rtlgetunloadeventtrace-function"></a>RtlGetUnloadEventTrace 函式

\[您可以從 Windows 中變更或移除此函式，而不需另行通知。\]

啟用傾印程式碼，從 Ntdll.dll 取得傾印中儲存的已卸載模組資訊。

## <a name="syntax"></a>語法


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函數會傳回陣列的指標。 如需詳細資訊，請參閱＜備註＞。

## <a name="remarks"></a>備註

RtlpUnloadEventTrace 陣列的定義如下：

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

此函數沒有相關聯的標頭檔。 相關聯的匯入程式庫（ntdll.dll）可在 Windows 驅動程式套件 (WDK) 中取得。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數呼叫這個函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
