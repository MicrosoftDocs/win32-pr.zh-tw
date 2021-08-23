---
description: 使用範本、主體名稱和金鑰長度（以位為單位），向憑證授權單位單位註冊 (CA) 的終端使用者。
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4763e3ae68404e47207dccdb75c759fc30394e849bee07a71f2c54c649347a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669908"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

EnrollSimpleUserCert 範例會使用範本、主體名稱和金鑰長度（以位為單位），向使用者註冊憑證授權單位單位 (CA) 。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，根據預設，會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows 7.0 版的 \\ \\ \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollSimpleUserCert 資料夾中安裝 c + + 版本的範例。 c # 版本安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows 7.0 版 \\ \\ 範例 \\ X509 憑證註冊 \\ CSharp \\ EnrollSimpleUserCert 資料夾中。

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

 

 



