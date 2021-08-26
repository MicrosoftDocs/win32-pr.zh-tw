---
description: 允許應用程式查詢系統上可用的 CPU 集，以及其目前的狀態。
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: 'GetSystemCpuSetInformation 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 011a809c78f2e94e6d16bbe5deb716ee7e97db356765bb771709048d3b00d05a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995368"
---
# <a name="getsystemcpusetinformation-function"></a>GetSystemCpuSetInformation 函式

允許應用程式查詢系統上可用的 CPU 集，以及其目前的狀態。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*資訊* \[out、optional\]
</dt> <dd>

[**系統 \_ cpu \_ 集合 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)結構的指標，此結構會接收 cpu 集資料。 以緩衝區長度0傳遞 Null，以決定所需的緩衝區大小。

</dd> <dt>

*BufferLength* \[在\]
</dt> <dd>

以位元組為單位的輸出緩衝區長度（以位元組為單位），以資訊引數形式傳遞。

</dd> <dt>

*ReturnedLength* \[擴展\]
</dt> <dd>

輸出緩衝區中有效資料的長度（以位元組為單位），如果緩衝區夠大或需要輸出緩衝區的大小。 如果沒有任何 CPU 集存在，此值會是0。

</dd> <dt>

*進程* \[在中，選擇性\]
</dt> <dd>

進程的選擇性控制碼。 此程式是用來判斷系統 \_ CPU \_ 集資訊結構中 AllocatedToTargetProcess 旗標的值 \_ 。 如果將 CPU 集合配置給指定的進程，就會設定旗標。 否則，它是明確的。 這個控制碼必須有「進程 \_ 查詢 \_ 限制的 \_ 資訊存取權」許可權。 您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。

</dd> <dt>

*旗標* 
</dt> <dd>

保留，必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 API 成功，則會傳回 TRUE。 如果失敗，則可透過 **GetLastError** 取得錯誤原因。 如果資訊緩衝區為 Null 或不夠大，則會傳回錯誤碼錯誤的 \_ \_ 緩衝區。 當傳遞有效的參數和足以容納所有傳回資料的緩衝區時，此 API 無法失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Windows。h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

