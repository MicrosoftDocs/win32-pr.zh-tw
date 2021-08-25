---
description: 在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: f45ee39e9599e2d77d77131eb64c2a9037de1f4ba31f907ac5c9ea562a706c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032188"
---
# <a name="ntgetcurrentprocessornumber-function"></a>NtGetCurrentProcessorNumber 函式

\[**NtGetCurrentProcessorNumber** 可能會在未來的 Windows 版本中變更或無法使用。 應用程式應該改用 [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) 函數。\]

在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。

## <a name="syntax"></a>語法


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

函數會傳回目前的處理器號碼。

## <a name="remarks"></a>備註

此函數是用來提供用來評估進程效能的資訊。

此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[多個處理器](multiple-processors.md)
</dt> <dt>

[處理序和執行緒函式](process-and-thread-functions.md)
</dt> <dt>

[處理序](child-processes.md)
</dt> </dl>

 

 
