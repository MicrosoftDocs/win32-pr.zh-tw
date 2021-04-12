---
description: GetJob 函式會抓取指定列印工作的相關資訊。
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: 'GetJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192717"
---
# <a name="getjob-function"></a>GetJob 函式

**GetJob** 函式會抓取指定列印工作的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

要抓取列印工作資料之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*JobId* \[在\]
</dt> <dd>

識別要取出資料的列印工作。 您可以使用 [**system.printing.printqueue.addjob**](addjob.md) 函數或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PJob* 緩衝區中傳回的資訊類型。 如果 *層級* 為1， *PJob* 會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 結構。 如果 *層級* 為2， *PJob* 會收到 [**工作 \_ 資訊 \_ 2**](job-info-2.md) 結構。

</dd> <dt>

*pJob* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 或 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構，其中包含作業的相關資訊。 緩衝區必須夠大，才能儲存結構成員所指向的字串。

若要判斷所需的緩衝區大小，請呼叫 **GetJob** ，並將 *cbBuf* 設定為零。 **GetJob** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

陣列的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

值的指標，指定函式成功時所複製的位元組數目，或如果 *cbBuf* 太小，則為所需的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetJobW** (Unicode) 和 **GetJobA** (ANSI) <br/>                                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 1**](job-info-1.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

