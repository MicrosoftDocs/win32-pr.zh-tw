---
description: CorePrinterDriverInstalled 函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: 'CorePrinterDriverInstalled 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027122"
---
# <a name="coreprinterdriverinstalled-function"></a>CorePrinterDriverInstalled 函式

**CorePrinterDriverInstalled** 函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。

## <a name="syntax"></a>語法


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
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

*CoreDriverGUID* \[在\]
</dt> <dd>

核心印表機驅動程式的 GUID。

</dd> <dt>

*ftDriverDate* \[在\]
</dt> <dd>

核心印表機驅動程式的日期。

</dd> <dt>

*dwlDriverVersion* \[在\]
</dt> <dd>

核心印表機驅動程式的版本。

</dd> <dt>

*pbDriverInstalled* \[擴展\]
</dt> <dd>

如果已安裝驅動程式或較新的版本， **則為 TRUE** 的指標，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **CorePrinterDriverInstalledW** (Unicode) 和 **CorePrinterDriverInstalledA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

