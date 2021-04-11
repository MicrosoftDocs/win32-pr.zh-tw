---
description: EnumJobs 函式會抓取指定印表機的一組指定列印工作的相關資訊。
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: 'EnumJobs 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193763"
---
# <a name="enumjobs-function"></a>EnumJobs 函式

**EnumJobs** 函式會抓取指定印表機的一組指定列印工作的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

此函式會列舉其列印工作的印表機物件控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*FirstJob* \[在\]
</dt> <dd>

第一個要列舉之列印工作的列印佇列中，以零為基底的位置。 例如，值為0會指定列舉應該從列印佇列中的第一個列印工作開始;值為9時，會指定在列印佇列中的第十個列印工作開始列舉。

</dd> <dt>

*NoJobs* \[在\]
</dt> <dd>

要列舉的列印工作總數。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PJob* 緩衝區中傳回的資訊類型。



| 值                                                                                                | 意義                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* 接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md) 結構的陣列<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* 接收 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構的陣列<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* 接收 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構的陣列<br/> |



 

</dd> <dt>

*pJob* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、 [**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 3**](job-info-3.md) 結構的陣列。 緩衝區必須夠大，才能接收結構的陣列，以及結構成員指向的任何字串或其他資料。

若要判斷所需的緩衝區大小，請呼叫 **EnumJobs** ，並將 *cbBuf* 設定為零。 **EnumJobs** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PJob* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收函式成功時所複製的位元組數目。 如果函式失敗，則變數會收到所需的位元組數目。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pJob* 緩衝區中傳回的 [**作業 \_ 資訊 \_ 1**](job-info-1.md)、[**作業 \_ 資訊 \_ 2**](job-info-2.md)或 [**作業 \_ 資訊 \_ 3**](job-info-3.md)結構的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

[**作業 \_ 資訊 \_ 1**](job-info-1.md)結構包含一般列印工作資訊，[**作業 \_ 資訊 \_ 2**](job-info-2.md)結構有更詳細的資訊。 [**作業 \_ 資訊 \_ 3**](job-info-3.md)結構包含如何連結作業的相關資訊。

若要判斷印表機佇列中的列印工作數目，請呼叫 [**GetPrinter**](getprinter.md) 函數，並將 *Level* 參數設定為2。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumJobsW** (Unicode) 和 **EnumJobsA** (ANSI) <br/>                                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 1**](job-info-1.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 2**](job-info-2.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

