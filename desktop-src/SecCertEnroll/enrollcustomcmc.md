---
description: 建立 CMC 憑證要求，並在憑證階層中註冊電腦。
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799cd70d8f3b70ae32a95b7720a879ddd611fba5e35064d1794d39bdcd7ab9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780057"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

EnrollCustomCMC 範例會建立 CMC 憑證要求，並在憑證階層中註冊電腦。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomCMC 資料夾中安裝範例。

## <a name="discussion"></a>討論

EnrollCustomCMC 範例：

1.  處理下列命令列引數：
    -   要加入至憑證要求的自訂名稱/值組。
    -   替代主體名稱。
    -   針對增強金鑰使用方法 (OID) 的物件識別碼 (EKU) 延伸模組。
2.  建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 要求物件，並使用電腦內容將它初始化。
3.  使用 PKCS \# 10 要求初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。
4.  使用命令列上指定的 OID 來建立 [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) 物件，並將它新增至 CMC 要求的擴充集合。
5.  使用命令列上指定的名稱建立 [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) 物件，並將它加入至 [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) 集合，使用集合初始化 [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) 延伸模組，並將其新增至 CMC 要求的擴充集合。
6.  使用命令列上指定的名稱和值建立 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件，並將它新增至 CMC 要求的 [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) 集合中。
7.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 CMC 要求物件將它初始化，並抓取包含 base64 編碼要求的字串。
8.  建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。
9.  建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。
10. 檢查提交狀態，並在成功時將憑證安裝至憑證存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 
