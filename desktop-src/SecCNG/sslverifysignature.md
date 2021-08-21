---
description: 使用提供的雜湊和公開金鑰，驗證指定的簽章。
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: 'SslVerifySignature 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905657"
---
# <a name="sslverifysignature-function"></a>SslVerifySignature 函式

**SslVerifySignature** 函式會使用提供的 [*雜湊*](/windows/desktop/SecGloss/h-gly)和 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)，驗證指定的簽章。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*hPublicKey* \[在\]
</dt> <dd>

公開金鑰的控制碼。

</dd> <dt>

*pbHashValue* \[在\]
</dt> <dd>

緩衝區的指標，其中包含要用來驗證簽章的雜湊。

</dd> <dt>

*cbHashValue* \[在\]
</dt> <dd>

*PbHashValue* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pbSignature* \[在\]
</dt> <dd>

緩衝區的指標，此緩衝區包含要驗證的簽章。

</dd> <dt>

*cbSignature* \[在\]
</dt> <dd>

*PbSignature* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                    | 描述                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl> | 其中一個提供的控制碼無效。<br/> |



 

## <a name="remarks"></a>備註

Windows 目前未呼叫 **SslVerifySignature** 函數。 此函式是 SSL 提供者介面的必要部分，應完全實作為以確保向前相容性。

[*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)的伺服器端目前的執行 (TLS) 連線在用戶端驗證期間呼叫 [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature)函式，以處理憑證驗證訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

