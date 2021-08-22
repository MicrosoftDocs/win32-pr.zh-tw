---
description: 將指定之執行緒所發出的暫止同步 i/o 作業標示為已取消。
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: 'CancelSynchronousIo 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582548"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo 函式

將指定之執行緒所發出的暫止同步 i/o 作業標示為已取消。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hThread* \[在\]
</dt> <dd>

執行緒的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果函式失敗，則傳回值為 0 (零) 。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

如果此函式找不到要取消的要求，則傳回值為 0 (零) ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 則找 **不到錯誤 \_ \_**。

## <a name="remarks"></a>備註

呼叫端必須讓 [執行緒 \_ 終止](/windows/desktop/ProcThread/thread-security-and-access-rights) 存取權。

如果指定的執行緒有任何正在進行的暫止 i/o 作業， **CancelSynchronousIo** 函式會將它們標示為取消。 大部分的作業類型都可以立即取消;其他作業可能會在實際取消之前繼續完成，並通知呼叫者。 **CancelSynchronousIo** 函數不會等候所有已取消的作業完成。 如需詳細資訊，請參閱 [I/o 完成/取消指導方針](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)。

正在取消的作業會以三個狀態之一完成：您必須檢查完成狀態以判斷完成狀態。 有三種狀態：

-   **作業正常完成。** 即使作業已取消，也可能會發生這種情況，因為取消要求可能尚未及時提交來取消作業。
-   **已取消作業。** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數傳回錯誤作業已 **\_ \_ 中止**。
-   **作業失敗，發生另一個錯誤。** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數會傳回相關的錯誤碼。

在 Windows 8 和 Windows Server 2012 中，下列技術支援此函數。



| 技術                                           | 支援      |
|------------------------------------------------------|----------------|
| 伺服器訊息區 (SMB) 3.0 通訊協定<br/>   | Yes<br/> |
| SMB 3.0 透明容錯移轉 (TFO) <br/>        | Yes<br/> |
| 具有向外延展檔案共用的 SMB 3.0 (因此) <br/>   | Yes<br/> |
| 叢集共用磁碟區檔案系統 (CsvFS) <br/> | Yes<br/> |
| 彈性檔案系統 (ReFS)<br/>              | Yes<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                                                                                                                                                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                                                                                                                                                                    |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista (的 WinBase .h 包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[同步和非同步 i/o](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

