---
description: 代表另一位使用者建立 CMC 憑證要求，並在證書階層中註冊使用者。
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511989"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

EnrollEOBOCMC 範例會代表另一個使用者建立 CMC 憑證要求，並在憑證階層中註冊使用者。 代表其他使用者註冊需要使用註冊代理程式憑證來簽署憑證要求。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollEOBOCMC 資料夾中。

## <a name="discussion"></a>討論

EnrollEOBOCMC 範例：

1.  處理下列命令列引數：
    -   憑證範本的名稱。
    -   要求憑證的使用者名稱。
    -   要儲存要求的個人資訊交換名稱 (PFX) 檔。
    -   用於 PFX 檔案的密碼。
    -   選用的註冊代理程式範本名稱。 如果憑證存放區中沒有註冊代理程式憑證，則會使用此範本來建立註冊代理程式憑證。
2.  建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用命令列上指定的憑證範本將它初始化。
3.  將要求者的名稱加入 CMC request 物件。
4.  抓取現有的註冊代理程式憑證，如果找不到，則會從命令列上指定的註冊代理程式範本建立憑證要求，並嘗試進行註冊。
5.  確認包含註冊代理程式憑證的憑證鏈。
6.  建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，使用註冊代理程式憑證將它初始化、從 CMC request 物件抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合，並將註冊代理程式簽署憑證物件新增至集合。 下一個步驟中所討論的 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件會使用憑證來簽署 CMC 要求。
7.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件、使用 CMC 要求進行初始化、嘗試註冊，以及檢查註冊程式的進度。
8.  將已安裝的憑證匯出至 PFX 檔案。 使用命令列上指定的密碼來保護檔案。 EncodeToFileW 函式定義于 enrollCommon .cpp 中。
9.  從憑證存放區刪除憑證。 下列程式碼範例中使用的函式可以在 CryptoAPI 檔中找到。
10. 從電腦刪除私密金鑰。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC EOBO 要求](cmc-eobo-request.md)
</dt> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



