---
description: System.printing.printqueue.addjob 函式會將列印工作加入至可由列印多工緩衝處理器排程的列印工作清單。 函數會抓取您可用來儲存作業的檔案名。
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: 'System.printing.printqueue.addjob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de99b0866e8cd7ec8486d2a3f15f95194b4350008a43fe4db8ae82d970684c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950748"
---
# <a name="addjob-function"></a>System.printing.printqueue.addjob 函式

**System.printing.printqueue.addjob** 函式會將列印工作加入至可由列印多工緩衝處理器排程的列印工作清單。 函數會抓取您可用來儲存作業的檔案名。

> [!NOTE]
> 在 Windows 8 和更新版本的作業系統中，我們不建議您直接使用 **system.printing.printqueue.addjob** ，因為在某些情況下 (，例如使用 File：或 PORTPROMPT： ) 列印到佇列， **system.printing.printqueue.addjob** 將會失敗。 相反地，建議您從 Windows 使用 [GDI 列印 api](gdi-printing.md)、 [XPS 列印 api](xps-printing.md)、 [**StartDocPrinter**](startdocprinter.md)或適當的方法 [**。圖形：列印**](/uwp/api/Windows.Graphics.Printing)命名空間（視列印案例而定）。
>
> 如果您嘗試使用 **File：** 或 **PORTPROMPT：** 來列印至佇列， **System.printing.printqueue.addjob** 將會傳回不 \_ 支援的錯誤。

## <a name="syntax"></a>語法

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

指定列印工作之印表機的控制碼。 這必須是設定為多工緩衝處理印表機的本機印表機。 如果 *hPrinter* 是遠端印表機連線的控制碼，或印表機設定為直接列印，則 **system.printing.printqueue.addjob** 函式會失敗。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

函數儲存在 *.pdata* 所指向之緩衝區中的列印工作資訊資料結構版本。 將此參數設定為一個。

</dd> <dt>

*.pdata* \[擴展\]
</dt> <dd>

接收 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 資料結構和路徑字串的緩衝區指標。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。 緩衝區必須夠大，才能包含 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 結構和路徑字串。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 [**System.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md) 資料結構和路徑字串的總大小（以位元組為單位）。 如果這個值小於或等於 *cbBuf* ，且函式成功，則這是寫入 *.pdata* 所指向之緩衝區的實際位元組數。 如果這個數位大於 *cbBuf*，緩衝區太小，而且您必須使用至少與 pcbNeeded 一樣的緩衝區大小來呼叫函式 \* **。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

您可以呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式來開啟 [**system.printing.printqueue.addjob \_ INFO \_ 1**](addjob-info-1.md)結構的 **Path** 成員所指定的多工緩衝處理檔案，然後呼叫 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)函數將列印工作資料寫入其中。 完成之後，請呼叫 [**ScheduleJob**](schedulejob.md) 函式來通知列印多工緩衝處理器，列印工作現在可以由多工緩衝處理器排程來進行列印。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddJobW** (Unicode) 和 **AddJobA** (ANSI) <br/>                                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ 資訊 \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[GDI 列印 API](gdi-printing.md)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows。圖形：列印**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[XPS 列印 API](xps-printing.md)
</dt> </dl>

 

