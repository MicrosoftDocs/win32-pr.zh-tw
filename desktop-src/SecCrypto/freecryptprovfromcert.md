---
description: 將密碼編譯服務提供者的控制碼釋放 (CSP) ，並選擇性地刪除 GetCryptProvFromCert 函式所建立的暫存容器。
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851307"
---
# <a name="freecryptprovfromcert-function"></a>FreeCryptProvFromCert 函式

> [!IMPORTANT]
> 此 API 即將淘汰。 Microsoft 可能會在未來的版本中移除此 API。

 

**FreeCryptProvFromCert** 函式會將 [*密碼編譯服務提供者*](../secgloss/c-gly.md) () 的控制碼釋出，並選擇性地刪除 [**GetCryptProvFromCert**](getcryptprovfromcert.md)函數所建立的暫存容器。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fAcquired* \[在\]
</dt> <dd>

值，指定是否從 [*憑證*](../secgloss/c-gly.md)取得提供者控制碼。

</dd> <dt>

*hProv* \[在\]
</dt> <dd>

CSP [**HCRYPTPROV**](hcryptprov.md) 結構的指標。

</dd> <dt>

*pwszCapiProvider* \[在中，選擇性\]
</dt> <dd>

提供者名稱之以 null 結束的字串指標。

</dd> <dt>

*dwProviderType* \[在\]
</dt> <dd>

指定 CSP 類型。 這可以是零或其中一個 [密碼編譯提供者類型](cryptographic-provider-types.md)。 如果這個成員是零，金鑰容器就是其中一個 CNG 金鑰儲存提供者。

</dd> <dt>

*pwszTmpContainer* \[在中，選擇性\]
</dt> <dd>

暫時金鑰容器名稱的以 null 結束的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
