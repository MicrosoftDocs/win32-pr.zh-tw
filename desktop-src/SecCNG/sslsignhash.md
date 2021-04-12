---
description: 使用指定的私密金鑰來簽署雜湊。
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: 'SslSignHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468900"
---
# <a name="sslsignhash-function"></a>SslSignHash 函式

**SslSignHash** 函數會使用指定的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)來簽署 [*雜湊*](/windows/desktop/SecGloss/h-gly)。 簽署進程會在伺服器上執行。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
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

*hPrivateKey* \[在\]
</dt> <dd>

用來簽署雜湊之私密金鑰的控制碼。

</dd> <dt>

*pbHashValue* \[在\]
</dt> <dd>

緩衝區的指標，其中包含要簽署的雜湊。

</dd> <dt>

*cbHashValue* \[在\]
</dt> <dd>

*PbHashValue* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pbSignature* \[擴展\]
</dt> <dd>

接收雜湊特徵標記的緩衝區位址。 *CbSignature* 參數包含這個緩衝區的大小。 若要判斷緩衝區的所需大小大小，請將 *pbSignature* 參數設定為 **Null**。 將會在 *pcbResult* 參數中傳回所需的緩衝區大小。

</dd> <dt>

*cbSignature* \[在\]
</dt> <dd>

*PbSignature* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbResult* \[擴展\]
</dt> <dd>

值的指標，此值會在完成時包含寫入至 *pbSignature* 緩衝區的實際位元組數目。

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



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

