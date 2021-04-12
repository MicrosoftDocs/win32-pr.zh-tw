---
description: 從指定的憑證存放區尋找符合指定主體憑證的簽發者憑證。
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192941"
---
# <a name="wthelpercertfindissuercertificate-function"></a>WTHelperCertFindIssuerCertificate 函式

\[**WTHelperCertFindIssuerCertificate** 函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

**WTHelperCertFindIssuerCertificate** 函式會從指定的憑證存放區尋找符合指定主體憑證的簽發者憑證。

> [!Note]  
> 此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Wintrust.dll。

 

## <a name="syntax"></a>語法


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pChildCoNtext* \[在\]
</dt> <dd>

要尋找相符簽發者憑證的主體憑證。

</dd> <dt>

*chStores* \[在\]
</dt> <dd>

*PahStores* 陣列中的元素數目。

</dd> <dt>

*pahStores* \[在\]
</dt> <dd>

要在其中搜尋的憑證存放區陣列。

</dd> <dt>

*psftVerifyAsOf* \[在\]
</dt> <dd>

驗證的時間。

</dd> <dt>

*dwEncoding* \[在\]
</dt> <dd>

**DWORD** 值，指定要檢查之憑證的編碼類型。 如需可能編碼類型的詳細資訊，請參閱 [憑證和訊息編碼類型](certificate-and-message-encoding-types.md)。

</dd> <dt>

*pdwConfidence* \[out、optional\]
</dt> <dd>

這個參數可以是零或多個下列信賴值的位元組合。



| 值                                                                                                                                                                                                                                                                 | 意義                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**CERT \_信心 \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | 憑證的簽章有效。<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**CERT \_信賴 \_ 時間**</dt> <dt> 0x01000000</dt> </dl>                  | 憑證簽發者的時間有效。<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERT \_ 信賴 \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | 憑證的有效時間。<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERT \_ 信賴 \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | 授權單位識別碼延伸有效。<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **CERT \_ 信賴 \_ 度**</dt> <dt>0x00001000</dt> </dl>       | 憑證與授權單位識別碼延伸的簽章至少為有效。<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERT \_ 信賴度 \_ 最高**</dt> <dt>0x11111000</dt> </dl>       | 所有其他信賴值的組合。<br/>                                 |



 

</dd> <dt>

*dwError* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標，其中包含此憑證的錯誤值（如果適用）。

</dd> </dl>

## <a name="return-value"></a>傳回值

符合 *pChildCoNtext* 參數所指定之主體憑證的簽發者憑證。

## <a name="remarks"></a>備註

若要成功找到相符的簽發者憑證，必須符合下列需求：

-   *PChildCoNtext* 參數所指定的主體憑證簽章必須是有效的。
-   *PChildCoNtext* 參數之 **PCertInfo** 成員的 **rgExtension** 成員必須包含 [**CERT \_ 授權單位 \_ 金鑰 \_ 識別碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)結構。 此結構的 **CertIssuer** 和 **CertSerialMember** 成員非常符合簽發者憑證的對應成員。
-   *PsftVerifyAsOf* 參數的值必須在主體憑證的有效期間內。
-   主體憑證的有效期間必須在簽發者憑證的有效期間內。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
