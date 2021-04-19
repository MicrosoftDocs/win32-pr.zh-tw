---
description: 傳回密碼編譯 API：新一代 (CNG) 雜湊演算法的演算法識別碼，用於傳輸層安全性通訊協定 (TLS) 虛擬隨機函式 (適用于輸入通訊協定、加密套件和金鑰類型的) PRF。
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: 'SslGetCipherSuitePRFHashAlgorithm 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979847"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>SslGetCipherSuitePRFHashAlgorithm 函式

**SslGetCipherSuitePRFHashAlgorithm** 函式會傳回「密碼編譯 API：新一代」 (CNG) [*雜湊演算法*](/windows/desktop/SecGloss/h-gly)的演算法識別碼，用於 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly) (TLS) [*虛擬隨機函式*](/windows/desktop/SecGloss/p-gly) (適用于輸入通訊協定、加密套件和金鑰類型的 PRF) 。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
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

*szPRFHash* \[擴展\]
</dt> <dd>

將用於 TLS PRF 之雜湊的其中一個 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

此參數會保留供日後使用，且必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 參數包含不正確指標。<br/>                |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *SzPRFHash* 參數設定為 **Null**。<br/>                                     |
| <dl> 不 <dt>**超過 \_不 \_ 支援**</dt>的 <dt>0x80090029L</dt> </dl>     | 指定的介面版本不支援選取的函式。<br/> |
| <dl> 不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt> </dl>         | *DwFlags* 參數必須設定為零。<br/>                                      |



 

## <a name="remarks"></a>備註

此 **SslGetCipherSuitePRFHashAlgorithm** 函式會針對 tls 1.2 或更新版本的交談呼叫，以查詢將在 tls PRF 中使用的雜湊演算法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

