---
description: 計算 (SSL) 主要秘密金鑰的安全通訊端層通訊協定。
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: 'SslGenerateMasterKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386298"
---
# <a name="sslgeneratemasterkey-function"></a>SslGenerateMasterKey 函式

**SslGenerateMasterKey** 函式會 (SSL) 主要秘密金鑰來計算 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*hPrivateKey* \[在\]
</dt> <dd>

交換中所使用之 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 的控制碼。

</dd> <dt>

*hPublicKey* \[在\]
</dt> <dd>

交換中所使用 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 的控制碼。

</dd> <dt>

*phMasterKey* \[擴展\]
</dt> <dd>

所產生之 [*主要金鑰*](/windows/desktop/SecGloss/m-gly)的控制碼指標。

</dd> <dt>

*dwProtocol* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。

</dd> <dt>

*dwCipherSuite* \[在\]
</dt> <dd>

其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。

</dd> <dt>

*pParameterList* \[在\]
</dt> <dd>

[**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx)緩衝區陣列的指標，其中包含用來做為金鑰交換作業一部分的資訊。 確切的緩衝區集取決於所使用的通訊協定和加密套件。 清單最少會包含緩衝區，其中包含用戶端和伺服器提供的隨機值。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

接收以伺服器的公開金鑰加密之 premaster 秘密的緩衝區位址。 *CbOutput* 參數包含這個緩衝區的大小。 如果此參數為 **Null**，則此函式會傳回 *pcbResult* 參數所指向之 **DWORD** 中所需的大小（以位元組為單位）。

> [!Note]  
> 執行 RSA 金鑰交換時，會使用這個緩衝區。

 

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

*PbOutput* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbResult* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，要在其中放置寫入至 *pbOutput* 緩衝區的位元組數目。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定此函數是否用於用戶端或伺服器端金鑰交換。



| 值                                                                                                                                                                                                                                                      | 意義                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_SSL \_ 用戶端 \_ 旗**</dt>標 <dt>0x00000001</dt> </dl> | 指定用戶端金鑰交換。<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_SSL \_ 伺服器 \_ 旗**</dt>標 <dt>0x00000002</dt> </dl> | 指定伺服器端金鑰交換。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | 其中一個提供的控制碼無效。<br/>                     |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhMasterKey* 或 *hPublicKey* 參數無效。<br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

