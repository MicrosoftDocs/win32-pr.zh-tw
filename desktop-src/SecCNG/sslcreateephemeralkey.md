---
description: 建立在安全通訊端層通訊協定 (SSL) 交握期間所發生驗證期間所使用的暫時金鑰。
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: 'SslCreateEphemeralKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: a6a54de2865df805af51b054c22d455d52914a5b00514767d432ceda28c16a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907095"
---
# <a name="sslcreateephemeralkey-function"></a>SslCreateEphemeralKey 函式

**SslCreateEphemeralKey** 函式會建立暫時金鑰，以供在 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 交握期間進行驗證時使用。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*phEphemeralKey* \[擴展\]
</dt> <dd>

暫時金鑰的控制碼。

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

其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。 針對非 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯 (ECC) 的索引鍵類型，將此參數設定為零。

</dd> <dt>

*dwKeyBitLen* \[在\]
</dt> <dd>

金鑰的長度 (位元數)。

</dd> <dt>

*pbParams* \[在\]
</dt> <dd>

緩衝區的指標，其中包含要建立之索引鍵的參數。 如果未使用 [*diffie-hellman (暫時) 金鑰交換演算法*](/windows/desktop/SecGloss/d-gly) (DHE) 加密套件，請將 *pbParams* 參數設定為 **Null** ，並將 *cbParams* 參數設定為零。

</dd> <dt>

*cbParams* \[在\]
</dt> <dd>

*PbParams* 緩衝區中資料的長度（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。



| 傳回碼/值                                                                                                                                                       | Description                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 記憶體不足，無法配置緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 控制碼無效。<br/>              |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | 其中一個提供的參數無效。<br/>         |



 

## <a name="remarks"></a>備註

使用 DHE 加密套件時，內部 SSL 執行會將伺服器 *p* 和 *g* 參數傳遞至 *pbParams* 和 *cbParams* 參數中的 **SslCreateEphemeralKey** 函式。

*PbParams* 緩衝區中的資料格式與設定 [**BCRYPT \_ DH \_ PARAMETERS**](cng-property-identifiers.md)屬性時所使用的格式相同，且開頭為 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

