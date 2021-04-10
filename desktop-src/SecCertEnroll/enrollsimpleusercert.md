---
description: 使用範本、主體名稱和金鑰長度（以位為單位），向憑證授權單位單位註冊 (CA) 的終端使用者。
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026974"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

EnrollSimpleUserCert 範例會使用範本、主體名稱和金鑰長度（以位為單位），向使用者註冊憑證授權單位單位 (CA) 。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，根據預設，系統會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollSimpleUserCert 資料夾中安裝 c + + 版本的範例。 C # 版本安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ X509 憑證註冊 \\ CSharp \\ EnrollSimpleUserCert 資料夾中。

## <a name="discussion"></a>討論

EnrollSimpleUserCert 範例：

1.  處理命令列引數。 命令列應該包含範本的名稱、主體名稱和金鑰長度。
2.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用範本將它初始化。
3.  從註冊物件中抓取內部憑證要求物件，並針對 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件進行查詢。 最內層的要求一律是 PKCS \# 10 要求。
4.  從 PKCS 10 要求抓取 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件 \# ，並設定命令列上指定的金鑰長度。
5.  建立 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件，並使用它來編碼 X. 500 主體名稱，並將名稱新增至 PKCS \# 10 要求。
6.  嘗試向 CA 註冊終端使用者，並監視註冊程式的進度。 CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



