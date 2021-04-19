---
description: 將憑證物件儲存在集合中。
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificate. Save 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995083"
---
# <a name="certificatessave-method"></a>Certificate. Save 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]

Save 方法會將 [**憑證**](certificate.md)物件 **儲存** 在集合中。

## <a name="syntax"></a>語法


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
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

字串，其中包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*純文字*](../secgloss/p-gly.md)密碼。 預設值為空字串 ("")。 密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。 如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*SaveAs* \[在中，選擇性\]
</dt> <dd>

指定輸出檔格式之 [**CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型**](capicom-certificates-save-as-type.md) 列舉的值。 預設值為 [ \_ 將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX]。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                          | 意義                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</dt> </dl>                      | 憑證會儲存為 PFX。<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PKCS7**</dt> </dl>                | 憑證會儲存為 PKCS \# 7。<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**\_將 CAPICOM 憑證 \_ 另存為已 \_ \_ 序列化**</dt> </dl> | 憑證會儲存為已序列化。<br/> |



 

</dd> <dt>

*ExportFlag* \[在中，選擇性\]
</dt> <dd>

此為 [**CAPICOM \_ 匯出 \_ 旗**](capicom-export-flag.md) 標列舉值，指定是否忽略任何私用金鑰匯出錯誤。 預設值是 [CAPICOM \_ 匯出 \_ 預設值]。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                                                          | 意義                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**CAPICOM \_ 匯出 \_ 預設值**</dt> </dl>                                                                                                      | 不會忽略私密金鑰匯出錯誤。<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**CAPICOM \_ 匯出 \_ 略 \_ 過 \_ 私密金鑰 \_ 不可 \_ 匯出的 \_ 錯誤**</dt> </dl> | 私密金鑰匯出錯誤會被忽略。<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

您可以使用 [**Store. Load**](store-load.md)方法來取出 [**憑證**](certificate.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificates.md)
</dt> </dl>

 

 
