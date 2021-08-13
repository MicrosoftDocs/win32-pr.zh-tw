---
description: 安全通訊端層通訊協定 (SSL) 通訊協定提供者匯入金鑰。
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: 'SslImportKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 00dbe668c28e234c0ed4fdc7950b6b9627ae5aaba46bbef4e17d1eb8cb213f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906086"
---
# <a name="sslimportkey-function"></a>SslImportKey 函式

**SslImportKey** 函式會 (SSL) 通訊協定提供者，將金鑰匯入 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*phKey* \[擴展\]
</dt> <dd>

要接收匯入金鑰之 [*密碼編譯金鑰*](/windows/desktop/SecGloss/c-gly) 的控制碼指標。

</dd> <dt>

*pszBlobType* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串，其中包含指定 *pbInput* 緩衝區中所包含之 [*BLOB*](/windows/desktop/SecGloss/b-gly)類型的識別碼。 這可以是下列其中一個值。



| 值                                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**BCRYPT \_ DH \_ 公用 \_ BLOB**</dt> </dl>    | 匯出 Diffie-Hellman 的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)。 *PbOutput* 緩衝區會立即接收 [**BCRYPT \_ DH \_ 金鑰 \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob)結構，後面接著金鑰資料。<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt> </dl>     |  (ECC) [*公開金鑰*](/windows/desktop/SecGloss/p-gly)匯出 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly)編譯。 *PbOutput* 緩衝區會立即接收 [**BCRYPT \_ ECCKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob)結構，後面接著金鑰資料。<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BCRYPT 不 \_ 透明的 \_ 金鑰 \_ BLOB**</dt> </dl> | 使用 (CSP) 的單一 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly)專用的格式來匯出 [*對稱金鑰*](/windows/desktop/SecGloss/s-gly)。 不透明的 Blob 無法轉移，而且必須使用產生 BLOB 的相同 CSP 來匯入。<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt> </dl>     | 匯出 [*RSA*](/windows/desktop/SecGloss/r-gly) 公開金鑰。 *PbOutput* 緩衝區會立即接收 [**BCRYPT \_ RSAKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob)結構，後面接著金鑰資料。<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[在\]
</dt> <dd>

包含 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly)的緩衝區指標。

</dd> <dt>

*cbKeyBlob* \[在\]
</dt> <dd>

*PbKeyBlob* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | 描述                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 控制碼無效。<br/>                       |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhKey* 參數為 **Null**。<br/>                            |



 

## <a name="remarks"></a>備註

您可以使用 **SslImportKey** 函式，在將工作階段金鑰從某個進程傳送到另一個進程的過程中，匯入工作階段金鑰。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

