---
description: 傳回交握雜湊的控制碼。
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: 'SslHashHandshake 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906096"
---
# <a name="sslhashhandshake-function"></a>SslHashHandshake 函式

**SslHashHandshake** 函式會傳回交握雜湊的控制碼。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。

</dd> <dt>

*hHandshakeHash* \[in、out\]
</dt> <dd>

雜湊物件的控制碼。

</dd> <dt>

*pbInput* \[擴展\]
</dt> <dd>

包含要雜湊之資料的緩衝區位址。

</dd> <dt>

*cbInput* \[在\]
</dt> <dd>

*PbInput* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

## <a name="remarks"></a>備註

**SslHashHandshake** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。

1.  呼叫 [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) 函數來取得雜湊控制碼。
2.  **SslHashHandshake** 函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。
3.  使用雜湊控制碼呼叫 [**SslComputeFinishedHash**](sslcomputefinishedhash.md) 函數，以取得雜湊資料的摘要。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

