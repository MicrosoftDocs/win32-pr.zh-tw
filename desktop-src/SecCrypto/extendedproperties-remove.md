---
description: 從集合中移除擴充屬性。
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: ExtendedProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1774ce0fc8b03bed621c58b0f7a9a0f16a7d4156
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976119"
---
# <a name="extendedpropertiesremove-method"></a>ExtendedProperties 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Remove** 方法會移除集合中的擴充屬性。

## <a name="syntax"></a>語法


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*propID* \[在\]
</dt> <dd>

[**CAPICOM \_ PROPID**](capicom-propid.md)列舉的值，可定義要移除之擴充屬性的 CAPICOM 屬性識別碼。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**CAPICOM \_ PROPID \_ 不明**</dt> </dl>                                                                       | 未知的屬性類型。<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ >PROV \_ 控制碼**</dt> </dl>                                             | [*密碼編譯服務提供者*](../secgloss/c-gly.md)中金鑰容器的控制碼 (CSP) 。<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM \_ PROPID \_ 金鑰 \_ >PROV \_ 資訊**</dt> </dl>                                                   | CSP 內金鑰容器的相關資訊。<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SHA1 \_ 雜湊**</dt> </dl>                                                                | SHA1 雜湊物件。<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**CAPICOM \_ PROPID \_ 雜湊 \_**</dt> </dl>                                                                | 雜湊物件的屬性。<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ MD5 \_ 雜湊**</dt> </dl>                                                                   | MD5 雜湊物件。<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**CAPICOM \_ PROPID 索引 \_ 鍵 \_ 內容**</dt> </dl>                                                          | 主要 [*內容*](../secgloss/c-gly.md)。<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**CAPICOM \_ PROPID \_ 金鑰 \_ 規格**</dt> </dl>                                                                   | 索引鍵的規格。<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**已 \_ 保留的 CAPICOM PROPID \_ IE30 \_**</dt> </dl>                                                    | 物件是否保留在 Internet Explorer 3.0 中的相關資訊。<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**已 \_ 保留的 CAPICOM PROPID \_ PUBKEY \_ 雜湊 \_**</dt> </dl>                              | 是否保留公開金鑰雜湊的相關資訊。<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ ENHKEY \_ 使用方式**</dt> </dl>                                                       |  (EKU) 的 [*增強金鑰使用*](../secgloss/e-gly.md) 方法。<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ CTL \_ 使用方式**</dt> </dl>                                                                | [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 使用方式。<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**CAPICOM \_ PROPID \_ 下一個 \_ 更新 \_ 位置**</dt> </dl>                              | [*憑證撤銷清單*](../secgloss/c-gly.md)的下一個更新位置 (CRL) 。<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**CAPICOM \_ PROPID \_ 易記 \_ 名稱**</dt> </dl>                                                    | 人們看得懂的名稱。<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**CAPICOM \_ PROPID \_ PVK \_ 檔**</dt> </dl>                                                                   | 包含私密金鑰的檔案。<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**CAPICOM \_ PROPID \_ 描述**</dt> </dl>                                                           | 人們看得懂的描述。<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**CAPICOM \_ PROPID \_ 存取 \_ 狀態**</dt> </dl>                                                       | 存取的狀態。<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ 簽名 \_ 雜湊**</dt> </dl>                                                 | 簽章的雜湊。<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**CAPICOM \_ PROPID \_ 智慧 \_ 卡 \_ 資料**</dt> </dl>                                             | 智慧卡資料。<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM \_ PROPID \_ EFS**</dt> </dl>                                                                                   | 加密檔案系統 (EFS) 。<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**CAPICOM \_ PROPID \_ FORTEZZA \_ 資料**</dt> </dl>                                                    | 使用「 [*國家/地區」標準和技術*](../secgloss/n-gly.md) 所擁有的密碼編譯通訊協定和演算法所建立的資料 (NIST) 。<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**已封存的 CAPICOM \_ PROPID \_**</dt> </dl>                                                                    | 物件是否已封存的相關資訊。<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**CAPICOM \_ PROPID \_ 金鑰 \_ 識別碼**</dt> </dl>                                                 | 金鑰識別碼。<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**CAPICOM \_ PROPID \_ 自動 \_ 註冊**</dt> </dl>                                                          | 憑證的自動註冊資訊。<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ 段落**</dt> </dl>                                             | 公開金鑰演算法的參數。<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**CAPICOM \_ PROPID \_ 跨 \_ CERT \_ DIST \_ 點**</dt> </dl>                       | 用來更新動態交叉憑證的資訊。<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ 簽發 \_ 者 \_ 公開金鑰 \_ MD5 \_ 雜湊**</dt> </dl>          | 簽發者之公開金鑰的 MD5 雜湊。<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ 主體 \_ 公開金鑰 \_ \_ MD5 \_ 雜湊**</dt> </dl>       | 主體公開金鑰的 MD5 雜湊。<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**CAPICOM \_ PROPID \_ 註冊**</dt> </dl>                                                              | 憑證註冊的相關資訊。<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**CAPICOM \_ PROPID \_ 日期 \_ 戳記**</dt> </dl>                                                             | 日期戳記。<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ 簽發 \_ 者 \_ 序號 \_ MD5 \_ 雜湊**</dt> </dl> | 簽發者序號的 MD5 雜湊。<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ 主體 \_ 名稱 \_ MD5 \_ 雜湊**</dt> </dl>                          | 主體名稱的 MD5 雜湊。<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**CAPICOM \_ PROPID \_ 延伸 \_ 錯誤 \_ 資訊**</dt> </dl>                                 | 有關錯誤的延伸資訊。<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**CAPICOM \_ PROPID \_ 續約**</dt> </dl>                                                                       | [*憑證授權單位*](../secgloss/c-gly.md)單位更新的相關資訊。<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**CAPICOM \_ PROPID 封存的 \_ \_ 金鑰 \_ 雜湊**</dt> </dl>                                       | 金鑰的封存雜湊。<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**\_ \_ 先保留 CAPICOM \_ PROPID**</dt> </dl>                                                 | 第一個保留的相關資訊。<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**\_ \_ 上次 \_ 保留的 CAPICOM PROPID**</dt> </dl>                                                    | 最新保留的相關資訊。<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ 第一位 \_ 使用者**</dt> </dl>                                                             | 第一個使用者的相關資訊。<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ 上次 \_ 使用者**</dt> </dl>                                                                | 最新使用者的相關資訊。<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
