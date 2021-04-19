---
description: 設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。 這是預設屬性。
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: IEKU：： Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987879"
---
# <a name="iekuname-property"></a>IEKU：： Name 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**Name** 屬性會設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。 這是預設屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>屬性值

指定 EKU 之 CAPICOM 名稱的 [**CAPICOM \_ EKU**](capicom-eku.md) 列舉值。 下表顯示可能的值。



| 值                                                                                                                                                                                                                           | 意義                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**CAPICOM \_ EKU \_ 其他**</dt> </dl>                                                      | 憑證具有在本機原則中定義的使用方式。 如果需要的 EKU 未預先定義，而且應用程式必須設定 OID 值，就會使用這個方法。<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ 伺服器 \_ 驗證**</dt> </dl>                                   | 憑證可以用來驗證服務器。<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ 用戶端 \_ 驗證**</dt> </dl>                                   | 憑證可以用來驗證用戶端。<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**CAPICOM \_ EKU 程式 \_ 代碼 \_ 簽署**</dt> </dl>                                | 憑證可以用來建立數位簽章。<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**CAPICOM \_ EKU \_ 電子郵件 \_ 保護**</dt> </dl>                    | 憑證可用於電子郵件保護。<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**CAPICOM \_ EKU \_ 智慧卡 \_ 登入**</dt> </dl>                       | 憑證可用於智慧卡登入。 在 CAPICOM 2.0 中引進。<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**CAPICOM \_ EKU \_ 加密 \_ 檔 \_ 系統**</dt> </dl> | 憑證可用於 EFS。 在 CAPICOM 2.0 中引進。<br/>                                                                                      |



 

## <a name="remarks"></a>備註

當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
