---
description: 設定或抓取憑證的有效性檢查旗標。
ms.assetid: c80c95a0-8a9b-441d-b243-7ee0552731e4
title: CertificateStatus. CheckFlag 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CheckFlag
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1c47d7f1c59ecd629db1d6fc735f61b8d1fe59c864ffa8a5a9f013c86bd30faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877448"
---
# <a name="certificatestatuscheckflag-property"></a>CertificateStatus. CheckFlag 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**CheckFlag** 屬性會設定或抓取憑證的有效性檢查旗標。

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CheckFlag As CAPICOM_CHECK_FLAG
```



## <a name="property-value"></a>屬性值

可描述憑證有效性檢查之 [**CAPICOM \_ 檢查 \_ 旗**](capicom-check-flag.md) 標列舉的值。 預設值為 [ **\_ \_ \_ 全部線上的 CAPICOM 檢查**]。

**CAPICOM 2.0.0.3/2.0.0.2/2.0.0.1：** 預設值為 [**capicom \_ 檢查簽 \_ 章 \_ 有效性**](capicom-check-flag.md)、 [**capicom \_ 檢查 \_ 時間 \_ 有效性**](capicom-check-flag.md)、 [**capicom \_ 檢查 \_ 受信任的 \_ 根**](capicom-check-flag.md)，以及 [**capicom \_ 檢查 \_ 完成 \_ 鏈**](capicom-check-flag.md)。

**CAPICOM 2.0 及更早版本：** 預設值為 [**capicom \_ 檢查簽 \_ 章 \_ 有效性**](capicom-check-flag.md)、 [**Capicom \_ 檢查 \_ 時間 \_ 有效性**](capicom-check-flag.md)，以及 [**capicom \_ 檢查 \_ 信任的 \_ 根**](capicom-check-flag.md)。

下表顯示可能的值。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CHECK_BASIC_CONSTRAINTS"></span><span id="capicom_check_basic_constraints"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 基本 \_ 條件約束**</dt> </dl>                          | 檢查基本條件約束。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_CHECK_COMPLETE_CHAIN"></span><span id="capicom_check_complete_chain"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 完成 \_ 鏈**</dt> </dl>                                   | 檢查整個鏈。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_CHECK_NAME_CONSTRAINTS"></span><span id="capicom_check_name_constraints"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 名稱 \_ 條件約束**</dt> </dl>                             | 檢查名稱條件約束。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_CHECK_NESTED_VALIDITY_PERIOD"></span><span id="capicom_check_nested_validity_period"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 嵌套 \_ 有效 \_ 期間**</dt> </dl>          | 檢查嵌套有效性。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_CHECK_NONE"></span><span id="capicom_check_none"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 無**</dt> </dl>                                                                  | 未完成任何有效性檢查。<br/>                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_OFFLINE_ALL"></span><span id="capicom_check_offline_all"></span><dl> <dt>**所有的 CAPICOM \_ 檢查 \_ \_ 全部離線**</dt> </dl>                                            | 全離線檢查。 撤銷檢查會對鏈中的所有憑證執行，但根憑證除外。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_CHECK_ONLINE_ALL"></span><span id="capicom_check_online_all"></span><dl> <dt>**\_ \_ 全部線上的 CAPICOM 檢查 \_**</dt> </dl>                                               | 全部線上檢查。 撤銷檢查會對鏈中的所有憑證執行，但根憑證除外。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                                                                         |
| <span id="CAPICOM_CHECK_OFFLINE_REVOCATION_STATUS"></span><span id="capicom_check_offline_revocation_status"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 離線 \_ 撤銷 \_ 狀態**</dt> </dl> | 只使用離線 Crl 來檢查鏈中所有憑證的撤銷狀態。<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_CHECK_ONLINE_REVOCATION_STATUS"></span><span id="capicom_check_online_revocation_status"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 線上 \_ 撤銷 \_ 狀態**</dt> </dl>    | 使用可在線上取得的 Crl，檢查鏈中所有憑證的撤銷狀態。 您可以使用憑證中的 CDP 延伸來下載 Crl。<br/> 如果 CRL 已下載且尚未過期，則 CAPICOM 會使用它，而不會上線。<br/> 如果 CRL 尚未下載或已過期，則 CAPICOM 會上線以嘗試下載 CRL。<br/> |
| <span id="CAPICOM_CHECK_SIGNATURE_VALIDITY"></span><span id="capicom_check_signature_validity"></span><dl> <dt>**CAPICOM \_ 檢查簽章 \_ \_ 有效性**</dt> </dl>                       | 檢查鏈中所有憑證的有效簽章。<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="CAPICOM_CHECK_TIME_VALIDITY"></span><span id="capicom_check_time_validity"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 時間 \_ 有效性**</dt> </dl>                                      | 檢查鏈中所有憑證的時間有效性。<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_CHECK_TRUSTED_ROOT"></span><span id="capicom_check_trusted_root"></span><dl> <dt>**CAPICOM \_ 檢查 \_ 信任的 \_ 根目錄**</dt> </dl>                                         | 檢查憑證鏈的根信任。<br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
