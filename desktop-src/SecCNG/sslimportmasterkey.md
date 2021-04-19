---
description: 執行伺服器端安全通訊端層通訊協定 (SSL) 金鑰交換操作。
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: 'SslImportMasterKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993126"
---
# <a name="sslimportmasterkey-function"></a>SslImportMasterKey 函式

**SslImportMasterKey** 函式會 (SSL) 金鑰交換作業來執行伺服器端 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
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

*phMasterKey* \[擴展\]
</dt> <dd>

要接收 [*主要金鑰*](/windows/desktop/SecGloss/m-gly)的控制碼指標。

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

*pbEncryptedKey* \[在\]
</dt> <dd>

緩衝區的指標，其中包含加密的 premaster 秘密金鑰，並以伺服器的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 加密。

</dd> <dt>

*cbEncryptedKey* \[在\]
</dt> <dd>

*PbEncryptedKey* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

將此參數設定為 **NCRYPT \_ SSL \_ 伺服器 \_ 旗** 標，表示這是伺服器呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | 其中一個提供的控制碼無效。<br/>                     |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhMasterKey* 參數為 **Null**。<br/>                      |



 

## <a name="remarks"></a>備註

此函式會將 premaster 秘密解密、計算 SSL 主要密碼，然後將此物件的控制碼傳回給呼叫者。 然後，您可以使用此主要金鑰來衍生 SSL 工作階段金鑰，並完成 SSL 交握。

> [!Note]  
> 使用 [*RSA*](/windows/desktop/SecGloss/r-gly) 金鑰交換演算法時，會使用此函式。 使用 [*DH*](/windows/desktop/SecGloss/d-gly) 時，伺服器程式碼會改為呼叫 [**SslGenerateMasterKey**](sslgeneratemasterkey.md) 。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

