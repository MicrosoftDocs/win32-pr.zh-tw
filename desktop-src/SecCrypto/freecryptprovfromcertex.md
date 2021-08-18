---
description: 將控制碼釋放給密碼編譯服務提供者 (CSP) 或密碼編譯 API：新一代 (CNG) 金鑰。
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: b887fd7cd37e8963430378590552273b0856dc2cf73e9d0da15ab41a5a622447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006736"
---
# <a name="freecryptprovfromcertex-function"></a>FreeCryptProvFromCertEx 函式

**FreeCryptProvFromCertEx** 函式會將控制碼釋放給 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 或密碼編譯 API：新一代 (CNG) 金鑰。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
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

CAPICOM CSP 的控制碼或 CNG 金鑰的控制碼。

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

接收有關金鑰之其他資訊的 **DWORD** 變數位址。 這可以是下列其中一個值。



| 值                                                                                                                                                                                | 意義                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**在 \_ KEYEXCHANGE**</dt> </dl>                     | 金鑰組是一組金鑰交換。<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ SIGNATURE**</dt> </dl>                           | 金鑰組是一組簽章組。<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**CERT \_ NCRYPT \_ 金鑰 \_ 規格**</dt> </dl> | 金鑰是 CNG 金鑰。<br/> **Windows Server 2003 和 Windows XP：** 不支援這個值。<br/> |



 

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
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
