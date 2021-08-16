---
description: 初始化 PKCS \# 10 憑證要求物件、將它包裝在 CMC 要求物件中、將 CMC 要求提交給企業憑證授權單位單位 (CA) ，然後將 CA 傳回的憑證儲存在檔案中。
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780047"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

EnrollFromPublicKey 範例會初始化 PKCS \# 10 憑證要求物件、將它包裝在 CMC 要求物件中、將 CMC 要求提交給企業憑證授權單位單位 (CA) ，然後將 CA 傳回的憑證儲存在檔案中。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollFromPublicKey 資料夾中安裝範例。

## <a name="discussion"></a>討論

EnrollFromPublicKey 範例：

1.  處理下列命令列引數：
    -   憑證範本的名稱。
    -   用來將已安裝的憑證儲存為 base64 編碼位元組陣列的檔案名。
    -   選用的簽署憑證範本名稱。 如果憑證存放區中沒有憑證，則會使用範本來建立簽署憑證。
2.  建立 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)私密金鑰物件，並使用目前電腦的預設密碼編譯提供者、金鑰大小和 [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec)值，呼叫 [**create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create)方法來建立非對稱私密金鑰。
3.  抓取 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件的公開金鑰部分。
4.  建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並使用命令列上指定的範本和公開金鑰將它初始化。
5.  建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 PKCS \# 10 要求物件初始化它。
6.  抓取現有的簽署憑證，如果找不到，則會從命令列上指定的範本建立憑證要求，並嘗試進行註冊。 FindCertByKeyUsage 定義于 enrollCommon .cpp 中。
7.  驗證憑證鏈。
8.  建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，使用簽署憑證將它初始化、從 CMC request 物件抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合，然後將簽署憑證物件新增至集合。
9.  使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 來編碼 CMC 要求。
10. 建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。
11. 建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。
12. 檢查註冊程式的狀態，並將已安裝的憑證儲存至檔案。 EncodeToFileW 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 
