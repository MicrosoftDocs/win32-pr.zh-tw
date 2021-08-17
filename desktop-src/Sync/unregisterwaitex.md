---
description: 取消 RegisterWaitForSingleObject 函式所發出的已註冊等候作業。
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: 'UnregisterWaitEx 函式 (Threadpoollegacyapiset) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 4181aa43cb0c2844f99b7ad81b448271366eb2925740c25d400f891389efb129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765519"
---
# <a name="unregisterwaitex-function"></a>UnregisterWaitEx 函式

取消 [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) 函式所發出的已註冊等候作業。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*WaitHandle* \[在\]
</dt> <dd>

等候控制碼。 [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)函數會傳回這個控制碼。

</dd> <dt>

*CompletionEvent* \[在中，選擇性\]
</dt> <dd>

在等候作業取消註冊時，要發出信號的事件物件控制碼。 此參數可以是 **Null**。

如果這個參數是 **不正確 \_ 控制碼 \_ 值**，則函式會先等候所有回呼函數完成，然後再傳回。

如果這個參數是 **Null**，函式會將計時器標示為刪除，並立即傳回。 不過，大部分的呼叫端應該等候回呼函式完成，才能執行任何所需的清除。

如果呼叫端提供此事件且函式成功，或函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，請不要關閉事件，直到收到信號為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

您無法在相同等候作業的回呼函式中進行 **UnregisterWaitEx** 封鎖呼叫。 否則回呼將會等待其本身完成。 一般來說，封鎖呼叫 **UnregisterWaitEx** 會在目前的執行緒與回呼之間建立相依性，因此若要在另一個等候作業上封鎖取消註冊呼叫，您必須確定回呼函式不會彼此相依，而且第二個等候作業也不會在第一次作業時執行封鎖取消註冊呼叫。

在持續性執行緒上進行封鎖 **UnregisterWaitEx** 呼叫時，請務必小心。 如果正在取消註冊的等候作業是使用 **Wt. \_ EXECUTEINPERSISTENTTHREAD** 所建立，則可能會發生鎖死。

在對 **UnregisterWaitEx** 進行非封鎖呼叫之後，不會將任何與 *WaitHandle* 相關聯的新回呼函式排入佇列。 不過，可能有暫止的回呼函式已排入工作者執行緒佇列中。

在某些情況下，如果 *CompletionEvent* 為 **Null**，函式將會失敗，而且 **錯誤 IO 會 \_ \_ 處於擱置狀態**。 這表示有未處理的回呼函數。 這些回呼可能會執行或正在執行中。

如果 *CompletionEvent* 是呼叫端所提供事件的控制碼，則函式可能會成功，因為 **錯誤 \_ IO \_ 暫** 止而失敗，或因不同的錯誤碼而失敗。 如果函式成功，或如果函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，則呼叫端應該一律等候，直到發出事件的信號關閉為止。 如果函式失敗，並出現不同的錯誤碼，就不需要等到事件被告知關閉事件。

**Windows XP：** 如果 *CompletionEvent* 是呼叫端所提供事件的控制碼，且此函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，則呼叫端應等候事件收到信號，以關閉事件。 從 Windows Vista 開始，此行為已變更。

若要編譯使用此函數的應用程式，請將 **\_ WIN32 \_ WINNT** 定義為0x0500 或更新版本。 如需詳細資訊，請參閱[使用 Windows 標頭](../winprog/using-the-windows-headers.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                                                                                                                    |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                                                                                                           |
| 標頭<br/>                   | <dl> <dt>Windows 8 與 Windows Server 2012 上的 Threadpoollegacyapiset .h (包含 Windows .h) ;</dt><dt>WinBase Windows 7、Windows Server 2008 R2、Windows Vista、Windows Server 2008、Windows XP 和 Windows server 2003 (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[同步處理函式](synchronization-functions.md)
</dt> <dt>

[執行緒共用](../procthread/thread-pooling.md)
</dt> </dl>

 

 
