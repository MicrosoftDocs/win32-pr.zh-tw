---
description: 為指定的執行緒設定選取的 CPU 集合指派。 此指派會覆寫進程預設指派（如果有設定）。
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: 'SetThreadSelectedCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849261"
---
# <a name="setthreadselectedcpusets-function"></a>SetThreadSelectedCpuSets 函式

為指定的執行緒設定選取的 CPU 集合指派。 此指派會覆寫進程預設指派（如果有設定）。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*執行緒* \[在\]
</dt> <dd>

指定要設定 CPU 集合指派的執行緒。 這個控制碼必須設定執行緒 \_ 的 \_ 有限 \_ 資訊存取權限。 也可以使用 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 傳回的值。

</dd> <dt>

*CpuSetIds* \[在\]
</dt> <dd>

指定要設定為執行緒所選 CPU 集的 CPU 集識別碼清單。 如果這是 Null，則 API 會清除任何指派，如果有設定，則會還原為處理預設指派。

</dd> <dt>

*CpuSetIdCount* \[在\]
</dt> <dd>

指定在 **CpuSetIds** 引數中傳遞之清單中的識別碼數目。 如果該值為 Null，則應為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳遞的有效參數時，此函式不能失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016 \[ desktop app \| UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Windows。h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
