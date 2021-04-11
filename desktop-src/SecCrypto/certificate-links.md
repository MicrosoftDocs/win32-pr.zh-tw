---
description: CertAddCertificateLinkToStore、CertAddCRLLinkToStore 和 CertAddCTLLinkToStore 函式會將現有內容的連結新增至憑證存放區，而不是新增這些內容的複本。
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: 憑證連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115329"
---
# <a name="certificate-links"></a>憑證連結

[**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)、 [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)和 [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)函式會將現有內容的連結新增至 [*憑證存放區*](../secgloss/c-gly.md)，而不是新增這些內容的複本。 將連結新增至存放區，可讓相同的實體 [*憑證*](../secgloss/c-gly.md)、 [*CRL*](../secgloss/c-gly.md)或 [*CTL*](../secgloss/c-gly.md) 可透過數個不同的存放區使用。 從原始內容存放區或儲存該內容連結的存放區中，對 [*內容*](../secgloss/c-gly.md) 的擴充屬性所做的變更，都可在保存原始內容的存放區中，以及具有該內容連結的所有其他存放區中使用。

如需使用 [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)的範例，請參閱 [範例 C 程式：憑證存放區作業](example-c-program-certificate-store-operations.md)。

![憑證連結](images/mancert1.png)

假設憑證 A. 1、2、3和 A. 4 最初是存放區，而憑證 b. 1、b. 2、b. 3 和 b. 4 最初是存放區 B。

-   此圖表顯示在 store B 中新增至憑證 A 的連結，以及將 store A 中新增至憑證 B 的連結。2。
-   憑證 A. 2 仍在存放區 A 中。原始的 b. 2 仍在 store B 中。
-   從 store A 或 store B 對憑證 A. 2 或憑證 B 的擴充屬性所做的任何變更，都將可供這兩個存放區使用。
-   如果已建立憑證 A. 3 的複本，並將其儲存在存放區 B 中，則不會在存放區 B 的新複本中看到對原始 A. 3 憑證的擴充屬性所做的任何變更。如果在 store B 中對憑證 A 的擴充屬性進行了變更，這些變更不會影響原始的. 3 憑證的內容，也不會顯示在存放區中。

 

 
