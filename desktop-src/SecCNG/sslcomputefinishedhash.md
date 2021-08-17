---
description: 計算在安全通訊端層通訊協定的完成訊息中傳送的雜湊 (SSL) 信號交換。
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: 'SslComputeFinishedHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e0f23a58111bfcebbe668cd3b6c50a135da0dae240907f09a65d60ef1cebdda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907139"
---
# <a name="sslcomputefinishedhash-function"></a>SslComputeFinishedHash 函式

**SslComputeFinishedHash** 函式會計算在 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)的完成訊息中傳送的 [*雜湊*](/windows/desktop/SecGloss/h-gly) (SSL) 信號交換。 如需 SSL 交握順序的詳細資訊，請參閱 [安全通訊端層 (ssl) 交握的說明](https://support.microsoft.com/kb/257591)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*hMasterKey* \[在\]
</dt> <dd>

[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。

</dd> <dt>

*hHandshakeHash* \[在\]
</dt> <dd>

交握訊息雜湊的控制碼。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收完成訊息的雜湊。

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

*PbOutput* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

下列其中一個常數。



| 值                                                                                                                                                                                                                                                      | 意義                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_SSL \_ 用戶端 \_ 旗**</dt>標 <dt>0x00000001</dt> </dl> | 指定這是用戶端呼叫。<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_SSL \_ 伺服器 \_ 旗**</dt>標 <dt>0x00000002</dt> </dl> | 指定這是伺服器呼叫。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。



| 傳回碼/值                                                                                                                                                                | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | 其中一個提供的控制碼無效。<br/> |



 

## <a name="remarks"></a>備註

**SslComputeFinishedHash** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。

1.  呼叫 [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) 函數來取得雜湊控制碼。
2.  [**SslHashHandshake**](sslhashhandshake.md)函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。
3.  使用雜湊控制碼呼叫 **SslComputeFinishedHash** 函數，以取得雜湊資料的摘要。

雜湊值的計算方式是使用傳送或接收的所有先前交握訊息的雜湊來雜湊主要密碼。

*CbOutput* 的值會決定雜湊資料的長度。 使用 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 通訊協定時，應該一律為 12 (個位元組) 。 如需詳細資訊，請參閱 [TLS 通訊協定1.0 版](https://www.ietf.org/rfc/rfc2246.txt)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

