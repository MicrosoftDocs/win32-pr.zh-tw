---
description: EnumPrinterDataEx 函式會列舉指定之印表機和索引鍵的所有值名稱和資料。
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: 'EnumPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e78c17cccf416d186c4669e3576c5a0c9bf2365cb048a73b42d583b187156f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034266"
---
# <a name="enumprinterdataex-function"></a>EnumPrinterDataEx 函式

**EnumPrinterDataEx** 函式會列舉指定之印表機和索引鍵的所有值名稱和資料。

印表機資料會儲存在登錄中。 列舉印表機資料時，請勿呼叫可能會變更資料的登錄功能。

## <a name="syntax"></a>語法


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

由函式抓取設定資料的印表機控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含要列舉之值的索引鍵。 使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。 **EnumPrinterDataEx** 會列舉索引鍵的所有值，但不會列舉指定之索引鍵的子機碼值。 使用 [**EnumPrinterKey**](enumprinterkey.md) 函式來列舉子機碼。

如果 *pKeyName* 為 **Null** 或空字串，則 **EnumPrinterDataEx** 會傳回錯誤 \_ 不正確 \_ 參數。

</dd> <dt>

*pEnumValues* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**印表機 \_ 列舉 \_ 值**](printer-enum-values.md) 結構的陣列。 每個結構都包含值的名稱、類型、資料和值在索引鍵下的大小。

</dd> <dt>

*cbEnumValues* \[在\]
</dt> <dd>

*PcbEnumValues* 所指向之緩衝區的大小（以位元組為單位）。 如果您將 *cbEnumValues* 設定為零， *pcbEnumValues* 參數會傳回所需的緩衝區大小。

</dd> <dt>

*pcbEnumValues* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收所抓取設定資料的大小（以位元組為單位）。 如果 *cbEnumValues* 所指定的緩衝區大小太小，則函式會傳回 \_ 錯誤 \_ 的資料，而 *pcbEnumValues* 則會指出所需的緩衝區大小。

</dd> <dt>

*pnEnumValues* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *pEnumValues* 中傳回之 [**印表機 \_ 列舉 \_ 值**](printer-enum-values.md)結構的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為系統錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**EnumPrinterDataEx** 會透過 [**SetPrinterDataEx**](setprinterdataex.md) 和 [**SetPrinterData**](setprinterdata.md) 函式來抓取印表機設定資料集。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrinterDataExW** (Unicode) 和 **EnumPrinterDataExA** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**印表機 \_ 列舉 \_ 值**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




