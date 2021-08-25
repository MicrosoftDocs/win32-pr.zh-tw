---
description: ReadPrinter 函數會從指定的印表機抓取資料。
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: 'ReadPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 63683e421441fb15ec299f3077088bd8f9cffb65644550be912ee39b5c530371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824018"
---
# <a name="readprinter-function"></a>ReadPrinter 函式

**ReadPrinter** 函數會從指定的印表機抓取資料。

## <a name="syntax"></a>語法


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

要取得其資料之印表機物件的控制碼。 使用 [**OpenPrinter**](openprinter.md) 函式來取出印表機物件控制碼。 使用格式： Printername，Job xxxx。

</dd> <dt>

*pBuf* \[擴展\]
</dt> <dd>

接收印表機資料之緩衝區的指標。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PBuf* 所指向的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pNoBytesRead* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收復制到 *pBuf* 點之陣列中的資料位元組數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

如果裝置或印表機不是雙向， **ReadPrinter** 會傳回錯誤。

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

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




