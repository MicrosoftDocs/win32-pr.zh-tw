---
description: 有幾個函式會將憑證內容或內容的連結新增至 store \[ Platform 軟體發展工具組 (SDK) \] 。
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: 使用憑證存放區中的憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320040"
---
# <a name="working-with-certificates-in-certificate-stores"></a>使用憑證存放區中的憑證

有幾個函式會將憑證內容或內容的連結新增至存放區。

針對已在憑證內容表單中的憑證：

-   [**CertAddCertificateCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**CertAddCRLCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**CertAddCTLCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

針對編碼形式但不是完整憑證內容的憑證：

-   [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

下列函式會將憑證、CRL 或 CTL 的參考計數遞減一，以將其從存放區中刪除。 如果這會導致參考計數變成零，則會釋放用來儲存憑證、CRL 或 CTL 的記憶體。

-   [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



