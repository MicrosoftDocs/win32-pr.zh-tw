---
description: CloseSpoolFileHandle 函式會關閉與應用程式目前所提交列印工作相關聯之多工緩衝處理檔案的控制碼。
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: 'CloseSpoolFileHandle 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974259"
---
# <a name="closespoolfilehandle-function"></a>CloseSpoolFileHandle 函式

**CloseSpoolFileHandle** 函式會關閉與應用程式目前所提交列印工作相關聯之多工緩衝處理檔案的控制碼。

## <a name="syntax"></a>語法


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

提交工作之印表機的控制碼。 這應該是用來取得 *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md)的相同控制碼。

</dd> <dt>

*hSpoolFile* \[在\]
</dt> <dd>

要關閉之多工緩衝處理檔案的控制碼。 如果在呼叫 [**GetSpoolFileHandle**](getspoolfilehandle.md)之後尚未呼叫 [**CommitSpoolData**](commitspooldata.md) ，則這應該與 **GetSpoolFileHandle** 所傳回的控制碼相同。 否則，它應該是最近呼叫 **CommitSpoolData** 所傳回的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，**則為 TRUE**，否則為 **FALSE** 。

## <a name="remarks"></a>備註

您的應用程式不能在 *hPrinter* 上呼叫 [**ClosePrinter**](closeprinter.md) ，直到它上次存取多工緩衝處理檔案為止。 然後，它應該呼叫 **CloseSpoolFileHandle** ，後面接著 **ClosePrinter**。 在原始 *hPrinter* 關閉之後，嘗試存取多工緩衝處理檔案控制代碼會失敗，即使檔案控制代碼本身尚未關閉也一樣。 如果先呼叫 **ClosePrinter** ， **CloseSpoolFileHandle** 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




