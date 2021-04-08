---
description: DeletePrinterDataEx 函式會從印表機的設定資料中刪除指定的值。
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: 'DeletePrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693567"
---
# <a name="deleteprinterdataex-function"></a>DeletePrinterDataEx 函式

**DeletePrinterDataEx** 函式會從印表機的設定資料中刪除指定的值。 印表機的設定資料是由一組儲存在登錄機碼階層中的命名和類型值所組成。 函數會刪除指定之索引鍵下的指定值。

如同 [**DeletePrinterData**](deleteprinterdata.md) 函數， **DeletePrinterDataEx** 可以刪除 [**SetPrinterData**](setprinterdata.md) 函數所儲存的值。 此外， **DeletePrinterDataEx** 也可以刪除 [**SetPrinterDataEx**](setprinterdataex.md) 函數在指定索引鍵下儲存的值。

## <a name="syntax"></a>語法


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

此函式會刪除其值之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含要刪除之值的索引鍵。 使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。

如果 *pKeyName* 為 **Null** 或空字串，則 **DeletePrinterDataEx** 會傳回錯誤 \_ 不正確 \_ 參數。

</dd> <dt>

*pValueName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要刪除之值的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為系統錯誤碼。

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
| Unicode 與 ANSI 名稱<br/>   | **DeletePrinterDataExW** (Unicode) 和 **DeletePrinterDataExA** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterKey**](deleteprinterkey.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




