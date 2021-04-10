---
description: 將單一安全通訊端層通訊協定解密 (SSL) 封包。
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: 'SslDecryptPacket 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943925"
---
# <a name="ssldecryptpacket-function"></a>SslDecryptPacket 函式

**SslDecryptPacket** 函式會將單一 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)解密 (SSL) 封包。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

SSL 通訊協定提供者實例的控制碼。

</dd> <dt>

*hKey* \[in、out\]
</dt> <dd>

用來解密封包的金鑰控制碼。

</dd> <dt>

*pbInput* \[在\]
</dt> <dd>

包含要解密之封包的緩衝區指標。

</dd> <dt>

*cbInput* \[在\]
</dt> <dd>

*PbInput* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

要包含解密封包的緩衝區指標。

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

*PbOutput* 緩衝區的長度（位元組）。

</dd> <dt>

*pcbResult* \[擴展\]
</dt> <dd>

寫入 *pbOutput* 緩衝區的位元組數目。

</dd> <dt>

*SequenceNumber* \[在\]
</dt> <dd>

對應至此封包的序號。

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

封包長度可以是零，例如解密 "HelloRequest" 訊息時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

