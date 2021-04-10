---
description: 傳回 NCRYPT \_ SSL \_ 密碼 \_ 長度結構，其中包含輸入通訊協定、加密套件和金鑰類型的標頭和結尾長度。
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: 'SslLookupCipherLengths 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943877"
---
# <a name="ssllookupcipherlengths-function"></a>SslLookupCipherLengths 函式

**SslLookupCipherLengths** 函式會傳回 [**NCRYPT \_ SSL \_ 加密 \_ 長度**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**)結構，其中包含輸入通訊協定、加密套件和金鑰類型的標頭和結尾長度。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*dwProtocol* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。

</dd> <dt>

*dwCipherSuite* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。

</dd> <dt>

*dwKeyType* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。 對於非 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯 (ECC) 的金鑰類型，請將此參數設定為零。

</dd> <dt>

*pCipherLengths* \[擴展\]
</dt> <dd>

接收 [**NCRYPT \_ SSL \_ 密碼 \_ 長度**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) 結構之緩衝區的指標。

</dd> <dt>

*cbCipherLengths* \[在\]
</dt> <dd>

*PCipherLengths* 參數所指向之緩衝區的長度（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

此參數會保留供日後使用，且必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 參數包含不正確指標。<br/>                                                      |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PCipherLengths* 參數設定為 **Null** ，或 *cbCipherLengths* 所指定的緩衝區長度太短。<br/> |
| <dl> 不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt> </dl>         | *DwFlags* 參數必須設定為零。<br/>                                                                            |



 

## <a name="remarks"></a>備註

**SslLookupCipherLengths** 函式是針對 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)（ (TLS) 1.1 或更新版本的交談）進行呼叫，以查詢要求的通訊協定、加密套件和金鑰類型的標頭和結尾長度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

