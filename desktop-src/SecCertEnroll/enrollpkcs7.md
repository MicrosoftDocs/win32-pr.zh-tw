---
description: 藉 \# 由繼承公開金鑰和私密金鑰和憑證範本，從現有的憑證建立 PKCS 7 要求。
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0635fdf4daacc9c7a04db98c7e34e9d3495c6f18ca3e145b166f19e3cd49610a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779949"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

EnrollPKCS7 範例會透過 \# 繼承公開金鑰和私密金鑰和憑證範本，從現有的憑證建立 PKCS 7 要求。 現有的憑證會用來簽署要求。 此範例會在憑證階層中註冊使用者，並安裝憑證回應。 此範例會使用現有的憑證來註冊並安裝新的憑證。 如需更新現有憑證的詳細資訊，請參閱 [enrollRenewalPKCS7](enrollrenewalpkcs7.md)。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollPKCS7 資料夾中安裝範例。

## <a name="discussion"></a>討論

EnrollPKCS7 範例：

1.  處理命令列引數。 命令列應該包含用來尋找現有憑證的憑證範本名稱。
2.  使用命令列上指定的範本名稱來抓取現有的憑證，或者，如果找不到憑證，則嘗試註冊使用該範本建立的新憑證。 FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。
3.  驗證憑證鏈，並將憑證轉換成 **BSTR**。
4.  建立 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件，並使用現有的憑證將它初始化。 新的 PKCS \# 7 要求物件會從現有的憑證繼承私用和公開金鑰和範本。
5.  建立 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件，並使用現有的憑證將它初始化，然後將它新增至 PKCS \# 7 request 物件。
6.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，使用 PKCS \# 7 要求物件初始化它、嘗試向 CA 註冊，並監視註冊程式的狀態。 CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



