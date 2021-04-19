---
description: GetDefaultPrinter 函式會針對本機電腦上的目前使用者，抓取預設印表機的印表機名稱。
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: 'GetDefaultPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985447"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter 函式

**GetDefaultPrinter** 函式會針對本機電腦上的目前使用者，抓取預設印表機的印表機名稱。

## <a name="syntax"></a>語法


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszBuffer* \[在\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收以 null 終止的字元字串，其中包含預設印表機名稱。 如果這個參數為 **Null**，則函式會失敗，而且 *pcchBuffer* 所指向的變數會傳回所需的緩衝區大小（以字元為單位）。

</dd> <dt>

*pcchBuffer* \[in、out\]
</dt> <dd>

在 [輸入] 上，指定 *pszBuffer* 緩衝區的大小（以字元為單位）。 在輸出時，會接收印表機名稱字串的大小（以字元為單位），包括結束的 null 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值，且 *pcchBuffer* 所指向的變數包含複製到 *pszBuffer* 緩衝區的字元數，包括結束的 null 字元。

如果此函式失敗，則傳回值為零。



| 值                       | 意義                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_緩衝區不足的錯誤 \_ | *PszBuffer* 緩衝區太小。 *PcchBuffer* 所指向的變數包含所需的緩衝區大小（以字元為單位）。 |
| \_ \_ \_ 找不到錯誤檔案     | 沒有預設印表機。                                                                                                   |



 

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
| Unicode 與 ANSI 名稱<br/>   | **GetDefaultPrinterW** (Unicode) 和 **GetDefaultPrinterA** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




