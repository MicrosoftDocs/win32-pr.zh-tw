---
description: 憑證服務支援 (CA) 更新憑證授權單位單位。
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: 憑證授權單位單位更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943706"
---
# <a name="certification-authority-renewal"></a>憑證授權單位單位更新

[*憑證服務*](../secgloss/c-gly.md) 支援 (CA) 更新 [*憑證授權單位*](../secgloss/c-gly.md) 單位。 續約是簽發新憑證，讓 CA 將 CA 的存留期延長至其原始憑證的結束日期之外。 您可以使用 [憑證授權單位單位] MMC 嵌入式管理單元中的工作來更新 CA，或使用 Certutil.exe 工具 (搭配 **-renewCert** 命令) 。

每次更新都會產生新的 CA 憑證;不過，系統管理員可以產生新的公開/私密金鑰組，或重複使用 CA 憑證的現有公開/私密金鑰組。 基於一致性和完整性，ca 憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) ，在 ca 更新後才可供使用。 憑證服務會維護 CA 憑證、Crl 和金鑰的索引，使其可供使用。

在不同的 CA 更新作業期間，CA 憑證和 Crl 的索引和尾碼名稱如下所示。



| 作業                | CA 憑證索引 | CA 憑證檔案名尾碼 | CRL 和金鑰索引 | CRL 和金鑰容器名稱尾碼 |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| 原始 CA 安裝 | 0                    | ""                              | 0                 | ""                                |
| 以新的金鑰更新     | 1                    | " (1) "                           | 1                 | " (1) "                             |
| 續約重複使用金鑰      | 2                    | " (2) "                           | 1                 | " (1) "                             |
| 續約重複使用金鑰      | 3                    | " (3) "                           | 1                 | " (1) "                             |
| 以新的金鑰更新     | 4                    | " (4) "                           | 4                 | " (4) "                             |
| 續約重複使用金鑰      | 5                    | " (5) "                           | 4                 | " (4) "                             |
| 以新的金鑰更新     | 6                    | " (6) "                           | 6                 | " (6) "                             |
| 續約重複使用金鑰      | 7                    | " (7) "                           | 6                 | " (6) "                             |



 

安裝 CA 時，憑證索引為零，且憑證尾碼為 "" (空的字串) 。 每次更新憑證時 (是否重複使用金鑰) ，憑證索引會以1遞增，而憑證檔案名尾碼會變成 " (*n*) " 格式的字串，其中 *n* 代表已更新 CA 憑證的次數。 第一次更新之後，憑證索引為1，憑證檔案名尾碼為 " (1) "。 第二次更新之後，憑證索引為2，憑證檔案名尾碼為 " (2) " 等等。

雖然 CA 憑證索引和尾碼會在每次更新 CA 時遞增一次，但只有在更新程式封裝含新的公開/私密金鑰組時，才會將 CRL 和金鑰索引和檔案名尾碼設定為 CA 憑證索引。 如果沒有，這些索引和尾碼的值會維持與最後一個索引相同。 在更新期間，系統管理員會指定是否要產生新的金鑰組，或使用現有的金鑰組。  (在 [憑證授權單位單位] MMC 嵌入式管理單元中，使用者介面中的選項會指定新的或現有的金鑰組;在 Certutil.exe 工具中，命令 **certutil-renewCert** 會使用新的金鑰組來更新 ca，而 **renewCert ReuseKeys** 會以現有的金鑰組更新 ca。 ) 

CRL 索引直接系結至索引鍵索引，只有在新的金鑰組用於更新時，才會設定為 CA 憑證索引。 在第一次更新 (使用新的金鑰組) 之後，CRL 和金鑰的索引會設定為1，且 CRL 和金鑰容器名稱尾碼為 " (1) "。 不過，在第二次更新之後，CRL 和金鑰的索引會維持為1，而且 CRL 和金鑰容器名稱尾碼也會維持「 (1) 」;這是因為第二個更新使用現有的金鑰組，而且每個 CA 金鑰組只會發出一個 CRL。

您可以藉由呼叫 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)和 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)介面中的 **GetCertificateProperty** 方法 (，來取得已編制索引的 CA 憑證和 crl) 。 當您取得與 CA 憑證或 CRL 相關的特定屬性時，您可以將 CA 憑證的以零為基底的索引附加至屬性名稱。 例如，若要取得對應至 CA 第三個憑證的 CRL 索引，請將 "CRLIndex" 屬性傳遞至 [**ICertServerPolicy：： GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty);若為數據表，則抓取的 "CRLIndex. 2" 屬性值會是1。 名為 "CertCount" 的屬性可以用來判斷 CA 已發出 CA 憑證的次數。

CA 憑證和 Crl 包含的延伸模組可提供憑證和金鑰索引的相關資訊。 此延伸模組是在 Wincrypt 中定義為 szOID \_ CERTSRV \_ CA \_ 版本，其值為 "1.3.6.1.4.1.311.21.1"。 延伸模組資料是 **DWORD** 值， (編碼為 \_ 延伸) 中的 X509 整數; 低16位是憑證索引，而高16位是索引鍵索引。

CA 的初始安裝會產生零的憑證索引和索引鍵索引零。 更新 CA 憑證將會導致憑證索引遞增。 如果金鑰是在續約中重複使用，索引鍵索引會與先前的金鑰索引相同。 如果未重複使用索引鍵，索引鍵索引會與新的憑證索引相符。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
