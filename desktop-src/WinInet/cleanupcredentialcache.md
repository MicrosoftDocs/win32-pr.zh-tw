---
title: CleanupCredentialCache 函式
description: 由特定安全性支援提供者所執行 (SSP) 以排清 SSP 認證快取。
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- CleanupCredentialCache 函數 WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093876"
---
# <a name="cleanupcredentialcache-function"></a>CleanupCredentialCache 函式

**CleanupCredentialCache** 函式是由特定的安全性支援提供者所執行， (ssp) 來排清 SSP 認證快取。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

**CleanupCredentialCache** 函式是由下列 ssp 所執行：

-   MSNSSPC.dll
-   MSAPSSPC.dll

這些 Ssp 的 **CleanupCredentialCache** 執行一律會傳回 **TRUE**。

在嘗試取得模組控制碼以匯出 **CleanupCredentialCache** 之前，應用程式必須確認已載入的 ssp 是執行 **CleanupCredentialCache** 函式的其中一個已知 ssp。

為了排清 SSP 認證快取，應用程式必須藉由呼叫 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式來取得 ssp 的模組控制碼。 取得模組之後，應用程式應藉由呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)函式來匯出由 SSP 所執行的 **CleanupCredentialCache** 函式，並將 **GetModuleHandle** 和 **CleanupCredentialCache** 傳回的模組傳遞為輸入參數。

如同 WinINet API 的所有其他層面，無法從 DllMain 或全域物件的函式和析構函式中，安全地呼叫這個函式。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                                 |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll;</dt><dt>MSAPSSPC.dll</dt> </dl> |



 

