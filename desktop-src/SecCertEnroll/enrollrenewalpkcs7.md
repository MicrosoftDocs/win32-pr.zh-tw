---
description: 建立 PKCS \# 7 要求物件以更新現有的憑證。 要求物件會使用新的金鑰組，但會保留與要更新之憑證相關聯的密碼編譯提供者。
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3da14719cc2a9e6bdf4c16cad57d24b9ee4ec0c2ee955cc8b7c20643b2b6f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740428"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

EnrollRenewalPKCS7 範例會建立 PKCS \# 7 要求物件來更新現有的憑證。 要求物件會使用新的金鑰組，但會保留與要更新之憑證相關聯的密碼編譯提供者。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollRenewalPKCS7 資料夾中安裝範例。

## <a name="discussion"></a>討論

EnrollRenewalPKCS7 範例：

1.  處理命令列引數。 命令列應該包含用來建立憑證要求的範本名稱。
2.  使用命令列上指定的範本名稱來抓取現有的憑證，或者，如果找不到憑證，則會嘗試使用該範本註冊一個憑證。 FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。
3.  驗證憑證鏈，並將憑證轉換成 **BSTR**。
4.  建立 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件，並使用現有的憑證將它初始化。 由於 *inheritOptions* 參數設定為 InheritDefault，因此會為要求建立新的金鑰組，但會使用現有憑證中的密碼編譯提供者。 如需詳細資訊，請參閱 [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) 方法。
5.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 PKCS \# 7 要求物件初始化它、嘗試向 CA 註冊，並監視註冊程式的狀態。 CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[PKCS \# 7 更新要求](pkcs--7--renewal-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



