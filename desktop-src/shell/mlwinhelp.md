---
description: 啟動 Windows 說明 (Winhelp.exe) 並傳遞其他資料，以指出應用程式所要求之說明的本質。
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: MLWinHelp 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: a6c109f39107ba3cfd1800cca8db516d0033a2f3c32b9784e4359b3c6c50655d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968897"
---
# <a name="mlwinhelp-function"></a>MLWinHelp 函式

\[這項功能可透過 Windows XP 和 Windows Server 2003 取得。 它可能會在 Windows 的後續版本中變更或無法使用。\]

啟動 Windows 說明 (Winhelp.exe) 並傳遞其他資料，以指出應用程式所要求之說明的本質。

## <a name="syntax"></a>語法


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWndMain* \[在\]
</dt> <dd>

類型： **HWND**

要求協助的視窗控制碼。 **MLWinHelp** 函式會使用此控制碼來追蹤哪些應用程式已要求協助。 如果 *uCommand* 參數指定 help \_ CONTEXTMENU 或 help \_ WM \_ help， *hWndMain* 會識別要求說明的控制項。

</dd> <dt>

*lpszHelp* \[在\]
</dt> <dd>

類型： **LPCTSTR**

包含路徑之以 null 結束的字串的位址（如有必要），以及 **MLWinHelp** 要顯示之說明檔的名稱。

如果主題要顯示在次要視窗中，而不是在主視窗中，檔案名後面可以是角括弧 (>) 和次要視窗的名稱。 您必須在 [說明] 專案的 [WINDOWS] 區段中，定義次要視窗的名稱 \[ \] ( .hpj) 檔。

</dd> <dt>

*uCommand* \[在\]
</dt> <dd>

類型： **UINT**

要求的說明類型。 如需可能值的清單，以及它們如何影響要放置在 *dwData* 參數中的值，請參閱「備註」一節。

</dd> <dt>

*dwData* \[在\]
</dt> <dd>

類型： **DWORD \_ PTR**

其他資料。 使用的值取決於 *uCommand* 參數的值。 如需可能 *dwData* 值的清單，請參閱「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

在成功時傳回非零值，否則傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

這個函式不包含在標頭檔中，而且必須由序數395針對 **MLWinHelpA** 和397呼叫 **MLWinHelpW**。

**MLWinHelp** 基本上是 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)的包裝函式。 它會在呼叫 **WinHelp** 之前，嘗試取得對應于目前 UI 語言設定的說明檔路徑。 如果成功，則會傳遞該路徑。 如果失敗，則會傳遞 *lpszHelp* 所指向的路徑。

如果從任何內容呼叫但目前的使用者，則此函式會失敗。

在關閉要求說明的視窗之前，應用程式必須呼叫 **MLWinHelp** ，並將 *uCommand* 參數設定為 [ \_ 停止]。 在所有應用程式完成之前，Windows 說明將不會終止。 請注意， \_ 如果您使用 [說明 \_ CONTEXTPOPUP] 命令啟動 Windows 說明，就不需要呼叫 help QUIT 命令的 Windows 說明。

下表顯示 *uCommand* 參數的可能值，以及 *dwData* 參數的對應格式。



| *uCommand*          | 動作                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HELP \_ 命令       | 執行 help 宏或宏字串。                                                                                                                                                                                                                               | 字串的位址，指定要執行) 的說明宏 (的名稱。 如果字串指定多個宏名稱，則名稱必須以分號分隔。 您必須針對某些宏使用宏名稱的簡短形式，因為 Windows 說明不支援完整名稱。                         |
| 說明 \_ 內容      | 顯示 [內容] 選項在 .hpj 檔案的 [選項] 區段中指定的主題 \[ \] 。 此命令適用于回溯相容性。 新的應用程式應該提供 cnt 檔案，並使用 HELP \_ FINDER 命令。                                           | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ 內容       | 顯示在 .hpj 檔案的 [對應] 區段中定義的指定內容識別碼所識別的主題。 \[ \]                                                                                                                                                   | 包含主題的內容識別碼。                                                                                                                                                                                                                                                               |
| 說明 \_ CONTEXTMENU   | 顯示所選視窗的 [說明 **] 功能表，** 然後在快顯視窗中顯示所選控制項的主題。                                                                                                                                             | **DWORD** 配對陣列的位址。 每個配對中的第一個 **DWORD** 是控制項識別碼，而第二個是主題的內容識別碼。 陣列必須以一對零結束 {0,0} 。 如果您不想要將說明新增至特定控制項，請將其內容識別碼設定為-1。 |
| 說明 \_ CONTEXTPOPUP  | 顯示在 \[ 快顯視窗中，在 .hpj 檔案的 [對應] 區段中定義的指定內容識別碼所識別的主題 \] 。                                                                                                                                | 包含主題的內容識別碼。                                                                                                                                                                                                                                                                 |
| HELP \_ FINDER        | 顯示 [ **說明主題** ] 對話方塊。                                                                                                                                                                                                                             | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ FORCEFILE     | 確保 Windows 說明會顯示正確的說明檔。 如果顯示的是不正確的說明檔，Windows 說明會開啟正確的說明檔。否則，就不會採取任何動作。                                                                                     | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ HELPONHELP    | 如果有 winhlp32.exe 的 .hlp 檔案，會顯示如何使用 Windows 說明的說明。                                                                                                                                                                                     | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ 索引         | 顯示 [內容] 選項在 .hpj 檔案的 [選項] 區段中指定的主題 \[ \] 。 此命令適用于回溯相容性。 新的應用程式應該使用 HELP \_ FINDER 命令。                                                                   | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ 鍵           | 如果完全相符，則在符合指定關鍵字的關鍵字表格中顯示主題。 如果有一個以上的相符項，則會使用 [ **找到的主題** ] 清單方塊中列出的主題來顯示索引。                                                 | 關鍵字字串的位址。 多個關鍵字必須以分號分隔。                                                                                                                                                                                                                              |
| 說明 \_ MULTIKEY      | 在替代關鍵字表中顯示關鍵字所指定的主題。                                                                                                                                                                                           | 指定資料表註腳字元和關鍵字的 [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) 結構位址。                                                                                                                                                                                     |
| 說明 \_ PARTIALKEY    | 如果完全相符，則在符合指定關鍵字的關鍵字表格中顯示主題。 如果有一個以上的相符項，則會顯示 [ **找到的主題** ] 對話方塊。 若要顯示索引但不傳遞關鍵字，請使用空字串的指標。 | 關鍵字字串的位址。 多個關鍵字必須以分號分隔。                                                                                                                                                                                                                              |
| 協助 \_ 結束          | 通知 Windows 您不再需要該資訊。 如果沒有任何其他應用程式要求提供協助，Windows 會關閉 Windows 說明。                                                                                                                                         | 忽略設定為0。                                                                                                                                                                                                                                                                                           |
| 說明 \_ SETCONTENTS   | 指定內容主題。 Windows當使用者按一下 [**內容**] 按鈕時，如果說明檔沒有相關聯的 cnt 檔案，[說明] 會顯示此主題。                                                                                                  | 包含內容主題的內容識別碼。                                                                                                                                                                                                                                                      |
| 協助 \_ SETPOPUP \_ POS | 設定後續快顯視窗的位置。                                                                                                                                                                                                                   | 包含位置資料。 使用 [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) 宏將水準和垂直座標串連成單一值。 當叫用快顯視窗時，快顯視窗的位置就像是滑鼠游標位於指定的點。                                 |
| 說明 \_ SETWINPOS     | 如果最小化或在記憶體中，則會顯示 Windows 說明視窗，並依指定設定其大小和位置。                                                                                                                                                      | [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)結構的位址，指定主要或次要說明視窗的大小和位置。                                                                                                                                                             |
| 說明 \_ TCARD         | 指出命令適用于 Windows 說明的訓練卡實例。 使用位 OR 運算子將這個命令與其他命令合併。                                                                                                                    | 取決於結合這個命令所使用的命令。                                                                                                                                                                                                                                                  |
| 說明 \_ WM \_ 協助      | 顯示快顯視窗中 *hWndMain* 參數所識別之控制項的主題。                                                                                                                                                                        | **DWORD** 配對陣列的位址。 每個配對中的第一個 **DWORD** 是控制項識別碼，而第二個是主題的內容識別碼。 陣列必須以一對零結束 {0,0} 。 如果您不想要將說明新增至特定控制項，請將其內容識別碼設定為-1。       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **MLWinHelpW** (Unicode) 和 **MLWinHelpA** (ANSI) <br/>                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
