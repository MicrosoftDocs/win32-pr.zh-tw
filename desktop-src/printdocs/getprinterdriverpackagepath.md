---
description: 抓取列印伺服器上指定之印表機驅動程式套件的路徑。
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: 'GetPrinterDriverPackagePath 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5058d57a0275019c5e603673d260c9969cc0b5d5641dea15e09ffe242addff10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600798"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath 函式

抓取列印伺服器上指定之印表機驅動程式套件的路徑。

## <a name="syntax"></a>語法


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
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

*pszLanguage* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定要安裝之驅動程式的[多語系消費者介面](/windows/desktop/Intl/mui-resource-management)語言。 這可以是 **Null**。

</dd> <dt>

*pszPackageID* \[在\]
</dt> <dd>

常數、以 null 結束的字串指標，指定驅動程式套件的識別碼。

</dd> <dt>

*pszDriverPackageCab* \[in、out\]
</dt> <dd>

以 null 結束的字串指標，指定驅動程式套件的封包檔路徑。 這可以是 **Null**。 請參閱＜備註＞。

</dd> <dt>

*cchDriverPackageCab* \[在\]
</dt> <dd>

*PszDriverPackageCab* 緩衝區的大小（以字元為單位）。 這可以是 **Null**。

</dd> <dt>

*pcchRequiredSize* \[擴展\]
</dt> <dd>

*PszDriverPackageCab* 緩衝區所需大小的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。

如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

若要取得 *cchDriverPackageCab* 的值，請使用 **Null** 做為 *pszDriverPackageCab* 的值來呼叫函數。 使用 *pcchRequiredSize* 中傳回的值做為 *cchDriverPackageCab* 的值，然後再次呼叫函數。

*PszPackageID* 通常是從 [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)的呼叫所取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **GetPrinterDriverPackagePathW** (Unicode) 和 **GetPrinterDriverPackagePathA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

