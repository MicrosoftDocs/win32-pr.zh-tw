---
description: 憑證中的資料、憑證撤銷清單 (CRL) 或憑證信任清單 (CTL) 內容（包括任何擴充功能）都是唯讀的，而且無法變更。
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: 憑證擴充屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127088"
---
# <a name="certificate-extended-properties"></a>憑證擴充屬性

[*憑證*](../secgloss/c-gly.md)中的資料、[*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) 或 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) [*內容*](../secgloss/c-gly.md)（包括任何擴充功能）都是唯讀的，而且無法變更。 不過，在 Microsoft 平臺上，CryptoAPI 憑證也有可新增和變更的動態擴充屬性。

> [!Note]  
> 擴充屬性會與憑證相關聯，而且不是證書 [*頒發機構*](../secgloss/c-gly.md) 單位所簽發的憑證 (CA) 的一部分。 在非 Microsoft 平臺上使用擴充屬性時，憑證上無法使用它。

 

這些屬性包含下列資料：

-   適用于與憑證搭配使用的私密金鑰。
-   表示要在憑證上執行的雜湊類型。
-   提供與憑證相關聯的使用者定義資訊。

在 Microsoft 平臺上，這些屬性的值會附加至憑證，並隨之移動。 目前使用屬性識別碼識別的預先定義屬性包含下列屬性：

-   這些屬性會將憑證系結至特定的 CSP，並將該 CSP 內的特定私密金鑰系結至特定的私密金鑰：
    -   CERT \_ KEY \_ >PROV \_ 句 \_ 柄 \_ 識別碼
    -   CERT \_ KEY \_ >PROV \_ INFO \_ 資訊 \_ 識別碼
    -   CERT \_ KEY \_ CONTEXT \_ 內容 \_ 識別碼
-   這些屬性工作表示執行雜湊作業時要使用的雜湊演算法：
    -   CERT \_ SHA1 \_ 雜湊的 \_ \_ 識別碼
    -   CERT \_ MD5 \_ 雜湊的 \_ \_ 識別碼

如需目前定義之擴充憑證屬性的完整清單，以及每個屬性的意義與用法說明，請參閱 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 和 [**CertSetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CertGetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
