---
description: 取消所有暫止的輸入和輸出 (由呼叫執行緒針對指定檔案發出的 i/o) 作業。
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: 'CancelIo 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001698"
---
# <a name="cancelio-function"></a>CancelIo 函式

取消所有暫止的輸入和輸出 (由呼叫執行緒針對指定檔案發出的 i/o) 作業。 此函數不會取消其他執行緒針對檔案控制代碼發出的 i/o 作業。

若要取消另一個執行緒的 i/o 作業，請使用 [**CancelIoEx**](cancelioex-func.md) 函數。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFile* \[在\]
</dt> <dd>

檔案的控制碼。

此函式會取消此檔案控制代碼的所有暫止 i/o 作業。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。 已成功要求呼叫執行緒針對指定檔案控制代碼發出的所有暫止 i/o 作業的取消作業。 執行緒可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷 i/o 作業本身何時完成。

如果函式失敗，則傳回值為零 (0) 。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

## <a name="remarks"></a>備註

如果指定的檔案控制代碼有任何正在進行的暫止 i/o 作業，而且這些作業是由呼叫執行緒所發出，則 **CancelIo** 函式會將它們取消。 **CancelIo** 只會取消控制碼上的未處理 i/o，而不會變更控制碼的狀態。這表示您無法依賴控制碼的狀態，因為您無法得知作業是否已順利完成或取消。

I/o 作業必須發出為重迭的 i/o。 如果不是，i/o 作業就不會傳回，讓執行緒呼叫 **CancelIo** 函式。 使用未以檔案 **\_ 旗 \_** 標重迭開啟的檔案控制代碼來呼叫 CancelIo 函式不會執行任何動作。

所有已取消且錯誤錯誤作業完成的 i/o 作業都會 **\_ \_ 中止**，且 i/o 作業的所有完成通知都會正常執行。

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2003 \[ desktop app \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP (的 WinBase，包括 windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[同步和非同步 i/o](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

