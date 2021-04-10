---
description: 計算憑證驗證期間使用的雜湊。
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: 'SslComputeClientAuthHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192299"
---
# <a name="sslcomputeclientauthhash-function"></a>SslComputeClientAuthHash 函式

**SslComputeClientAuthHash** 函式會計算 [*憑證*](/windows/desktop/SecGloss/c-gly)驗證期間所使用的 [*雜湊*](/windows/desktop/SecGloss/h-gly)。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
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

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*hMasterKey* \[在\]
</dt> <dd>

[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。

</dd> <dt>

*hHandshakeHash* \[在\]
</dt> <dd>

目前為止所計算之交握雜湊的控制碼。

</dd> <dt>

*pszAlgId* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，可識別所要求的 [*密碼編譯演算法*](/windows/desktop/SecGloss/c-gly)。 這可以是其中一個標準的 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 或另一個已註冊演算法的識別碼。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

接收 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly)的緩衝區位址。 *CbOutput* 參數包含這個緩衝區的大小。 如果此參數為 **Null**，此函式會將所需的大小（以位元組為單位）放在 *pcbResult* 參數所指向的 **DWORD** 中。

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

*PbOutput* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pcbResult* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，指定寫入至 *pbOutput* 緩衝區之雜湊的長度（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl> | 其中一個提供的控制碼無效。<br/> |



 

## <a name="remarks"></a>備註

**SslComputeClientAuthHash** 函式會計算在 SSL 信號交換的憑證驗證訊息中傳送的雜湊。 雜湊值的計算方式是建立包含主要密碼的雜湊，並在其中傳送或接收所有先前的交握訊息雜湊。 如需 SSL 交握順序的詳細資訊，請參閱 [安全通訊端層 (ssl) 交握的說明](https://support.microsoft.com/kb/257591)。

雜湊的計算方式取決於所使用的通訊協定和加密套件。 此外，雜湊取決於所使用的用戶端驗證金鑰類型; *pszAlgId* 參數會指出用於用戶端驗證的金鑰類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

