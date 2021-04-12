---
description: EnumForms 函式會列舉指定印表機所支援的表單。
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: 'EnumForms 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319096"
---
# <a name="enumforms-function"></a>EnumForms 函式

**EnumForms** 函式會列舉指定印表機所支援的表單。

## <a name="syntax"></a>語法


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

應列舉表單之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

指定 *pForm* 點的結構版本。 此值必須是1或2。

</dd> <dt>

*pForm* \[擴展\]
</dt> <dd>

一或多個 [**表單 \_ 資訊 \_ 1**](form-info-1.md) 結構的指標，或一個或多個 [**表單 \_ 資訊 \_ 2**](form-info-2.md) 結構的指標。 所有結構都有相同的層級。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

指定 *pForm* 點的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收復制到陣列的 PForm 點所複製的位元組數目，如果作業) 成功，則為點 (的位元組數目; 如果失敗，則為 (所需的位元組數目，因為 *cbBuf* 太小) 。

</dd> <dt>

*pcReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收復制到 *pForm* 點之陣列中的結構數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

如果呼叫端是遠端的，而且 *層級* 是2，則傳回 [**表單 \_ INFO \_ 2**](form-info-2.md)結構的 **StringType** 值一律會是 **字串 \_ LANGPAIR**。

在 Windows Vista 中， **EnumForms** 所傳回的表單資料，會在 *hPrinter* 指的是由列印伺服器所裝載的遠端列印伺服器或印表機時，從本機快取中取出，而且至少有一個開啟的連接可連至遠端列印伺服器上的印表機。 在所有其他設定中，會從遠端列印伺服器查詢表單資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumFormsW** (Unicode) 和 **EnumFormsA** (ANSI) <br/>                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**表單 \_ 資訊 \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




