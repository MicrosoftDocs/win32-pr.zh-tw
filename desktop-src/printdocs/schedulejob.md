---
description: ScheduleJob 函式要求列印多工緩衝處理器排程指定的列印工作來進行列印。
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: 'ScheduleJob 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470223"
---
# <a name="schedulejob-function"></a>ScheduleJob 函式

**ScheduleJob** 函式要求列印多工緩衝處理器排程指定的列印工作來進行列印。

## <a name="syntax"></a>語法


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

列印工作之印表機的控制碼。 這必須是設定為多工緩衝處理印表機的本機印表機。 如果 *hPrinter* 是遠端印表機連線的控制碼，或印表機設定為直接列印，則 **ScheduleJob** 函式會失敗。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

*hPrinter* 必須與取得 *dwJobID* 列印工作識別碼的 [**system.printing.printqueue.addjob**](addjob.md)呼叫中指定的印表機控制碼相同。

</dd> <dt>

*dwJobID* \[在\]
</dt> <dd>

要排程的列印工作。 您可以藉由呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函數來取得此列印工作識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

您必須先成功呼叫 [**system.printing.printqueue.addjob**](addjob.md) 函式，才能呼叫 **ScheduleJob** 函數。 **System.printing.printqueue.addjob** 會取得您以 *dwJobID* 的形式傳遞至 **ScheduleJob** 的列印工作識別碼。 這兩個呼叫都必須使用相同的 *hPrinter* 值。

**ScheduleJob** 函式會檢查有效的多工緩衝處理檔案。 如果有不正確多工緩衝處理檔案，或如果是空的， **ScheduleJob** 會同時刪除多工緩衝處理檔案和列印多工緩衝處理器中對應的列印工作專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




