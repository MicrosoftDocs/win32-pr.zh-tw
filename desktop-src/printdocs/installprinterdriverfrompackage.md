---
description: 從列印伺服器驅動程式存放區中的驅動程式套件安裝印表機驅動程式。
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: 'InstallPrinterDriverFromPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194964"
---
# <a name="installprinterdriverfrompackage-function"></a>InstallPrinterDriverFromPackage 函式

從列印伺服器的驅動程式存放區中的驅動程式套件安裝印表機驅動程式。

## <a name="syntax"></a>語法


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszServer* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定列印伺服器的名稱。 **Null** 表示本機電腦。

</dd> <dt>

*pszInfPath* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定列印驅動程式 .inf 檔案的驅動程式存放區路徑。 **Null** 表示驅動程式位於隨附于 Windows 的 inf 檔案中。

</dd> <dt>

*pszDriverName* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定驅動程式的名稱。

</dd> <dt>

*pszEnvironment* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。 這可以是 **Null**。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這只能是0或 IPDFP \_ 複製 \_ 所有檔案 \_ 。 值為0表示必須在印表機驅動程式目錄中新增印表機驅動程式，而且必須在目前使用中的對應檔案之後，才複製印表機驅動程式目錄中的任何檔案。 IPDFP \_ 複製所有檔案的 \_ 值 \_ 表示必須新增印表機驅動程式和印表機驅動程式目錄中的所有檔案。 當 *dwFlags* 的值為 IPDFP 複製所有檔案時，會忽略檔案時間戳記 \_ \_ \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。

**InstallPrinterDriverFromPackage** 也會安裝套件中的其他檔案，例如色彩設定檔和列印處理器。

當使用者使用終端機服務登入時，使用者必須具備印表機管理許可權，才能安裝在遠端電腦或本機電腦上。

只有已簽署的封裝可以安裝在遠端電腦上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) 和 **InstallPrinterDriverFromPackageA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

