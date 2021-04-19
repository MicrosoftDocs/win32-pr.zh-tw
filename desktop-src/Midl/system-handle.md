---
title: system_handle 屬性
description: '\ System_handle \ 屬性指定系統定義的控制碼類型。'
keywords:
- system_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106984268"
---
# <a name="system_handle-attribute"></a>system_handle 屬性

\[ **System_handle** \] 屬性會指定代表系統物件存取權的系統定義控制碼類型。

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>參數

<dl> <dt>

*系統控點類型* 
</dt> <dd>

指定其中一個系統控制碼類型選項。

有效的選項為：
* [sh_composition](sh-composition.md) -DirectComposition 介面控制碼
* [sh_event](sh-event.md) -已命名或未命名的事件物件
* [sh_file](sh-file.md) -檔案或 i/o 裝置
* [sh_job](sh-job.md) -工作物件
* [sh_mutex](sh-mutex.md) -已命名或未命名的 mutex 物件
* [sh_pipe](sh-pipe.md) -匿名或具名管道物件
* [sh_process](sh-process.md) -進程物件
* [sh_reg_key](sh-reg-key.md) -登錄機碼
* [sh_section](sh-section.md) -共用記憶體區段
* [sh_semaphore](sh-semaphore.md) -已命名或未命名的信號物件
* [sh_socket](sh-socket.md) -WinSock 通訊端物件
* [sh_thread](sh-thread.md) -執行緒物件
* [sh_token](sh-token.md) -存取權杖物件

</dd> <dt>

*選擇性-存取-遮罩*
</dt> <dd>

選擇性地要求套用至重複控制碼的特定存取權限。 依預設，當未指定時，會使用相同的存取權複製控制碼。 

若要指定不同層級的存取權，請使用對應于所選基礎系統物件的物件特定存取權限。

如需有關如何在重複期間傳播存取權限的詳細資訊，請參閱 [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 檔。

您可以在 *DuplicateHandle* 參考中找到每個物件類型的存取權限清單連結，也可以在 [ **另請參閱** 每個參數的標題] 頁面中找到 `sh_*` 。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用這個屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。

系統控制碼是作業系統所定義的控制碼，可提供系統資源的存取權。 宣告屬性時，必須指定控制碼後方的特定物件類型。

針對標示的控制碼 `[in]` ，此控制碼會複製到遠端程式中，並在該程式的持續時間內保持有效。 從遠端程式傳回時，會釋放重複的控制碼。 為了維持對基礎物件的存取權，遠端應用程式必須將控制碼複製到它自己的位址空間中。

相反地，針對標示的控制碼， `[out]` 當遠端程式從呼叫傳回控制碼時，遠端程式將會失去其擁有權。 為了維持對基礎物件的存取權，遠端程式應該複製控制碼，並傳回重複的。 傳回的控制碼接著會由呼叫者所擁有，而該呼叫者會在不再需要基礎系統物件的存取權時，負責將其關閉。

因為這是轉送系統物件存取權的機制，這個屬性只適用于同一部電腦上的程式之間的呼叫。

在建立及存取系統控制碼背後的基礎物件時，會決定是否可以將它成功封送處理至遠端程式內容。

的陣列 `system_handle` 可以使用 [**size_is 屬性**](size-is.md) 檔中所找到的語法，傳入或傳出。

## <a name="examples"></a>範例

下列範例會使用的數個 `system_handle` 。 如需完整範例，請參閱 [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) 範例。

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
|-|-|
| 最低支援的用戶端 | Windows 10 年度更新版 (1607 版、組建 14393)  |
| 最低支援的伺服器 | Windows Server 2016 (build 14393)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[/target 參數](./-target.md)
</dt> <dt>

[系結和控制碼](../Rpc/binding-and-handles.md)
</dt> <dt>

[控制碼和物件](../sysinfo/handles-and-objects.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[安全性描述項](../secauthz/security-descriptors.md)
</dt></dl>
