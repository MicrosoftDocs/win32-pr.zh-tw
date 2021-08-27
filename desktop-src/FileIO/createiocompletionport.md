---
description: 建立輸入/輸出 (i/o) 完成埠，並將其與指定的檔案控制代碼建立關聯，或建立尚未與檔案控制代碼相關聯的 i/o 完成埠，以便於稍後建立關聯。
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: 'CreateIoCompletionPort 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083158"
---
# <a name="createiocompletionport-function"></a>CreateIoCompletionPort 函式

建立輸入/輸出 (i/o) 完成埠，並將其與指定的檔案控制代碼建立關聯，或建立尚未與檔案控制代碼相關聯的 i/o 完成埠，以便於稍後建立關聯。

將開啟的檔案控制代碼的實例與 i/o 完成埠相關聯，可讓進程接收與該檔案控制代碼相關之非同步 i/o 作業的完成通知。

> [!Note]
>
> 此處所用的詞彙 *檔案控制代碼* 是指代表重迭 i/o 端點的系統抽象，而不只是磁片上的檔案。 任何支援重迭 i/o 的系統物件（例如網路端點、TCP 通訊端、具名管道和郵件位置）都可以用來做為檔案控制代碼。 如需詳細資訊，請參閱「備註」一節。

 

## <a name="syntax"></a>語法


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileHandle* \[在\]
</dt> <dd>

開啟的檔案控制代碼或 **不正確 \_ 控制碼 \_ 值**。

控制碼必須是支援重迭 i/o 的物件。

如果有提供控制碼，它必須已針對重迭的 i/o 完成開啟。 例如，使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函數取得控制碼時，您必須指定檔案 **\_ 旗 \_** 標重迭旗標。

如果指定了 **不正確 \_ 控制碼 \_ 值** ，函式就會建立 i/o 完成埠，而不會將它與檔案控制代碼建立關聯。 在此情況下， *ExistingCompletionPort* 參數必須為 **Null** ，而且會忽略 *CompletionKey* 參數。

</dd> <dt>

*ExistingCompletionPort* \[在中，選擇性\]
</dt> <dd>

現有 i/o 完成埠的控制碼或 **Null**。

如果這個參數指定現有的 i/o 完成通訊埠，則函式會將它與 *FileHandle* 參數所指定的控制碼產生關聯。 如果成功，函數會傳回現有 i/o 完成埠的控制碼;它不會建立新的 i/o 完成通訊埠。

如果此參數為 **Null**，此函式會建立新的 i/o 完成埠，而且如果 *FileHandle* 參數有效，就會將它與新的 i/o 完成通訊埠產生關聯。 否則，就不會發生檔案控制代碼關聯。 如果成功，函數會將控制碼傳回至新的 i/o 完成埠。

</dd> <dt>

*CompletionKey* \[在\]
</dt> <dd>

針對指定檔案控制代碼，每個 i/o 完成封包中包含的每個處理常式使用者定義的完成索引鍵。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

*NumberOfConcurrentThreads* \[在\]
</dt> <dd>

作業系統可允許同時處理 i/o 完成埠之 i/o 完成封包的執行緒數目上限。 如果 *ExistingCompletionPort* 參數不是 **Null**，則會忽略這個參數。

如果此參數為零，則系統會允許多個同時執行的執行緒，就像系統中的處理器一樣。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是 i/o 完成埠的控制碼：

-   如果 *ExistingCompletionPort* 參數為 **Null**，則傳回值為新的控制碼。

-   如果 *ExistingCompletionPort* 參數是有效的 i/o 完成通訊埠控制碼，則傳回值會是相同的控制碼。

-   如果 *FileHandle* 參數是有效的控制碼，該檔案控制代碼現在會與傳回的 i/o 完成埠相關聯。

如果函式失敗，則傳回值為 **Null**。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

## <a name="remarks"></a>備註

系統可以指示 i/o 系統將 i/o 完成通知封包傳送至 i/o 完成埠，以將它們排入佇列。 **CreateIoCompletionPort** 函式會提供這種功能。

I/o 完成埠及其控制碼會與建立它的進程相關聯，而且在進程間無法共用。 不過，在相同進程中的執行緒之間可共用單一控制碼。

**CreateIoCompletionPort** 可用於三種不同的模式：

-   只建立 i/o 完成埠，而不將它與檔案控制代碼建立關聯。
-   將現有的 i/o 完成埠與檔案控制代碼建立關聯。
-   在單一呼叫中執行建立和關聯。

若要建立 i/o 完成埠而不建立其關聯，請將 *FileHandle* 參數設定 **為不正確 \_ 控制碼 \_ 值**、將 *ExistingCompletionPort* 參數設定為 **Null**，並將 *CompletionKey* 參數設定為零 (在此情況下會忽略) 。 針對新的 i/o 完成通訊埠，將 *NumberOfConcurrentThreads* 參數設定為所需的並行值，或針對預設 (系統) 中的處理器數目為零。

在 *FileHandle* 參數中傳遞的控制碼可以是任何支援重迭 i/o 的控制碼。 最常見的情況是，這是 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式使用檔案 **\_ 旗 \_** 標重迭旗標所開啟的控制碼 (例如，檔案、郵件位置和管道) 。 其他函式（例如 [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket) ）所建立的物件也可以與 i/o 完成埠相關聯。 如需使用通訊端的範例，請參閱 [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)。 控制碼只能與一個 i/o 完成埠相關聯，且在建立關聯之後，控制碼會維持與該 i/o 完成埠相關聯，直到它關閉為止。

如需 i/o 完成埠理論、使用方式和相關聯函式的詳細資訊，請參閱 [I/o 完成埠](i-o-completion-ports.md)。

多個檔案控制代碼可以與單一 i/o 完成埠相關聯，方法是使用 *ExistingCompletionPort* 參數中的相同 i/o 完成埠控制碼多次呼叫 **CreateIoCompletionPort** ，以及每次 *FileHandle* 參數中的不同檔案控制代碼。

使用 *CompletionKey* 參數有助於您的應用程式追蹤已完成的 i/o 作業。 **CreateIoCompletionPort** 不會使用此值來進行功能控制;相反地，它會附加至與 i/o 完成埠關聯時，在 *FileHandle* 參數中指定的檔案控制代碼。 此完成索引鍵對於每個檔案控制代碼都應該是唯一的，而且在整個內部完成佇列程式中都隨附檔案控制代碼。 當完成封包抵達時，它會在 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式呼叫中傳回。 [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)函式也會使用 *CompletionKey* 參數，將您自己的特殊用途完成封包排入佇列。

開啟控制碼的實例與 i/o 完成埠相關聯之後，就無法在 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 或 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式中使用，因為這些函式有自己的非同步 i/o 機制。

最好不要使用控制碼繼承或 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 函式的呼叫，與 i/o 完成埠共用相關聯的檔案控制代碼。 使用這類重複的控制碼執行的作業會產生完成通知。 建議您仔細考慮。

I/o 完成通訊埠控制碼，以及與該特定 i/o 完成埠相關聯的每個檔案控制代碼，稱為 *i/o 完成埠的參考*。 當 i/o 完成通訊埠沒有其他參考時，就會釋放它。 因此，所有這些控制碼都必須適當地關閉，才能釋放 i/o 完成埠及其相關聯的系統資源。 滿足這些條件之後，請呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉 i/o 完成埠控制碼。

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                                       |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP (的 WinBase .h 包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**總覽主題**
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[I/o 完成埠](i-o-completion-ports.md)
</dt> <dt>

[使用 Windows 標頭](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[Windows通訊端2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**函數**
</dt> <dt>

[**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

