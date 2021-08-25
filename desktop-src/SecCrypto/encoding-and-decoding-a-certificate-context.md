---
description: 使用 CryptoAPI 編碼和解碼憑證內容。
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: 編碼和解碼憑證內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f640e12034ebf4ec84e0e71013197f043453b62e1102018dcfe9ea887d6ada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874882"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>編碼和解碼憑證內容

[*CryptoAPI*](../secgloss/c-gly.md) 支援 [*憑證*](../secgloss/c-gly.md)的編碼和解碼。 CryptoAPI 包含廣泛、彈性的函式和 C 結構系統，可讓您以各種方式進行編碼和解碼。 CryptoAPI 支援標準的 [*x.509*](../secgloss/x-gly.md) 憑證結構和標準 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 編碼，以提供與其他系統之間的互通性。

如需編碼資料的總覽，請參閱 [編碼和解碼的資料](encoded-and-decoded-data.md)。

## <a name="certificate-contexts"></a>憑證內容

[*憑證內容*](../secgloss/c-gly.md)（ [**CERT \_ coNtext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)）是包含編碼成員的 C 結構、[*憑證存放區*](../secgloss/c-gly.md)的控制碼、原始編碼 [*憑證 BLOB*](../secgloss/c-gly.md)的指標，以及 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)C 結構的指標。

[**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構是憑證的核心。 它包含以直接形式與編碼形式的憑證中的所有基本資訊。 下圖顯示 **CERT \_ 資訊** 結構，其中所有編碼的成員都顯示為陰影。

![cert \- 資訊結構](images/certinf2.png)

**IssuerUniqueID** 和 **SubjectUniqueID** 成員是 [*x.509*](../secgloss/x-gly.md)第2版憑證的一部分，但很少使用。 第3版中的憑證擴充取代這些成員的功能。

如果編碼 (所包含的資訊已加上陰影) 成員 **簽發者** 和 **主體** ，則必須將這些成員解碼。 使用 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 來解碼這些成員。 下圖顯示解碼其中一個成員的流程。

![使用 cryptdecodeobject 解碼](images/infoflow.png)

在說明的案例中， [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 函數會建立 [**憑證 \_ 名稱 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) 結構、 [**cert \_ rdn**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) 結構的陣列、憑證 [**\_ rdn \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構的對應陣列，以及包含名稱的字串。 **CERT \_ RDN \_ ATTR** 結構的成員會決定字串的內容。 例如，如果 **pszObjId** 成員是2.5.4.3，字串就會包含一般名稱。 如果是2.5.4.10，則字串會包含組織名稱。 如需 (Oid) 的 [*物件識別碼*](../secgloss/o-gly.md) 清單，請參閱 **CERT \_ RDN \_ ATTR**。

**DwValueType** 成員包含有關字串類型的資訊。 如果它是 CERT \_ RDN \_ 可列印 \_ 字串，則值成員會包含位元組寬度、以零結束的字元字串。 如果它是 CERT \_ RDN \_ UNICODE \_ 字串，則字串會是雙寬度 (文字大小) 字元字串。

如需編碼和解碼憑證的詳細程式，請參閱 [編碼憑證 \_ 資訊結構](encoding-a-cert-info-structure.md) 和 [解碼 cert \_ 資訊結構](decoding-a-cert-info-structure.md)。

 

 
