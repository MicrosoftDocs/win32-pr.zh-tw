---
description: 抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: 'GetCorePrinterDrivers 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319091"
---
# <a name="getcoreprinterdrivers-function"></a>GetCorePrinterDrivers 函式

抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。

## <a name="syntax"></a>語法


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszServer* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定列印伺服器的名稱。 針對本機電腦使用 **Null** 。

</dd> <dt>

*pszEnvironment* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。 這可以是 **Null**。

</dd> <dt>

*pszzCoreDriverDependencies* \[在\]
</dt> <dd>

以 null 終止的多字串指標，指定核心印表機驅動程式的 Guid。

</dd> <dt>

*cCorePrinterDrivers* \[在\]
</dt> <dd>

*PszzCoreDriverDependencies* 中的字串數目。

</dd> <dt>

*pCorePrinterDrivers* \[擴展\]
</dt> <dd>

一或多個 [**核心 \_ 印表機 \_ 驅動程式**](core-printer-driver.md) 結構的陣列指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **GetCorePrinterDriversW** (Unicode) 和 **GetCorePrinterDriversA** (ANSI) <br/>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

