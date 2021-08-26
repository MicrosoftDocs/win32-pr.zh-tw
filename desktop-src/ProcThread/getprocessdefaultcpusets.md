---
description: 抓取 SetProcessDefaultCpuSets 所設定之進程預設集中的 CPU 集合清單。 如果未針對指定的進程設定預設的 CPU 集，則 RequiredIdCount 會設定為0，且函式會成功。
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: 'GetProcessDefaultCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3c5d71e4811411756719177647fda8dd76224f756629ad01794720d291565b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886698"
---
# <a name="getprocessdefaultcpusets-function"></a>GetProcessDefaultCpuSets 函式

抓取 [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)所設定之進程預設集中的 CPU 集合清單。 如果未針對指定的進程設定預設的 CPU 集，則 **RequiredIdCount** 會設定為0，且函式會成功。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*進程* \[在\]
</dt> <dd>

指定要查詢之進程的進程控制碼。 這個控制碼必須有「進程 \_ 查詢 \_ 限制的 \_ 資訊存取權」許可權。 您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。

</dd> <dt>

*CpuSetIds* \[out、optional\]
</dt> <dd>

指定一個選擇性的緩衝區，以抓取 CPU 組識別碼的清單。

</dd> <dt>

*CpuSetIdCount* \[在\]
</dt> <dd>

指定 **CpuSetIds** 中指定之緩衝區的容量。 如果緩衝區為 Null，則必須是0。

</dd> <dt>

*RequiredIdCount* \[擴展\]
</dt> <dd>

指定保留整個進程預設 CPU 集清單的緩衝區所需的容量。 在成功傳回時，這會指定填入緩衝區的識別碼數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此 API 會在成功時傳回 TRUE。 如果緩衝區不夠大，則 API 會傳回 FALSE，而 **GetLastError** 值是 \_ 緩衝區不足的錯誤 \_ 。 傳遞有效的參數且傳回緩衝區夠大時，此 API 無法失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Windows。h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

