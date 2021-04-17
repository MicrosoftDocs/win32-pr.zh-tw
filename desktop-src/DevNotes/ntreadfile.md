---
description: 從開啟的檔案讀取資料。
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: 'NtReadFile 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510455"
---
# <a name="ntreadfile-function"></a>NtReadFile 函式

從開啟的檔案讀取資料。

此函式是使用者模式，相當於 Windows 驅動程式套件 (WDK) 中記載的 [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) 函式。

## <a name="syntax"></a>語法


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileHandle* \[在\]
</dt> <dd>

File 物件的控制碼。 這個控制碼是由成功呼叫 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) 或 [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile)所建立。

</dd> <dt>

*活動* \[在中，選擇性\]
</dt> <dd>

（選擇性）在讀取作業完成後，將事件物件的控制碼設定為已發出信號的狀態。 裝置和中繼驅動程式應該將此參數設定為 **Null**。

</dd> <dt>

*ApcRoutine* \[在中，選擇性\]
</dt> <dd>

此參數已保留備用。 裝置和中繼驅動程式應該將此指標設定為 **Null**。

</dd> <dt>

*ApcCoNtext* \[在中，選擇性\]
</dt> <dd>

此參數已保留備用。 裝置和中繼驅動程式應該將此指標設定為 **Null**。

</dd> <dt>

*IoStatusBlock* \[擴展\]
</dt> <dd>

[**IO \_ 狀態 \_ 區塊**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block)結構的指標，此結構會接收最終完成狀態，以及有關所要求讀取作業的資訊。 **資訊** 成員會收到實際從檔案讀取的位元組數目。

</dd> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

呼叫端配置之緩衝區的指標，此緩衝區會接收從檔案讀取的資料。

</dd> <dt>

*長度* \[在\]
</dt> <dd>

*緩衝區* 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*ByteOffset* \[在中，選擇性\]
</dt> <dd>

變數的指標，該變數會在檔案中指定開始讀取作業的起始位元組位移。 如果嘗試讀取超過檔案結尾， **NtReadFile** 會傳回錯誤。

如果對 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) 的呼叫設定 *CreateOptions* 旗標檔案 \_ 同步 \_ io \_ 警示或檔案 \_ 同步 \_ io \_ NONALERT，則 i/o 管理員會維護目前的檔案位置。 如果是， **NtReadFile** 的呼叫端可以指定使用目前的檔案位置位移，而不是明確的 *ByteOffset* 值。 您可以使用下列其中一種方法來建立此規格：

-   指定 **HighPart** 成員設為-1 的 **大型 \_ 整數** 值的指標，並將 **LowPart** 成員設為系統定義的值檔案 \_ 使用檔案 \_ \_ 指標 \_ 位置。

-   傳遞 *ByteOffset* 的 **Null** 指標。

**NtReadFile** 會在完成讀取作業時新增讀取的位元組數目，以更新目前的檔案位置（如果它使用 i/o 管理員所維護的目前檔案位置）。

即使 i/o 管理員正在維護目前的檔案位置，呼叫者也可以將明確的 *ByteOffset* 值傳遞給 **NtReadFile**，以重設這個位置。 這樣做會自動將目前的檔案位置變更為該 *ByteOffset* 值，執行讀取作業，然後根據實際讀取的位元組數來更新位置。 這項技術提供呼叫者不可部分完成的搜尋和讀取服務。

</dd> <dt>

*金鑰* \[在中，選擇性\]
</dt> <dd>

裝置和中繼驅動程式應該將此指標設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtReadFile** 會傳回狀態 \_ SUCCESS 或適當的 NTSTATUS 錯誤碼。

## <a name="remarks"></a>備註

**NtReadFile** 的呼叫端必須已使用 [](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) \_ DesiredAccess 參數中所設定的 FILE read \_ DATA 或 GENERIC \_ READ 值來呼叫 NtCreateFile。

如果上述對 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)的呼叫將 \_ \_ CREATEOPTIONS 參數中的 FILE NO 中繼緩衝旗標設 \_ 為 **NtCreateFile**，則 **NtReadFile** 的 *長度* 和 *ByteOffset* 參數必須是磁區大小的倍數。 如需詳細資訊，請參閱 **NtCreateFile**。

**NtReadFile** 會開始從指定的 *ByteOffset* 或目前的檔案位置讀取至指定的 *緩衝區*。 它會在下列其中一個條件下終止讀取作業：

-   緩衝區已滿，因為已讀取 *長度* 參數所指定的位元組數目。 因此，沒有任何資料可以放到緩衝區中，而不會發生溢位。

-   讀取作業期間已到達檔案結尾，因此檔案中沒有其他資料可傳輸到緩衝區。

如果呼叫端以 *DesiredAccess* 中設定的同步旗標來開啟檔案，呼叫端執行緒可以等候檔案控制代碼 *FileHandle*，同步處理至完成讀取作業。 每次控制碼上發出的 i/o 作業完成時，就會發出控制碼的信號。 不過，呼叫端不能等待開啟以進行同步檔案存取的控制碼 (檔案 \_ 同步 \_ io \_ NONALERT 或檔案 \_ 同步 \_ io \_ 警示) 。 在此情況下， **NtReadFile** 會代表呼叫端等候，直到讀取作業完成時才會返回。 只有在符合下列三個條件時，呼叫者才可以安全地在檔案控制代碼上等候：

-   開啟的控制碼為非同步存取 (也就是， \_ \_) 未指定任何檔案同步 IO \_ *XXX* 旗標。

-   控制碼一次僅用於一個 i/o 作業。

-   **NtReadFile** 傳回的狀態為 \_ 暫止。

如果有下列任何一種情況，驅動程式應該在系統進程的內容中呼叫 **NtReadFile** ：

-   驅動程式建立了它傳遞給 **NtReadFile** 的檔案控制代碼。

-   **NtReadFile** 會透過驅動程式所建立的事件，將 i/o 完成的驅動程式通知。

-   **NtReadFile** 會藉由驅動程式傳遞至 **NtReadFile** 的 APC 回呼常式，來通知 i/o 完成的驅動程式。

只有在建立控制碼的進程內容中，檔案和事件控制碼才有效。 因此，為了避免安全性漏洞，驅動程式應該在系統進程的內容中，建立傳遞給 **NtReadFile** 的任何檔案或事件控制碼，而不是驅動程式所在之進程的內容。

同樣地，如果 **NtReadFile** 在系統進程的環境中透過 APC 通知驅動程式，就應該呼叫它，因為 apc 一律會在發出 i/o 要求的執行緒內容中引發。 如果驅動程式在系統以外的進程內容中呼叫 **NtReadFile** ，APC 可能會無限期地延遲，或根本不會引發。

如需使用檔案的詳細資訊，請參閱 [在驅動程式中使用](/windows-hardware/drivers/kernel/using-files-in-a-driver)檔案。

**NtReadFile** 的呼叫端必須在 IRQL = 被動 \_ 層級執行，並 [啟用特殊的核心 apc](/windows-hardware/drivers/kernel/disabling-apcs)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                    |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| 標頭<br/>                   | <dl> <dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt> </dl>                   |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll (使用者模式) </dt> </dl>                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KeInitializeEvent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**NtQueryInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**NtSetInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**NtWriteFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
