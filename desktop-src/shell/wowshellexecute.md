---
description: 在指定的檔案上執行操作。
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 4389c348a06b7c54dc899da8114eee09e740681f043084bb0c32ab9f7163772e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591828"
---
# <a name="wowshellexecute-function"></a>WOWShellExecute 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在 Windows 的後續版本中變更或無法使用。\]

在指定的檔案上執行操作。 **WOWShellExecute** 僅適用于 Microsoft Windows NT 虛擬 DOS 機器 (Ntvdm.exe) ，可讓磁片作業系統 (DOS) 和16位軟體在 Windows 系統上執行，而且不應該由其他人使用。 請改用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 。

## <a name="syntax"></a>語法


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

類型： **HWND**

主控視窗的控制碼，用來顯示 UI 或錯誤訊息。 如果作業未與視窗相關聯，此值可以是 **Null** 。

</dd> <dt>

*lpOperation* \[在\]
</dt> <dd>

類型： **LPCTSTR**

以 **null** 結束的字串指標，在此案例中稱為 *動詞*，可指定要執行的動作。 可用的動詞集合取決於特定的檔案或資料夾。 一般而言，可從物件的快捷方式功能表取得的動作是可用的動詞命令。 如需動詞和其可用性的詳細資訊，請參閱 [啟動應用程式](launch.md)的 *物件動詞* 一節。 如需快捷方式功能表的進一步討論，請參閱 [擴充快捷方式功能表](context.md) 。 通常會使用下列動詞。

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**編輯**


</dt> <dd>

啟動編輯器並開啟要編輯的檔。 如果 *lpFile* 不是檔檔，則函式會失敗。

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**探討**


</dt> <dd>

探索 *lpFile* 所指定的資料夾。

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**找到**


</dt> <dd>

從指定的目錄起始搜尋。

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**打開**


</dt> <dd>

開啟 *lpFile* 參數所指定的檔案。 檔案可以是可執行檔、檔檔案或資料夾。

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**列印**


</dt> <dd>

列印 *lpFile* 所指定的檔檔案。 如果 *lpFile* 不是檔檔，則函式會失敗。

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**空**


</dt> <dd>

針對 Windows 2000 之前的系統，如果預設動詞命令有效且可在登錄中使用，則會使用預設動詞。 如果沒有，則會使用 "open" 動詞。

若為 Windows 2000 和更新版本的系統，則會使用預設動詞（如果有的話）。 如果沒有，則會使用 "open" 動詞。 如果沒有可用的動詞命令，系統會使用登錄中列出的第一個動詞。

</dd> </dl> </dd> <dt>

*lpFile* \[在\]
</dt> <dd>

類型： **LPCTSTR**

以 **null** 結束的字串指標，指定要在其上執行指定動詞命令的檔案或物件。 若要指定 Shell 命名空間物件，請傳遞完整的剖析名稱。 請注意，並非所有的動詞都支援所有物件。 例如，並非所有檔案類型都支援 "print" 動詞。

</dd> <dt>

*lpParameters* \[在\]
</dt> <dd>

類型： **LPCTSTR**

如果 *lpFile* 參數指定可執行檔，則 *lpParameters* 是以 **null** 結束的字串指標，可指定要傳遞至應用程式的參數。 這個字串的格式取決於要叫用的動詞。 如果 *lpFile* 指定檔檔， *LpParameters* 應該是 **Null**。

</dd> <dt>

*lpDirectory* \[在\]
</dt> <dd>

類型： **LPCTSTR**

指定預設目錄之以 **null** 結束的字串指標。

</dd> <dt>

*nShowCmd* \[在\]
</dt> <dd>

類型： **INT**

旗標，指定應用程式在開啟時的顯示方式。 如果 *lpFile* 指定檔檔，旗標就會直接傳遞至相關聯的應用程式。 應用程式會決定如何處理它。 它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

類型： **void \***

用來在16位核心中呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 的回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HINSTANCE**

如果成功，則傳回大於32的值，否則傳回小於或等於32的錯誤值。 下表列出錯誤值。 傳回值會轉換成 HINSTANCE，以提供與16位 Windows 應用程式的回溯相容性。 不過，這不是真正的 HINSTANCE。 使用傳回的 HINSTANCE 唯一可以完成的工作，就是將它轉換 **成整數，並將** 其與值32或下列其中一個錯誤碼進行比較。



| 傳回碼                                                                                             | 描述                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | 作業系統已用盡記憶體或資源。<br/>                                                                                                           |
| <dl> <dt>**\_ \_ \_ 找不到錯誤檔案**</dt> </dl>  | 找不到指定的檔案。<br/>                                                                                                                             |
| <dl> <dt>**\_ \_ 找不到錯誤路徑 \_**</dt> </dl>  | 找不到指定的路徑。<br/>                                                                                                                             |
| <dl> <dt>**錯誤 \_ \_ 格式錯誤**</dt> </dl>       | .exe 的檔案在 .exe 影像) 中 (非 Win32 .exe 或錯誤時無效。<br/>                                                                                             |
| <dl> <dt>**SE \_ERR \_ ACCESSDENIED**</dt> </dl>    | 作業系統拒絕存取指定的檔案。<br/>                                                                                                     |
| <dl> <dt>**SE \_ERR \_ ASSOCINCOMPLETE**</dt> </dl> | 檔案名關聯未完成或無效。<br/>                                                                                                           |
| <dl> <dt>**SE \_ERR \_ DDEBUSY**</dt> </dl>         | 無法完成 DDE 交易，因為正在處理其他 DDE 交易。<br/>                                                               |
| <dl> <dt>**SE \_ERR \_ DDEFAIL**</dt> </dl>         | DDE 交易失敗。<br/>                                                                                                                                   |
| <dl> <dt>**SE \_ERR \_ DDETIMEOUT**</dt> </dl>      | 因為要求超時，所以無法完成 DDE 交易。<br/>                                                                                     |
| <dl> <dt>**SE \_ERR \_ DLLNOTFOUND**</dt> </dl>     | 找不到指定的 DLL。<br/>                                                                                                                              |
| <dl> <dt>**SE \_ERR \_ FNF**</dt> </dl>             | 找不到指定的檔案。<br/>                                                                                                                             |
| <dl> <dt>**SE \_ERR \_ NOASSOC**</dt> </dl>         | 沒有與指定副檔名相關聯的應用程式。 如果您嘗試列印無法列印的檔案，也會傳回此錯誤。<br/> |
| <dl> <dt>**SE \_ERR \_ OOM**</dt> </dl>             | 沒有足夠的記憶體可完成此作業。<br/>                                                                                                        |
| <dl> <dt>**SE \_ERR \_ PNF**</dt> </dl>             | 找不到指定的路徑。<br/>                                                                                                                             |
| <dl> <dt>**SE \_錯誤 \_ 共用**</dt> </dl>           | 發生共用違規。<br/>                                                                                                                                 |



 

## <a name="remarks"></a>備註

**WOWShellExecute** 不包含在標頭或 .lib 檔案中。 它會依名稱從 Shell32.dll 匯出。

這個方法可讓您在資料夾的快捷方式功能表中執行任何命令，或儲存在登錄中。

如果 *lpOperation* 為 **Null**，則函式會開啟 *lpFile* 所指定的檔案。 如果 *lpOperation* 為「開啟」或「探索」，則函式會嘗試開啟或流覽資料夾。

若要取得由於呼叫 **WOWShellExecute** 而啟動之應用程式的相關資訊，請使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。

> [!Note]  
> [資料夾選項] 中個別進程設定的 [ **開機檔案夾] 視窗** 會影響 **WOWShellExecute**。 如果停用該選項 (預設設定) ， **WOWShellExecute** 會使用開啟的瀏覽器視窗，而不是啟動新的視窗。 如果未開啟任何 Explorer 視窗， **WOWShellExecute** 會啟動一個新視窗。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
