---
description: 開啟私密金鑰的控制碼。
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: 'SslOpenPrivateKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112688"
---
# <a name="sslopenprivatekey-function"></a>SslOpenPrivateKey 函式

**SslOpenPrivateKey** 函式會開啟 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)的控制碼。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*phPrivateKey* \[擴展\]
</dt> <dd>

要在其中將控制碼寫入至私密金鑰的緩衝區位址。

當您完成使用索引鍵時，您應該呼叫 [**SslFreeObject**](sslfreeobject.md)函式來釋放 *phPrivateKey* 。

</dd> <dt>

*pCertCoNtext* \[在\]
</dt> <dd>

從中取得私密金鑰的憑證位址。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 控制碼無效。<br/>                       |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhPrivateKey* 或 *PCertCoNtext* 參數為 **Null**。<br/>   |



 

## <a name="remarks"></a>備註

取得的私密金鑰是 [*憑證*](/windows/desktop/SecGloss/c-gly)內 [*公開/私密金鑰*](/windows/desktop/SecGloss/p-gly)組的一部分。 此函式只會從 *pCertCoNtext* 參數所指定的憑證解壓縮私密金鑰。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

