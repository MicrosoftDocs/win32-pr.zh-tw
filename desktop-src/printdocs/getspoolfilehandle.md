---
description: GetSpoolFileHandle 函式會抓取與應用程式目前所提交之作業相關聯的多工緩衝處理檔案的控制碼。
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: 'GetSpoolFileHandle 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027460"
---
# <a name="getspoolfilehandle-function"></a>GetSpoolFileHandle 函式

**GetSpoolFileHandle** 函式會抓取與應用程式目前所提交之作業相關聯的多工緩衝處理檔案的控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

提交工作之印表機的控制碼。 這應該是用來提交作業的相同控制碼。  (使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會將控制碼傳回至多工緩衝處理檔案。

如果函式失敗，則會傳回 **不正確 \_ 控制碼 \_ 值**。

## <a name="remarks"></a>備註

使用多工緩衝處理檔案的控制碼時，您的應用程式可以使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 的呼叫來寫入多工緩衝處理檔案，後面接著 [**CommitSpoolData**](commitspooldata.md)。

您的應用程式不能在 *hPrinter* 上呼叫 [**ClosePrinter**](closeprinter.md) ，直到它上次存取多工緩衝處理檔案為止。 然後，它應該呼叫 [**CloseSpoolFileHandle**](closespoolfilehandle.md) ，後面接著 **ClosePrinter**。 在原始 *hPrinter* 關閉之後，嘗試存取多工緩衝處理檔案控制代碼會失敗，即使檔案控制代碼本身尚未關閉也一樣。 如果先呼叫 **ClosePrinter** ， **CloseSpoolFileHandle** 本身將會失敗。

如果在列印工作完成幕後處理之前呼叫這個函式，此函式將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetSpoolFileHandleW** (Unicode) 和 **GetSpoolFileHandleA** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

