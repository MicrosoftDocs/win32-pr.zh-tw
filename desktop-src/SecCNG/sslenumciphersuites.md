---
description: 列舉安全通訊端層的通訊協定 (SSL) 通訊協定提供者所支援的加密套件。
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: 'SslEnumCipherSuites 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318992"
---
# <a name="sslenumciphersuites-function"></a>SslEnumCipherSuites 函式

**SslEnumCipherSuites** 函式會列舉 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者所支援的加密套件。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*hPrivateKey* \[在中，選擇性\]
</dt> <dd>

[*私密金鑰*](/windows/desktop/SecGloss/p-gly)的控制碼。 指定私密金鑰時， **SslEnumCipherSuites** 會列舉與私密金鑰相容的加密套件。 例如，如果私密金鑰是 DSS 金鑰，則只 \_ 會傳回 dss DHE 加密套件。 如果私密金鑰是 RSA 金鑰，但不支援原始解密作業，則不會傳回 SSL2 加密套件。

當您未指定私密金鑰時，請將此參數設定為 **Null** 。

> [!Note]  
> *HPrivateKey* 控制碼是藉由呼叫 [**SslOpenPrivateKey**](sslopenprivatekey.md)函數來取得的。 不支援從 [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 函數取得的控制碼。

 

</dd> <dt>

*ppCipherSuite* \[擴展\]
</dt> <dd>

[**NCRYPT \_ SSL \_ 密碼 \_ 套件**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)結構的指標，用來接收清單中下一個加密套件的位址。

</dd> <dt>

*ppEnumState* \[in、out\]
</dt> <dd>

緩衝區的指標，指出加密套件清單中目前的位置。

在第一次呼叫 **SslEnumCipherSuites** 時，將指標設定為 **Null** 。 在每個後續的呼叫中，將未修改的值傳遞回 **SslEnumCipherSuites**。

如果沒有更多可用的加密套件，您應該呼叫 [**SslFreeBuffer**](sslfreebuffer.md)函數來釋放 *ppEnumState* 。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                    | Description                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>      | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl> | 其中一個提供的控制碼無效。<br/>                     |
| <dl> 不 <dt>**超過 \_沒有 \_ 其他 \_ 專案**</dt> <dt>0x8009002AL</dt> </dl> | 不支援其他加密套件。<br/>                    |



 

## <a name="remarks"></a>備註

若要列舉 SSL 提供者所支援的所有加密套件，請在迴圈中呼叫 **SslEnumCipherSuites** 函式，直到不超過最 **大的 \_ \_ \_ 專案** 傳回為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Ncrypt .lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NCRYPT \_ SSL \_ 密碼 \_ 套件**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

