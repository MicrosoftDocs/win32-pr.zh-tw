---
description: 憑證授權單位 (CA) 負責證明使用者、電腦及組織的身分識別。
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: 憑證授權單位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850871"
---
# <a name="certification-authorities"></a>憑證授權單位

 (CA) 的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位負責證明至使用者、電腦和組織的身分識別。 CA 會驗證實體，並簽發數位簽署憑證為該身分識別提供擔保。 CA 也可以管理、撤銷，以及更新憑證。

CA 可以是公用或私用。 公用 CA 提供憑證服務，通常是透過網際網路公開的。 私用 CA 提供此服務給分隔擴展的成員，例如商務員工或其他私人群組的成員。

CA 用來驗證使用者的方式不同，但不在本檔的討論範圍內。 不過，驗證的方法會因提供者類型而異。 例如，私人 CA 可以參考群組名單（例如員工資料庫或 Active Directory）來建立使用者的身分識別。 公開 CA 所執行的驗證方法通常比較複雜，而且部分取決於憑證所承諾的保證等級。

隨著公開金鑰基礎結構的擴展 (PKI) 成長，單一 CA 可能會變得很難有效管理它所發出的所有憑證。 CA 可以藉由授權 PKI 中的其他 Ca 來簽發憑證，以彌補這些問題。 初始 CA 稱為根，而它授權的 Ca 稱為附屬節點。 次級 Ca 也可以在根設定的限制內指定自己的子公司。 產生的結構稱為「憑證階層」。 對階層中較低的 Ca 發出的憑證，包含足夠的憑證來追蹤指向根目錄的路徑。 這稱為憑證鏈。

「憑證授權單位單位」一詞指的是可保證使用者身分識別的組織，以及組織用來發行和管理憑證的伺服器。 您可以設定 Windows server 做為 CA 伺服器，而且此檔通常會在使用「CA」一詞時參考該伺服器。

憑證註冊 API 主要是使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件來與 CA 互動。 此物件上的 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 方法可以自動編碼憑證要求、將憑證要求提交給 CA，以及安裝已發行的憑證。 您也可以使用已初始化的 **IX509Enrollment** 物件進行頻外註冊或延遲註冊。 此外，您可以使用 [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) 物件來監視註冊狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKI 元素](about-pki-components.md)
</dt> </dl>

 

 
