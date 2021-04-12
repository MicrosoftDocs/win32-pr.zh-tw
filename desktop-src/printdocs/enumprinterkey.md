---
description: EnumPrinterKey 函式會列舉指定印表機之指定機碼的子機碼。
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: 'EnumPrinterKey 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319975"
---
# <a name="enumprinterkey-function"></a>EnumPrinterKey 函式

**EnumPrinterKey** 函式會列舉指定印表機之指定機碼的子機碼。

印表機資料會儲存在登錄中。 列舉印表機資料時，請勿呼叫可能會變更資料的登錄功能。

## <a name="syntax"></a>語法


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

此函式會列舉子機碼之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含要列舉之子機碼的索引鍵。 使用反斜線 ' \\ ' 字元做為分隔符號，以指定包含一或多個子機碼的路徑。 **EnumPrinterKey** 會列舉機碼的所有子機碼，但不會列舉這些子機碼的子機碼。

如果 *pKeyName* 是空字串 ( "" ) ，則 **EnumPrinterKey** 會列舉印表機的最上層索引鍵。 如果 *pKeyName* 為 **Null**，則 **EnumPrinterKey** 會傳回錯誤 \_ 無效 \_ 的參數。

</dd> <dt>

*pSubkey* \[擴展\]
</dt> <dd>

接收以 null 終止之子機碼名稱陣列的緩衝區指標。 陣列以兩個 null 字元結束。

</dd> <dt>

*cbSubkey* \[在\]
</dt> <dd>

*PSubkey* 所指向之緩衝區的大小（以位元組為單位）。 如果您將 *cbSubkey* 設定為零， *pcbSubkey* 參數會傳回所需的緩衝區大小。

</dd> <dt>

*pcbSubkey* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收在 *pSubkey* 緩衝區中取出的位元組數目。 如果 *cbSubkey* 所指定的緩衝區大小太小，則函式會傳回 \_ 錯誤 \_ 的資料，而 *pcbSubkey* 則會指出所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為系統錯誤碼。 如果 *pKeyName* 不存在，則傳回值為「找 \_ 不到錯誤檔案」 \_ \_ 。

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
| Unicode 與 ANSI 名稱<br/>   | **EnumPrinterKeyW** (Unicode) 和 **EnumPrinterKeyA** (ANSI) <br/>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




