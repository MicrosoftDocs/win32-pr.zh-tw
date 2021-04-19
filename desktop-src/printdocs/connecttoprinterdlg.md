---
description: ConnectToPrinterDlg 函式會顯示一個對話方塊，讓使用者流覽並聯機到網路上的印表機。
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: 'ConnectToPrinterDlg 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980507"
---
# <a name="connecttoprinterdlg-function"></a>ConnectToPrinterDlg 函式

**ConnectToPrinterDlg** 函式會顯示一個對話方塊，讓使用者流覽並聯機到網路上的印表機。 如果使用者選取印表機，此函式會嘗試建立與它的連接;如果伺服器上未安裝適當的驅動程式，則會提供使用者在本機建立印表機的選項。

## <a name="syntax"></a>語法


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

指定對話方塊的父視窗。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

此參數是保留的，而且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功且使用者選取印表機，則傳回值會是所選印表機的控制碼。

如果函式失敗，或使用者取消對話方塊，而不選取印表機，則傳回值為 **Null**。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**ConnectToPrinterDlg** 函式會嘗試建立與所選印表機的連接。 但是，如果印表機所在的伺服器沒有安裝適合的驅動程式，則此函式會提供使用者在本機建立印表機的選項。 呼叫應用程式可以藉由呼叫 [**GetPrinter**](getprinter.md) 與 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構，然後檢查該結構的 **屬性** 成員，來判斷函式是否已在本機建立印表機。

應用程式應該呼叫 [**DeletePrinter**](deleteprinter.md) 來刪除本機印表機。 應用程式應該呼叫 [**DeletePrinterConnection**](deleteprinterconnection.md) 來刪除印表機的連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




