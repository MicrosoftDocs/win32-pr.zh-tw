---
description: 將印表機驅動程式上傳至列印伺服器驅動程式存放區，以便藉由呼叫 InstallPrinterDriverFromPackage 來進行安裝。
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: 'UploadPrinterDriverPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 15347171299e370bd5e0128976f65e4de1f7034b083b16880ac21659bfac35f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233866"
---
# <a name="uploadprinterdriverpackage-function"></a>UploadPrinterDriverPackage 函式

將印表機驅動程式上傳至列印伺服器的驅動程式存放區，以便藉由呼叫 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md)來進行安裝。

## <a name="syntax"></a>語法


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszServer* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定列印伺服器的名稱。 如果伺服器是本機電腦，請使用 **Null** 。

</dd> <dt>

*pszInfPath* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定驅動程式 .inf 檔案的來源路徑。

</dd> <dt>

*pszEnvironment* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定伺服器的處理器架構 (例如 Windows NT x86) 。 這可以是 **Null**。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這可以是下列其中一個值：



| 值                                                                                                                                                                                     | 意義                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | 上傳期間將不會顯示 UI。<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | 即使封裝已在伺服器的驅動程式存放區中，也會上傳檔案。<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | 將會先檢查伺服器的驅動程式存放區，然後再上傳，以查看套件是否已存在。 如果已設定 UPDP_UPLOAD_ALWAYS，則會忽略此設定。<br/> |



 

</dd> <dt>

*hwnd* \[在\]
</dt> <dd>

複製使用者介面的控制碼。

</dd> <dt>

*pszDestInfPath* \[擴展\]
</dt> <dd>

驅動程式存放區中複製驅動程式 .inf 檔案的目的地路徑指標。

</dd> <dt>

*pcchDestInfPath* \[in、out\]
</dt> <dd>

在 [輸入] 上，指定 *pszDestInfPath* 緩衝區的大小（以字元為單位）。 在輸出時，會接收路徑字串的大小（以字元為單位），包括終止的 null 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S_OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。

可以上傳一次只能上傳一個封裝。 如果封裝相依于其他套件，則必須分別上傳。

只可上傳已簽署的驅動程式套件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **UploadPrinterDriverPackageW** (Unicode) 和 **UploadPrinterDriverPackageA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

