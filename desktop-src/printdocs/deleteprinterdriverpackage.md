---
description: 從驅動程式存放區刪除印表機驅動程式套件。
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: 'DeletePrinterDriverPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991858"
---
# <a name="deleteprinterdriverpackage-function"></a>DeletePrinterDriverPackage 函式

從驅動程式存放區刪除印表機驅動程式套件。

## <a name="syntax"></a>語法


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszServer* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定要從中刪除驅動程式套件的列印伺服器名稱。 **Null** 指標值表示本機電腦。

</dd> <dt>

*pszInfPath* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定驅動程式 .inf 檔案的路徑 \* 。

</dd> <dt>

*pszEnvironment* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。 這可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果作業成功，則為 [確定]。

E \_ ACCESSDENIED，如果封裝隨附于 Windows。

HRESULT \_ 程式碼 (錯誤 \_ 列印 \_ 驅動程式 \_ 封裝 \_ 在 \_ 使用中) （如果正在使用套件）。

否則， **HRESULT** 將會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。

使用此功能時，無法移除隨附于 Windows 的驅動程式套件。

使用者必須具備印表機管理許可權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **DeletePrinterDriverPackageW** (Unicode) 和 **DeletePrinterDriverPackageA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

