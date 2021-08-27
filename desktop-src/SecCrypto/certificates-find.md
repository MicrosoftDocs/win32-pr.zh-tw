---
description: 傳回憑證物件，其中包含符合指定之搜尋準則的所有憑證。
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: ICertificates2：： Find 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100988"
---
# <a name="icertificates2find-method"></a>ICertificates2：： Find 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]

**Find** 方法會傳回包含所有符合指定搜尋準則之憑證的 [**憑證**](certificates.md)物件。 此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FindType* \[在\]
</dt> <dd>

[**CAPICOM \_ 憑證 \_ 尋找 \_ 類型**](capicom-certificate-find-type.md)列舉值，指定 *varCriteria* 參數中提供的相符準則類型。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                        | 意義                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊**</dt> </dl>                              | 傳回具有 SHA1 雜湊的憑證，此雜湊符合在 *varCriteria* 參數中指定的 sha1 雜湊。<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱**</dt> </dl>                     | 傳回主體名稱完全或部分符合 *varCriteria* 參數中指定之主體名稱的憑證。 此呼叫只會搜尋 [主體名稱] 欄位。<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱**</dt> </dl>                        | 傳回其簽發者名稱完全或部分符合 *varCriteria* 參數中所指定之簽發者名稱的憑證。 此呼叫只會搜尋 [簽發者名稱] 欄位。<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱**</dt> </dl>                              | 傳回其根主體名稱完全或部分符合 *varCriteria* 參數中所指定之根主體名稱的憑證。 此呼叫會建立鏈。 此呼叫會搜尋根憑證的 [主體名稱] 欄位。<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱**</dt> </dl>                  | 傳回範本名稱符合 *varCriteria* 參數中所指定範本名稱的憑證。<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組**</dt> </dl>                               | 傳回副檔名符合 *varCriteria* 參數中指定之副檔名的憑證。<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性**</dt> </dl>      | 傳回存放區中的憑證，該憑證明確包含具有 *varCriteria* 參數中所指定之值的擴充屬性。<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則**</dt> </dl>   | 傳回存放區中的憑證，其中具有在 *varCriteria* 參數中指定的增強金鑰使用方法擴充功能、應用程式原則延伸模組或擴充屬性。<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則**</dt> </dl>   | 傳回憑證，其中包含在 *varCriteria* 參數中指定的憑證原則延伸中的原則 OID。<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效**</dt> </dl>                           | 傳回時間有效的憑證。<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效**</dt> </dl> | 傳回時間尚未生效的憑證。<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期**</dt> </dl>                     | 傳回時間已過期的憑證。<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式**</dt> </dl>                              | 傳回憑證，其中包含在 *varCriteria* 參數中指定的 KeyUsage 延伸模組中的金鑰使用方式。 如果 KeyUsage 延伸模組不存在，就會假設所有的金鑰使用方式都無法使用。<br/>                           |



 

</dd> <dt>

*varCriteria* \[在中，選擇性\]
</dt> <dd>

包含搜尋準則的 variant。 這項資料必須符合 *FindType* 參數中指定的資料類型。 如果 *FindType* 參數的值為 capicom \_ 憑證 \_ 尋找 \_ 時間 \_ 有效、capicom \_ 憑證尋找時間 \_ \_ \_ 尚未 \_ \_ 生效，或 capicom \_ 憑證 \_ 找 \_ \_ 出時間已過期，且您未將值傳遞給此參數，則會假設為目前時間。 如需每種資料類型的範例，請參閱備註。 預設值為 0。

</dd> <dt>

*bFindValidOnly* \[在中，選擇性\]
</dt> <dd>

布林值，指出是否只傳回有效的憑證。 預設值為 false;這表示會傳回所有符合搜尋準則的憑證。

若為 true，則搜尋不會傳回下列類型的憑證：

-   其時間已過期或尚未生效的憑證。
-   憑證未正確連結。
-   有簽章問題的憑證。
-   已撤銷的憑證。

</dd> </dl>

## <a name="return-value"></a>傳回值

包含搜尋結果的 [**憑證**](certificates.md)物件。

**CAPICOM 2.1：** 傳回的 [**憑證**](certificates.md) 物件包含對集合中執行搜尋的憑證的參考。 對傳回的 **憑證** 物件中的憑證所做的任何變更，都會反映在該集合中。

**Capicom 2.0、capicom 2.0.0.1、capicom 2.0.0.2 和 capicom 2.0.0.3：** 傳回的 [**憑證**](certificates.md) 物件包含完成搜尋的集合中憑證的複本。 對傳回的 **憑證** 物件中的憑證所做的任何變更都不會反映在該集合中。

## <a name="remarks"></a>備註

下列範例會顯示不同搜尋條件類型的可能搜尋準則。



| *FindType* 參數                              | *varCriteria* 參數                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱         | "NameOfPerson"                                                                                                                     |
| CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱          | 頒發                                                                                                                         |
| CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱            | 「Microsoft 根授權單位」                                                                                                         |
| CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組             | "2.5.29.31"<br/> CAPICOM \_ OID \_ 金鑰 \_ 使用方法 \_ 擴充功能<br/> 「CRL 通訊群組清單」<br/>                           |
| CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性    | CAPICOM \_ PROPID \_ 金鑰 \_ >PROV \_ 資訊                                                                                                   |
| CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則   | 1.3.6.1.5.5.7.3.3<br/> "1.3.6.1.5.5.7.3.4"<br/> CAPICOM \_ OID \_ 伺服器 \_ 驗證 \_ EKU<br/> 「程式碼簽署」<br/> |
| CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則   | "1.3.6.1.5.5.7.3.4.3.5"<br/> 「公司高保證」<br/>                                                           |
| CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效           | \#04/15/2002、6:00 PM\#                                                                                                            |
| CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效 | \#04/15/2002、6:00 PM\#                                                                                                            |
| CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期         | \#04/15/2002、6:00 PM\#                                                                                                            |
| CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式            | CAPICOM \_ \_ 只加密 \_ 金鑰 \_ 使用方式                                                                                                |



 

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
</dt> <dt>

[**CAPICOM \_ OID**](capicom-oid.md)
</dt> </dl>

 

 
