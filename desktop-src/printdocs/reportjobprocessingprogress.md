---
description: 向「列印多工緩衝處理器」服務回報 XPS 列印工作是否在幕後處理或轉譯階段，以及處理的哪個部分正在進行中。
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: 'ReportJobProcessingProgress 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944685"
---
# <a name="reportjobprocessingprogress-function"></a>ReportJobProcessingProgress 函式

向「列印多工緩衝處理器」服務回報 XPS 列印工作是否在幕後處理或轉譯階段，以及處理的哪個部分正在進行中。

## <a name="syntax"></a>語法


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*printerHandle* \[在\]
</dt> <dd>

函式用來取得資訊的印表機控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*jobId* \[in\]
</dt> <dd>

識別要取出資料的列印工作。 您可以使用 [**system.printing.printqueue.addjob**](addjob.md) 函數或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。

</dd> <dt>

*jobOperation* 
</dt> <dd>

指定作業是在幕後處理階段或轉譯階段。

</dd> <dt>

*jobProgress* 
</dt> <dd>

指定處理中的哪個部分正在進行中。 根據 *jobOperation* 的值，此值會參考在幕後處理或轉譯階段中的事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

> [!Note]  
> **ReportJobProcessingProgress** 只會報告 XPS 列印工作在幕後處理或轉譯階段的進度。 如果 XPS 列印工作不在幕後處理或轉譯階段時呼叫， **ReportJobProcessingProgress** 將會失敗。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EPrintXPSJobOperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**EPrintXPSJobProgress**](eprintxpsjobprogress.md)
</dt> </dl>

 

