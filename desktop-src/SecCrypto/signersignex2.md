---
description: 簽署和時間戳記指定的檔案，允許多個嵌套的簽章。
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194362"
---
# <a name="signersignex2-function"></a>SignerSignEx2 函式

**SignerSignEx2** 函式會簽署指定的檔案，並為其加上時間戳記，以允許多個嵌套簽章。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

修改此函式的行為。

如果要簽署的檔案是可移植的可執行檔 (PE) 檔，這可以是零或一或多個下列值的組合。



| 值                                                                                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_專有 \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x10</dt> </dl>                    | 建立 PE 檔案的 SIP 間接資料時，請排除頁面雜湊。 此旗標優先于 **SPC \_ Inc. \_ PE \_ 頁面 \_ 雜湊 \_ 旗** 標旗標。<br/> 如果未指定 **spc \_ 專有 \_ PE \_ page \_ 雜湊 \_ 旗** 標或 **spc \_ inc. \_ pe \_ Page \_ 雜湊 \_** 旗標旗標，則會使用 [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) 函數所設定的值來進行此設定。 這項設定的預設值是在建立 PE 檔案的 SIP 間接資料時排除頁面雜湊。<br/> 此值定義于 Mssip .h 標頭檔中。<br/> **Windows Server 2003 和 WINDOWS XP：** 不支援這個值。<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_INC. \_ PE 匯 \_ 入 \_ 位址 \_ 表 \_ 旗**</dt>標 <dt>0x20</dt> </dl> | 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_INC \_ PE \_ DEBUG \_ INFO \_ 旗**</dt>標 <dt>0x40</dt> </dl>                       | 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_INC. \_ PE \_ 資源 \_ 旗**</dt>標 <dt>0x80</dt> </dl>                           | 不支援這個值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_INC \_ PE \_ 頁面 \_ 雜湊 \_ 旗**</dt>標 <dt>0x100</dt> </dl>                   | 建立 PE 檔案的 SIP 間接資料時包含頁面雜湊。<br/> **Windows Server 2003 和 WINDOWS XP：** 不支援這個值。<br/> 此值定義于 Mssip .h 標頭檔中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_附加**</dt> <dt>0x1000</dt> </dl>                                                                         | 簽章將會被嵌套。 如果您在新增任何簽章之前設定此旗標，則會將產生的簽章新增為外部簽章。 如果您未設定此旗標，則產生的簽章會取代外部簽章，並刪除所有的內部簽章。<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pSubjectInfo* \[在\]
</dt> <dd>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的指標，此結構會指定要簽署的主旨。

</dd> <dt>

*pSignerCert* \[在\]
</dt> <dd>

[**簽署者 \_**](signer-cert.md)憑證結構的指標，此結構會指定要用來建立數位簽章的憑證。

</dd> <dt>

*pSignatureInfo* \[在\]
</dt> <dd>

簽署者簽章 [**\_ \_ 資訊**](signer-signature-info.md) 結構的指標，其中包含數位簽章的相關資訊。

</dd> <dt>

*pProviderInfo* \[在中，選擇性\]
</dt> <dd>

[**簽署者提供者 \_ \_ 資訊**](signer-provider-info.md)結構的指標，此結構會指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的私密金鑰資訊。

如果此參數的值為 **Null**，則 *pSignerCert* 參數必須指定與 CSP 相關聯的憑證。

</dd> <dt>

*dwTimestampFlags* \[在中，選擇性\]
</dt> <dd>

如果 *pwszHttpTimeStamp* 參數不是 **Null**，則會傳遞至 [**SignerTimeStampEx3**](signertimestampex3.md)的旗標。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                          | 意義                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**簽署者 \_ 時間戳記 \_ AUTHENTICODE**</dt> </dl> | 預設值。 指定 Authenticode 時間戳記。<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**簽署人 \_ 時間戳記 \_ RFC3161**</dt> </dl>                | 指定 RFC 3161 時間戳記。<br/>                    |



 

如果 *pwszHttpTimeStamp* 參數為 **Null**，則會忽略這個參數。

</dd> <dt>

*pszTimestampAlgorithmOid* \[在中，選擇性\]
</dt> <dd>

要用於建立 RFC 3161 時間戳記之演算法的物件識別碼。 Authenticode 時間戳記會忽略此參數。

</dd> <dt>

*pwszHttpTimeStamp* \[在中，選擇性\]
</dt> <dd>

時間戳記伺服器的 URL。

</dd> <dt>

*psRequest* \[在中，選擇性\]
</dt> <dd>

加入至簽署要求之 [**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) 結構陣列的指標。 如果 *pwszHttpTimeStamp* 參數不包含有效的值或為 **Null**，則會忽略這個參數。

</dd> <dt>

*pSipData* \[在中，選擇性\]
</dt> <dd>

以其他資料形式傳遞至 SIP 函數的32位值。 此的格式和內容是由 SIP 提供者定義。

</dd> <dt>

*ppSignerCoNtext* \[擴展\]
</dt> <dd>

包含已簽署 [*BLOB*](../secgloss/b-gly.md)之 [**簽署者 \_ 內容**](signer-context.md)結構的指標位址。 當您完成使用 **簽署者 \_ 內容** 結構時，請藉由呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md)函數來釋出 **簽署者 \_ 內容** 結構。

</dd> <dt>

*pCryptoPolicy* \[在中，選擇性\]
</dt> <dd>

如果存在，則為憑證 [**強式 \_ \_ 簽署 \_ 段落**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) 結構的指標，其中包含用來檢查強式簽章的參數。 如果憑證或其鏈未通過，則不會以任何方式更改檔案。 如果傳入 URL 以指定時間戳記授權單位 (TSA) ，此原則也會套用至時間戳記。

</dd> <dt>

*保存* 
</dt> <dd>

保留的。 這個值必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 此函式所傳回的可能錯誤碼包括（但不限於）下列程式碼。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。



| 傳回碼                                                                                  | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 如果您將 *dwTimestampFlags* 參數設定為「 **簽署 \_ 時間戳記 \_ AUTHENTICODE**」，則無法將 *dwFlags* 參數設定為「 **SIG \_ 附加**」。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerCoNtext**](signerfreesignercontext.md)
</dt> </dl>

 

 
