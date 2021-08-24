---
description: MsiDigitalCertificate 資料表會以二進位資料流程格式儲存憑證，並將每個憑證與主鍵產生關聯。
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: MsiDigitalCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828778"
---
# <a name="msidigitalcertificate-table"></a>MsiDigitalCertificate 資料表

MsiDigitalCertificate 資料表會以二進位資料流程格式儲存憑證，並將每個憑證與主鍵產生關聯。 主要金鑰是用來在多個數位簽署的物件之間共用憑證。 數位憑證是提供驗證身分識別方法的認證。 如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的[密碼](../seccrypto/cryptography-portal.md)編譯一節中的[數位憑證](../seccrypto/digital-certificates.md)。

從 Windows Installer 版本2.0 開始，可以使用[MsiDigitalSignature](msidigitalsignature-table.md)和 MsiDigitalCertificate 資料表。

Windows安裝程式可以使用數位簽章來偵測損毀的資源。 Windows安裝程式版本2.0 只能驗證外部封包的數位簽章，而且只能透過使用[MsiDigitalSignature](msidigitalsignature-table.md)和 MsiDigitalCertificate 資料表。

從 Windows Installer 版本3.0 開始，Windows Installer 可以使用[MsiPatchCertificate](msipatchcertificate-table.md)和 MsiDigitalCertificate 資料表來確認修補程式 () .msp 檔案的數位簽章。 如需詳細資訊，請參閱撰寫安全安裝和[使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)[的指導方針](guidelines-for-authoring-secure-installations.md)。

MsiDigitalCertificate 資料表具有下列資料行。



| Column             | 類型                         | 答案 | Nullable |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [識別碼](identifier.md) | Y   | N        |
| CertData           | [二進位](binary.md)         | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

識別數位簽章證書。 資料表的主鍵。

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

數位憑證的二進位標記法。 CertData 資料行包含憑證內容的編碼位元組陣列。 這是 [**CERT \_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)結構的 **pbCertEncoded** 成員。 您可以藉由呼叫 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)、 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)或匯入 .cer 檔案來取得憑證內容。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[MsiDigitalSignature 資料表](msidigitalsignature-table.md)
</dt> <dt>

[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
