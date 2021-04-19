---
description: 標示指定檔案控制代碼的任何未完成 i/o 作業。 此函式只會取消目前進程中的 i/o 作業，不論哪一個執行緒建立了 i/o 作業。
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: 'CancelIoEx 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976853"
---
# <a name="cancelioex-function"></a>CancelIoEx 函式

標示指定檔案控制代碼的任何未完成 i/o 作業。 此函式只會取消目前進程中的 i/o 作業，不論哪一個執行緒建立了 i/o 作業。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFile* \[在\]
</dt> <dd>

檔案的控制碼。

</dd> <dt>

*lpOverlapped* \[在中，選擇性\]
</dt> <dd>

重迭資料結構的指標，其中包含用於非同步 i/o [**的資料。**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

如果這個參數是 **Null**，就會取消 *hFile* 參數的所有 i/o 要求。

如果這個參數不是 **Null**，則只會將針對具有指定 *lpOverlapped* 重迭結構的檔案發出的特定 i/o 要求標示為已取消，這表示您可以取消一個或多個要求，而 [**CancelIo**](cancelio.md) 函式會取消檔案控制代碼上所有未處理的要求。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。 已成功要求指定檔案控制代碼之呼叫進程發出的所有暫止 i/o 作業的取消作業。 應用程式不能釋放或重複使用 [**與已**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 取消之 i/o 作業相關聯的重迭結構，直到它們完成為止。 執行緒可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷 i/o 作業本身何時完成。

如果函式失敗，則傳回值為 0 (零) 。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

如果此函式找不到要取消的要求，則傳回值為 0 (零) ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 則找 **不到錯誤 \_ \_**。

## <a name="remarks"></a>備註

**CancelIoEx** 函數可讓您取消呼叫執行緒以外線程中的要求。 [**CancelIo**](cancelio.md)函式只會取消呼叫 **CancelIo** 函式之相同執行緒中的要求。 **CancelIoEx** 只會取消控制碼上的未處理 i/o，而不會變更控制碼的狀態。這表示您無法依賴控制碼的狀態，因為您無法得知作業是否已順利完成或取消。

如果指定的檔案控制代碼有任何正在進行的暫止 i/o 作業， **CancelIoEx** 函式會將它們標示為取消。 大部分的作業類型都可以立即取消;其他作業可能會在實際取消之前繼續完成，並通知呼叫者。 **CancelIoEx** 函數不會等候所有已取消的作業完成。

如果檔案控制代碼與完成埠相關聯，且已成功取消同步作業，i/o 完成封包就不會排入埠佇列中。 如果非同步作業仍在擱置中，取消作業將會將 i/o 完成封包排在佇列中。

正在取消的作業會以三個狀態之一完成：您必須檢查完成狀態以判斷完成狀態。 有三種狀態：

-   作業正常完成。 即使作業已取消，也可能會發生這種情況，因為取消要求可能尚未及時提交來取消作業。
-   已取消作業。 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數傳回錯誤作業已 **\_ \_ 中止**。
-   作業失敗，發生另一個錯誤。 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數會傳回相關的錯誤碼。

在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。



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
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                                                                                                                                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                                                                                                                                                                                                             |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows Server 2008 和 Windows Vista (的 WinBase，包括 windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[解除擱置中的 i/o 作業](canceling-pending-i-o-operations.md)
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[同步和非同步 i/o](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

