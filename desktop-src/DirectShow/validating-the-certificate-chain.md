---
description: 驗證憑證鏈
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: 驗證憑證鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a1dd3a09e46199cb537c1ac4b17cb96ed0edc2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884036"
---
# <a name="validating-the-certificate-chain"></a>驗證憑證鏈

本主題說明使用認證輸出保護通訊協定 (COPP) 時，如何驗證驅動程式的憑證鏈。

圖形驅動程式的憑證鏈是一份 XML 檔。 憑證鏈包含三個憑證。 第一個憑證稱為分 *葉憑證*，而是驅動程式的 COPP 憑證。 下一個憑證是獨立硬體廠商 (IHV) 的簽署憑證。 最後一個憑證是 Microsoft 的簽署憑證。 若要確定圖形驅動程式是合法的 COPP 裝置，應用程式必須驗證上述三個憑證。 如果應用程式未正確驗證鏈中的憑證，惡意程式可能會導致 COPP 無法運作。

COPP 憑證連結使用 UTF-8 字元集。 憑證中的二進位資料，例如 RSA 公開金鑰，會以位元組由大到小的順序，以 base64 編碼和儲存。  (位元組由 *大* 到小表示最重要的位元組會儲存在最低位址的記憶體位置。 ) 

憑證內的某些元素包含布林值，表示憑證的功能存在。 如果功能存在，對應的子項目值會設定為1。 如果功能不存在，憑證中就不會出現該子項目。

### <a name="xml-element-definitions"></a>XML 元素定義

以下是憑證架構中的元素定義：

-   **CertificateCollection**。 XML 檔的根項目。 它包含憑證元素，鏈中的每個憑證各一個。
-   **憑證**。 包含一個憑證。 這個元素包含資料和簽章元素。
-   **資料**。 包含憑證的相關資訊。 尤其是，它包含憑證的公開金鑰和類型。 資料元素包含下列子項目：
    -   **PublicKey**。 包含憑證的 RSA 公開金鑰。 PublicKey 元素包含 KeyValue 元素，其中包含 Rsakeyvalue> 元素。 Rsakeyvalue> 專案有兩個子項目：模數和指數，而這些專案定義了公開金鑰。 模數和指數元素是以 base64 編碼，並以位元組由大到小的順序儲存。
    -   **KeyUsage**。 如果憑證是驅動程式的 COPP 憑證，此元素應該會包含名為 EncryptKey 的子項目。 如果憑證是 IHV 的簽署憑證或 Microsoft 的簽署憑證，它應該會包含名為 SignCertificate 的子項目。 這兩個子項目都包含布林值。
    -   **SecurityLevel**。 應忽略這個元素。
    -   **ManufacturerData**。 指定圖形裝置的製造商和型號。 此元素僅供參考。
    -   **Features**。 包含指定憑證使用方式的子項目。 與 COPP 相關的唯一一個是 COPPCertificate 元素。 可能存在其他子項目;如果是，則應該予以忽略。 如果 COPPCertificate 元素存在，則憑證是 COPP 憑證。 此元素必須存在於有效 COPP 憑證的分葉節點中。 這個元素包含布林值。
-   簽 **章。** 包含此憑證的簽章。 它包含下列子項目：
    -   **SignedInfo**。 包含簽章的相關資訊。 這個元素的重要子項目是 DigestValue 元素，其中包含資料元素上的 SHA-1 雜湊的 base64 編碼值。 針對 (CRL) 的憑證撤銷清單檢查憑證時，會使用摘要值。
    -   **SignatureValue**。 此值是透過資料元素計算，並根據 Public-Key 加密標準中定義的 RSASSA-PKCS-PSS 數位簽章配置 (PKCS) \# 1 (2.1 版) 來計算。 如需 PKCS 1 的相關資訊 \# ，請造訪 [https://www.rsa.com/](https://www.rsa.com/) 。
    -   **KeyInfo**。 包含鏈中下一個憑證的 RSA 公開金鑰。 此元素用來驗證資料元素中的資料是否未遭篡改。 這個元素的格式與 PublicKey 元素相同。

### <a name="certificate-validation"></a>憑證驗證

應用程式必須執行下列步驟，才能正確地驗證憑證鏈。 如果任何步驟失敗，或這些程式中參考的任何專案不存在，驗證就會失敗。

### <a name="validate-certificate-collection-procedure"></a>驗證憑證收集程式

若要驗證憑證鏈，請執行下列步驟：

1.  確認 CertificateCollection 是格式正確的 XML。
2.  確認 CertificateCollection 是以 UTF-8 格式編碼。
3.  檢查 CertificateCollection 元素中的 Version 屬性是2.0 或更新版本。
4.  確認憑證鏈只包含三個憑證元素。
5.  迴圈執行憑證鏈中的每個憑證元素，並在每個專案上執行驗證憑證程式（如下所述）。

### <a name="validate-certificate-procedure"></a>驗證憑證程式

若要驗證鏈中的憑證，請執行下列步驟：

1.  確認資料元素中的子項目都不會重複。 例如，應該只有一個 PublicKey 元素。
2.  請確定 Data/PublicKey/KeyValue/Rsakeyvalue>/模數元素存在。 Base64 解碼值的長度必須為256個位元組（除了根目錄以外的所有憑證）。 在根憑證中，此元素的長度必須是128個位元組。
3.  請確定 Data/PublicKey/KeyValue/Rsakeyvalue>/指數元素存在。 Base64 解碼的值不得超過4個位元組。
4.  如果此憑證是分葉憑證，請確認下列事項：
    -   KeyUsage 元素包含值為1的 EncryptKey 元素。
    -   Features 元素包含值為1的 COPPCertificate 元素。
5.  如果此憑證不是分葉憑證，請確認下列事項：
    -   Data/PublicKey 元素的模數和指數完全符合先前憑證之 Signature/KeyInfo 元素中的模數和指數。
    -   KeyUsage 元素包含 SignCertificate 元素，其值為1。
6.  使用 SHA-1 雜湊演算法來雜湊憑證的資料元素中的每個位元組。 從資料標記中第一個字元到結尾/Data sources 標記中之最後一個字元的每個位元組 &lt; &gt; &lt; &gt; 都應該進行雜湊處理。 雜湊值是用來根據憑證撤銷清單來檢查憑證 (CRL) ，如[憑證撤銷清單](certificate-revocation-lists.md)中所述
7.  將步驟6中的雜湊值與 Signature/SignedInfo/Reference/DigestValue 元素的 base64 解碼值進行比較。 這些值必須相符。
8.  執行驗證簽章程式，如下所述。
9.  如果此憑證不是鏈中的最終憑證，請在迴圈的下一個反覆運算中儲存 Signature/KeyInfo/KeyValue/Rsakeyvalue> 值。
10. 如果此憑證是鏈中的最終憑證，請確定 Signature/KeyInfo/KeyValue/Rsakeyvalue> 的值符合 Microsoft 的公開金鑰。 Microsoft 公開金鑰具有下列 base64 編碼值：
    -   模：

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   指數： `AQAB`

### <a name="verify-signature-procedure"></a>驗證簽章程式

SignatureValue 元素的值會根據 PKCS 1 2.1 版中定義的 RSASSA-PKCS-PSS 數位簽章配置來計算， \# (以下稱為 pkcs) 。 若要驗證此簽章，請執行下列步驟：

1.  解碼 Signature/KeyInfo/KeyValue/Rsakeyvalue> 元素中的模數和指數值。 這些值會定義簽署憑證的 RSA 公開金鑰。
2.  解碼 Signature/SignatureValue 元素。
3.  計算 RSASSA-PKCS-PSS-驗證作業，定義于 PKCS 的區段8.1.2 中。

針對 RSASSA-PKCS-PSS-驗證作業，請使用下列輸入：

-    (*n*，*e*) 是步驟1中的公開金鑰。
-   *M* 是資料元素中的所有位元組，包括 &lt; &gt; &lt; &gt; 用來括住元素的資料和/data sources 標記。
-   *S* 是步驟2中已解碼的簽章值。

RSASSA-PKCS-PSS-驗證作業會使用 EMSA-PSS 編碼作業，定義于區段9.1.1 中。 的 PKCS。 針對這項作業，COPP 會使用下列選項：

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (mask 產生函數) = 及 MGF1
-   *sLen* = 0

遮罩產生函式及 MGF1 是定義在 PKCS 的附錄 B. 2 中。 針對此功能，COPP 會使用下列選項：

-   Hash = SHA-1
-   *hLen* = 20

RSASSA-PKCS-PSS-驗證作業的輸出會指出簽章是否有效或無效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



