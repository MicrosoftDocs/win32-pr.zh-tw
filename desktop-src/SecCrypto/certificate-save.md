---
description: 將憑證儲存至檔案。
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: ICertificate2：： Save 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983004"
---
# <a name="icertificate2save-method"></a>ICertificate2：： Save 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

Save 方法會將憑證 **儲存** 至檔案。 此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

字串，其中包含將儲存憑證的輸出檔名稱。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

字串，其中包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*純文字*](../secgloss/p-gly.md)密碼。 密碼最多可包含32個 Unicode 字元，包括結束的 null 字元。 如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*SaveAs* \[在中，選擇性\]
</dt> <dd>

指定輸出檔格式之 [**CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型**](capicom-certificate-save-as-type.md) 列舉的值。 預設值為 **[ \_ 將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER**]。 下表顯示可能的值。



| 值                                                                                                                                                                                                                  | 意義                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER**</dt> </dl> | 輸出檔案會格式化為不儲存私密金鑰的 .cer 檔案。<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</dt> </dl> | 輸出檔將格式化為 .pfx (PKCS \# 12) 檔案，而且任何可匯出的相關私密金鑰也會儲存。<br/> |



 

</dd> <dt>

*IncludeOption* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 憑證 \_ 包含 \_ 選項**](capicom-certificate-include-option.md)列舉值，這個值會指定要將鏈中的憑證儲存到輸出檔的數量。 預設值為 [ \_ \_ 僅限 CAPICOM 憑證包含 \_ 結束實體] \_ \_ 。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                             | 意義                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈**</dt> </dl> | 將所有憑證儲存在鏈中，但根實體除外<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**</dt> </dl>                    | 儲存完整的憑證鏈<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**</dt> </dl>       | 只儲存終端實體憑證<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
