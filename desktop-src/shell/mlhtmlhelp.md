---
description: 顯示對應于目前 UI 語言設定的說明視窗。
title: MLHtmlHelp 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991123"
---
# <a name="mlhtmlhelp-function"></a>MLHtmlHelp 函式

\[這項功能可透過 Windows XP 和 Windows Server 2003 取得。 它可能會在後續版本的 Windows 中改變或無法使用。\]

顯示對應于目前 UI 語言設定的說明視窗。

## <a name="syntax"></a>語法


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndCaller* \[在\]
</dt> <dd>

類型： **HWND**

呼叫此函式之父視窗的控制碼。

</dd> <dt>

*pszFile* \[在\]
</dt> <dd>

類型： **LPCTSTR**

緩衝區的指標，其中包含已編譯說明 ( .chm) 檔案的完整路徑，或指定說明檔中的主題檔案。

</dd> <dt>

*uCommand* \[在\]
</dt> <dd>

類型： **UINT**

要完成的命令。 此函式只會直接支援 [hh \_ 顯示 \_ 主題](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) 和 [hh \_ 顯示 \_ 文字 \_ 快顯視窗](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command)。 在任何其他命令的情況下，會將不含 *dwCrossCodePage* 值的呼叫轉送至 [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)。

</dd> <dt>

*dwData* \[在\]
</dt> <dd>

類型： **DWORD \_ PTR**

任何可能需要的資料（根據 *uCommand* 參數的值）。

</dd> <dt>

*dwCrossCodePage* \[在\]
</dt> <dd>

類型： **DWORD**

**DWORD** 值，指出目前 UI 語言設定的字碼頁，例如 CP \_ ACP。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HWND**

根據指定的 *uCommand* 和結果， **MLHtmlHelp** 會傳回下列其中一項或兩項：

-   說明視窗 (hwnd) 的控制碼。
-   **Null**。 在某些情況下， **Null** 表示失敗;在其他情況下， **Null** 表示尚未建立說明視窗。

## <a name="remarks"></a>備註

如果目前語言的說明檔路徑發生問題，則會將呼叫轉送至 [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) 以進行標準處理。

當 [說明] 視窗關閉時，除非擁有者為桌面，否則焦點會回到擁有者。 如果 *hwndCaller* 是桌面，則作業系統會決定傳回焦點的位置。

此外，如果 **MLHtmlHelp** 從 [說明] 視窗傳送任何通知訊息，只要您已在 [說明] 視窗定義中啟用 [通知訊息](/previous-versions/windows/desktop/htmlhelp/about-notification-messages)追蹤，訊息就會傳送至 *hwndCaller* 。

## <a name="examples"></a>範例

下列範例會呼叫 [HH \_ DISPLAY \_ 主題](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) 命令以開啟名為 help 的說明檔，並在名為的 [說明] 視窗中顯示其預設主題 `Mainwin` 。 一般而言，此命令中指定的 [說明] 視窗是標準的 [HTML 說明檢視器](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)。

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> 使用此函式時，請將裝載可執行檔的堆疊大小設定為至少100k。 如果定義的堆疊大小太小，則建立來執行 HTML 說明的執行緒也會以這個堆疊大小建立，而作業可能會失敗。 （選擇性）您可以從 link 命令列中移除/STACK，也可以移除可執行檔 .DEF 檔中的任何堆疊設定 (預設堆疊大小在此案例中為 1MB) 。 您也可以使用/Fnumber 編譯器命令設定堆疊大小 (編譯器會將此值以/STACK) 的形式傳遞至連結器。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **MLHtmlHelpW** (Unicode) 和 **MLHtmlHelpA** (ANSI) <br/>                                               |



 

 
