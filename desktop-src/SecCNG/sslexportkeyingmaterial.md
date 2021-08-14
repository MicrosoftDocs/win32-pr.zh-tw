---
description: 根據 RFC 5705 標準匯出金鑰內容。
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: 'SslExportKeyingMaterial 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 39aaebba64f92794e179af95a5a175e2603fccc40410989cfcd427c6a7a1a88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906616"
---
# <a name="sslexportkeyingmaterial-function"></a>SslExportKeyingMaterial 函式

根據 [RFC 5705 標準](https://tools.ietf.org/html/rfc5705)匯出金鑰內容。 此函式會使用 TLS 的非虛擬亂數函式來產生金鑰內容的位元組緩衝區。 它會參考主要密碼、disambiguating ASCII 標籤、用戶端和伺服器隨機值，以及選擇性的應用程式內容資料。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

TLS 通訊協定提供者實例的控制碼。

</dd> <dt>

*hMasterKey* \[在\]
</dt> <dd>

主要金鑰組象的控制碼，該物件將用來建立已匯出至 br 的金鑰處理內容。

</dd> <dt>

*sLabel* \[在\]
</dt> <dd>

以 NUL 終止的 ASCII 標籤字串。 Schannel 會先移除終止的 NUL 字元，再將它傳遞給虛擬亂數函式。

</dd> <dt>

*pbRandoms* \[在\]
</dt> <dd>

包含 *用戶端 \_ 隨機* 和 *伺服器 \_ 隨機* 值（TLS 連接）串連的緩衝區指標。

</dd> <dt>

*cbRandoms* \[在\]
</dt> <dd>

*PbRandoms* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pbCoNtextValue* \[在中，選擇性\]
</dt> <dd>

包含應用程式內容的緩衝區指標。 如果 *pbCoNtextValue* 為 **Null**，則 *cbCoNtextValue* 必須為零。

</dd> <dt>

*cbCoNtextValue* \[在\]
</dt> <dd>

*PbCoNtextValue* 緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pbOutput* \[擴展\]
</dt> <dd>

接收匯出的金鑰內容的緩衝區位址。 *CbOutput* 參數包含這個緩衝區的大小。 此值不可以是 **Null**。

</dd> <dt>

*cbOutput* \[在\]
</dt> <dd>

*PbOutput* 緩衝區的長度（以位元組為單位）。 必須大於零。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

未使用。 必須設定為零。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




