---
description: 產生一組安全通訊端層的通訊協定 (SSL) 工作階段金鑰。
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: 'SslGenerateSessionKeys 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3a9d7a25e5dd2035bd0b060ae11904e351489309b3a5e3c65c0e1582dce77500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906170"
---
# <a name="sslgeneratesessionkeys-function"></a>SslGenerateSessionKeys 函式

**SslGenerateSessionKeys** 函式會產生一組 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 工作階段金鑰。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
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

*phReadKey* \[擴展\]
</dt> <dd>

傳回之讀取按鍵控制碼的指標。

</dd> <dt>

*phWriteKey* \[擴展\]
</dt> <dd>

傳回之寫入按鍵控制碼的指標。

</dd> <dt>

*pParameterList* \[在\]
</dt> <dd>

[**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx)緩衝區陣列的指標，其中包含用來做為金鑰交換作業一部分的資訊。 確切的緩衝區集取決於所使用的通訊協定和加密套件。 清單最少會包含緩衝區，其中包含用戶端和伺服器提供的隨機值。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | 描述                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | 其中一個提供的控制碼無效。<br/>                     |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhReadKey* 或 *phWriteKey* 參數為 null。<br/>            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

