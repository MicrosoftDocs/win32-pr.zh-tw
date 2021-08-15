---
description: 抓取用於用戶端驗證之交握雜湊的控制碼。
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: 'SslCreateClientAuthHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 96f1e7fa0de86439f89bf5c4c610bf5b46640533071260852c47321c5a1c6673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907085"
---
# <a name="sslcreateclientauthhash-function"></a>SslCreateClientAuthHash 函式

**SslCreateClientAuthHash** 函式會抓取用於用戶端驗證之交握 [*雜湊*](/windows/desktop/SecGloss/h-gly)的控制碼。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*phHandshakeHash* \[擴展\]
</dt> <dd>

要接收雜湊控制碼之 **NCRYPT \_ 雜湊 \_ 控制碼** 變數的指標。

</dd> <dt>

*dwProtocol* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。

</dd> <dt>

*dwCipherSuite* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。

</dd> <dt>

*pszHashAlgId* \[在\]
</dt> <dd>

其中一個 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 值。

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
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhHandshakeHash* 參數設定為 **Null**。<br/>                               |
| <dl> 不 <dt>**超過 \_不 \_ 支援**</dt>的 <dt>0x80090029L</dt> </dl>     | 指定的介面版本不支援選取的函式。<br/> |
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 記憶體不足，無法配置緩衝區。<br/>                                          |
| <dl> 不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt> </dl>         | *DwFlags* 參數必須設定為零。<br/>                                      |



 

## <a name="remarks"></a>備註

**SslCreateClientAuthHash** 函式是針對 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)（ (TLS) 1.2 或更新版本的交談）進行呼叫，以建立用來雜湊交握訊息的雜湊物件。 它會針對每個可用於用戶端驗證簽章的 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly) 呼叫一次。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

