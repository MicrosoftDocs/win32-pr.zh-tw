---
description: 建立自訂的 PKCS \# 10 要求，並嘗試在企業憑證授權單位單位 (CA) 中註冊它。
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780037"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

EnrollCustomPKCS10 \_ 2 範例會建立自訂的 PKCS \# 10 要求，並嘗試在企業 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 中註冊它。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollCustomPKCS10 \_ 2 資料夾中。

## <a name="discussion"></a>討論

EnrollCustomPKCS10 \_ 2 範例：

1.  處理命令列引數。 命令列應該包含範本的名稱和密碼編譯提供者的名稱。
2.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用命令列上指定的範本名稱將它初始化。
3.  從註冊物件捕獲 [*憑證要求*](/windows/desktop/SecGloss/c-gly) 。
4.  \#從步驟3取得的憑證要求物件抓取最內層的 PKCS 10 要求。
5.  從 PKCS 10 要求中取出 [*私用金鑰*](/windows/desktop/SecGloss/p-gly) \# 。
6.  建立 [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) 集合，並將可用的密碼編譯提供者加入至集合，然後針對命令列上指定的提供者抓取 [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) 物件。
7.  設定私密金鑰的狀態物件。
8.  嘗試註冊 [*憑證要求*](/windows/desktop/SecGloss/c-gly)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKCS \# 10 要求](pkcs--10-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 
