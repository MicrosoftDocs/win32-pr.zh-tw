---
description: 將連接新增至目前使用者的指定印表機，並指定連接詳細資料。
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: 'AddPrinterConnection2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f54cdafc2bc5c957f21ed4f9a14355d6a70f7df817e975c1fe701e2b20af35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868966"
---
# <a name="addprinterconnection2-function"></a>AddPrinterConnection2 函式

將連接新增至目前使用者的指定印表機，並指定連接詳細資料。

## <a name="syntax"></a>語法


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

父視窗的控制碼，如果列印系統必須從列印伺服器下載此連接的印表機驅動程式，則會顯示對話方塊。

</dd> <dt>

*pszName* \[在\]
</dt> <dd>

常數以 null 終止的字串指標，指定目前使用者希望連接的印表機名稱。

</dd> <dt>

*dwLevel* 
</dt> <dd>

*PConnectionInfo* 所指向的結構版本。 目前只會定義層級1，因此 *dwLevel* 的值必須是1。

</dd> <dt>

*pConnectionInfo* \[在\]
</dt> <dd>

[**印表機 \_ 連接 \_ 資訊 \_ 1**](printer-connection-info-1.md)結構的指標。 如需此參數的詳細資訊，請參閱「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。 如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

當 Windows Vista 連接至印表機時，可能需要從印表機所連接的伺服器複製印表機驅動程式檔案。 如果使用者沒有許可權可將檔案複製到適當的位置， **AddPrinterConnection2** 函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ 拒絕存取錯誤 \_ 。

如果印表機驅動程式檔案必須從列印伺服器複製，但因為有作用中的群組原則，而且無法以無訊息方式複製， \_ \_ \_ *pConnectionInfo->dwFlags* 中不會設定任何對話方塊，而且呼叫會失敗。

如果本機印表機驅動程式可用來轉譯此印表機的列印工作，而且本機驅動程式的版本必須與伺服器上的印表機驅動程式版本不相符，請 \_ \_ 在 *PConnectionInfo->DWFLAGS* 中設定印表機連線不相符，然後將指標指派給包含本機印表機驅動程式路徑的字串變數，以 *pConnectionInfo >pszDriverName*。

呼叫 **AddPrinterConnection2** 時所建立的印表機連線將會在呼叫 [**>enumprinters**](enumprinters.md) 時列舉，並將 *dwType* 設定為印表機 \_ 列舉 \_ 連接。

此函式 **AddPrinterConnection2A** 的 ANSI 版本不受支援，而且會傳回 **\_ 不 \_ 支援的錯誤**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrinterConnection2W** (Unicode) <br/>                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

