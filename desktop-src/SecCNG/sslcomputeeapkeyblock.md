---
description: 計算可延伸驗證通訊協定所使用的金鑰區塊 (EAP) 。
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: 'SslComputeEapKeyBlock 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988748"
---
# <a name="sslcomputeeapkeyblock-function"></a>SslComputeEapKeyBlock 函式

**SslComputeEapKeyBlock** 函式會計算可延伸驗證通訊協定所使用的金鑰區塊 (EAP) 。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
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

*pbRandoms* \[在\]
</dt> <dd>

緩衝區的指標，其中包含 SSL 會話的用戶端 \_ 隨機和伺服器 \_ 隨機值串連。

</dd> <dt>

*cbRandoms* \[在\]
</dt> <dd>

*PbRandoms* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pbOutput* \[out、optional\]
</dt> <dd>

接收金鑰 BLOB 的緩衝區位址。 *CbOutput* 參數包含這個緩衝區的大小。 如果此參數為 **Null**，此函式會將所需的大小（以位元組為單位）放在 *pcbResult* 參數所指向的 **DWORD** 中。

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

設定為 **NCRYPT \_ SSL \_ 伺服器 \_ 旗** 標，表示這是伺服器呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。



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



 

