---
description: 針對指定進程中的執行緒，設定預設的 CPU 集合指派。 建立的執行緒如果沒有使用 SetThreadSelectedCpuSets 明確設定的 CPU 集，將會自動繼承 SetProcessDefaultCpuSets 所指定的集合。
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: 'SetProcessDefaultCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793175"
---
# <a name="setprocessdefaultcpusets-function"></a>SetProcessDefaultCpuSets 函式

針對指定進程中的執行緒，設定預設的 CPU 集合指派。 建立的執行緒如果沒有使用 [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)明確設定的 CPU 集，將會自動繼承 **SetProcessDefaultCpuSets** 所指定的集合。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*進程* \[在\]
</dt> <dd>

指定要設定預設 CPU 集的進程。 這個控制碼必須有進程 \_ 集的 \_ 有限 \_ 資訊存取權限。 您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。

</dd> <dt>

*CpuSetIds* \[在中，選擇性\]
</dt> <dd>

指定要設定為進程預設 CPU 集的 CPU 集識別碼清單。 如果這是 Null，則 **SetProcessDefaultCpuSets** 會清除任何指派。

</dd> <dt>

*CpuSetIdCound* \[在\]
</dt> <dd>

指定在 **CpuSetIds** 引數中傳遞之清單中的識別碼數目。 如果該值為 Null，則應為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳遞的有效參數時，此函式不能失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Windows。h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
