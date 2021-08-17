---
description: 取得用來雜湊交握訊息的雜湊控制碼。
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: 'SslCreateHandshakeHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ea481a5b577c41eafddf9db8d80b4a3a1fe42d801bf96ed8cbc57127a4a8d91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906825"
---
# <a name="sslcreatehandshakehash-function"></a>SslCreateHandshakeHash 函式

**SslCreateHandshakeHash** 函數會取得用來雜湊交握訊息的雜湊控制碼。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
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

雜湊控制碼，可傳遞給其他 SSL 提供者函式。

</dd> <dt>

*dwProtocol* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。

> [!Note]  
> 此函式不會搭配 SSL 2.0 通訊協定使用。

 

</dd> <dt>

*dwCipherSuite* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 記憶體不足，無法配置雜湊緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 控制碼無效。<br/>                   |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhHandshakeHash* 為 null。<br/>                            |



 

## <a name="remarks"></a>備註

**SslCreateHandshakeHash** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。

1.  呼叫 **SslCreateHandshakeHash** 函數來取得雜湊控制碼。
2.  [**SslHashHandshake**](sslhashhandshake.md)函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。
3.  使用雜湊控制碼呼叫 [**SslComputeFinishedHash**](sslcomputefinishedhash.md) 函數，以取得雜湊資料的摘要。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

