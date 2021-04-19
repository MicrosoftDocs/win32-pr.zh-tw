---
description: SetDefaultPrinter 函式會設定本機電腦上目前使用者之預設印表機的印表機名稱。
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: 'SetDefaultPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985243"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter 函式

**SetDefaultPrinter** 函式會設定本機電腦上目前使用者之預設印表機的印表機名稱。

## <a name="syntax"></a>語法


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszPrinter* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含預設印表機名稱。 若為遠端印表機連線，名稱格式為 [ **\\\\** _伺服器_ *_\\_* _printername_]。 若為本機印表機，名稱格式為 *printername*。

如果此參數為 **Null** 或空字串，也就是 ""， **SetDefaultPrinter** 會從其中一個已安裝的印表機選取預設印表機。 如果預設印表機已經存在，在此參數中使用 **Null** 或空字串呼叫 **SetDefaultPrinter** ，可能會變更預設印表機。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

使用這個方法時，您必須指定有效的印表機、驅動程式和埠。 如果無效，則 Api 不會失敗，但不會定義結果。 這可能會導致其他程式將印表機設定回先前的有效印表機。 您可以使用 [**>enumprinters**](enumprinters.md) 來取得印表機名稱、驅動程式名稱，以及所有可用印表機的埠名稱。

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
| Unicode 與 ANSI 名稱<br/>   | **SetDefaultPrinterW** (Unicode) 和 **SetDefaultPrinterA** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




