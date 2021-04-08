---
description: CryptoAPI 提供的函式可用來處理憑證、憑證撤銷清單 (Crl) 和 (Ctl) 的憑證信任清單。
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: 具有憑證的作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851280"
---
# <a name="operations-with-certificates"></a>具有憑證的作業

[*CryptoAPI*](../secgloss/c-gly.md) 提供的函式可用來處理 [*憑證*](../secgloss/c-gly.md)、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 和 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。 這些函數包括將編碼的型別轉換成內容類型的函式、重複物件的函式，以及釋放這些物件的函式。 這些函式會將資訊編碼為內容，但不會將此內容新增至任何存放區。 這些函數包括 [**CertCreateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)、 [**CertCreateCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)和 [**CertCreateCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)。 使用適當的 CertFree 函式來釋放這些函式的其中一個所建立的內容。

重複憑證、Crl 和 Ctl 的 CryptoAPI 函式會遞增指定內容中的 [*參考計數器*](../secgloss/r-gly.md) ，並傳回內容的指標。 複製函式不會配置額外的空間，也不會將資料從內容複寫到新的記憶體位置。 這些函數包括 [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)、 [**CertDuplicateCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)和 [**CertDuplicateCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)。 使用任何這些函式所建立的內容，必須使用適當的 CertFree 函式來釋放。

可用憑證、Crl 和 Ctl 的 CryptoAPI 函數有 [**CertFreeCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)、 [**CertFreeCRLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)和 [**CertFreeCTLCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)。 這些函式中的每一個都會減少內容中的 [*參考計數*](../secgloss/r-gly.md) 。 如果參考計數到達零，則會釋放配置給內容的記憶體。

如需使用憑證、Crl 和 Ctl 之函式的完整清單，請參閱 [憑證和憑證存放區維護功能](cryptography-functions.md)、 [憑證功能](cryptography-functions.md)、 [憑證撤銷清單](cryptography-functions.md)函式和 [憑證信任清單](cryptography-functions.md)函式。

 

 
