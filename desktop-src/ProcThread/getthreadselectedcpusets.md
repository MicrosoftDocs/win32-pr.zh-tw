---
description: 如果已使用 SetThreadSelectedCpuSets API 設定任何指派，則會傳回指定執行緒的明確 CPU 集指派。 如果未設定明確指派，RequiredIdCount 會設為0，且函數會傳回 TRUE。
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: 'GetThreadSelectedCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978778"
---
# <a name="getthreadselectedcpusets-function"></a>GetThreadSelectedCpuSets 函式

如果已使用 [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API 設定任何指派，則會傳回指定執行緒的明確 CPU 集指派。 如果未設定明確指派， **RequiredIdCount** 會設為0，且函數會傳回 TRUE。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*執行緒* \[在\]
</dt> <dd>

指定要查詢所選 CPU 集的執行緒。 這個控制碼的 \_ 存取權必須限制為執行緒查詢的 \_ 有限 \_ 資訊。 您也可以在這裡指定 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 所傳回的值。

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

指定緩衝區的必要容量，以保存完整的執行緒選取的 CPU 集合清單。 在成功傳回時，這會指定填入緩衝區的識別碼數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此 API 會在成功時傳回 TRUE。 如果緩衝區不夠大，則 **GetLastError** 值是緩衝區不足的錯誤 \_ \_ 。 傳遞有效的參數且傳回緩衝區夠大時，此 API 無法失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Windows。h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

