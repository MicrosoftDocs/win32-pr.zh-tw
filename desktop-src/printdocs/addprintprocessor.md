---
description: AddPrintProcessor 函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: 'AddPrintProcessor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83de05dd6aa0ef6541322a45894dcf24cffa3cc6bebcbbd3b42e6c48941360b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868743"
---
# <a name="addprintprocessor-function"></a>AddPrintProcessor 函式

**AddPrintProcessor** 函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。

## <a name="syntax"></a>語法


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該安裝列印處理器之伺服器的名稱。 如果此參數為 **Null**，則會在本機安裝列印處理器。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定環境 (例如 Windows x86、Windows IA64 或 Windows x64) 。 如果這個參數是 **Null**，則會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。

</dd> <dt>

*pPathName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定包含列印處理器之檔案的名稱。 此檔案必須位於系統列印處理器目錄中。

</dd> <dt>

*pPrintProcessorName* \[在\]
</dt> <dd>

指定列印處理器名稱之以 null 結束的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

在呼叫 **AddPrintProcessor** 函式之前，應用程式應該確認包含列印處理器的檔案儲存在系統列印處理器目錄中。 應用程式可以藉由呼叫 [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) 函式來取出系統列印處理器目錄的名稱。

應用程式可以藉由呼叫 [**EnumPrintProcessors**](enumprintprocessors.md) 函數來判斷現有列印處理器的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrintProcessorW** (Unicode) 和 **AddPrintProcessorA** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

