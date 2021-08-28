---
description: MsiDigitalSignature 資料表包含安裝資料庫中每個數位簽署物件的簽章資訊。
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: MsiDigitalSignature 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18514747e5bb99f03bacc792f9a9ec311e28006b837061ce96088c3b723bf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679787"
---
# <a name="msidigitalsignature-table"></a>MsiDigitalSignature 資料表

MsiDigitalSignature 資料表包含安裝資料庫中每個數位簽署物件的簽章資訊。

從 Windows Installer 版本2.0 開始，可以使用 MsiDigitalSignature 和[MsiDigitalCertificate](msidigitalcertificate-table.md)資料表。

Windows安裝程式版本可以使用數位簽章來偵測損毀的資源。 Windows安裝程式2.0 只能驗證外部封包的數位簽章，而且只會使用 MsiDigitalSignature 和[MsiDigitalCertificate](msidigitalcertificate-table.md)資料表。

從 Windows Installer 3.0 開始，Windows Installer 可以使用[MsiPatchCertificate](msipatchcertificate-table.md)和 MsiDigitalCertificate 資料表來確認修補程式 () .msp 檔案的數位簽章。 如需詳細資訊，請參閱撰寫安全安裝和[使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)[的指導方針](guidelines-for-authoring-secure-installations.md)。

MsiDigitalSignature 資料表具有下列資料行。



| Column               | 類型                         | 答案 | Nullable |
|----------------------|------------------------------|-----|----------|
| 資料表                | [識別碼](identifier.md) | Y   | N        |
| SignObject           | [Text](text.md)             | Y   | N        |
| DigitalCertificate\_ | [識別碼](identifier.md) | N   | N        |
| 雜湊                 | [二進位](binary.md)         | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

使用 Windows Installer 版本2.0 時，此欄位中的專案必須是[媒體資料表](media-table.md)的「媒體」。 安裝程式只會驗證外部封包媒體專案的數位簽章。 此資料行和 SignObject 資料行會一起指定經過數位簽署的資源。

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

資料表資料行所指定之資料表主鍵的外鍵。 此資料行和資料表資料行會一起指定經過數位簽署的資源。

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)中的外鍵。 這會識別檔案上必須存在的憑證，才能讓相關聯的動作成功。 資源 (或物件) 一律需要符合 MsiDigitalCertificate 資料表中的這個憑證。

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>散 列
</dt> <dd>

在此欄位中，輸入資源 (或物件) 的參考雜湊，以針對資源 (或在執行時間取得的物件) 的實際雜湊進行檢查。 如果只有憑證需要驗證，則雜湊欄位可能是 null。 請注意，雜湊的格式取決於資源 (類型或簽署的物件) 。

雜湊資料行包含雜湊的二進位標記法。 實際的內容是 [**CRYPT \_ 雜湊 \_ Blob**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob)結構的 **>pbdata** 成員，這是 **CRYPTOAPI \_ blob** 結構的一部分。 這可透過呼叫 [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) 或 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)來取得。

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

[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)
</dt> <dt>

[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
