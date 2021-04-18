---
title: EAP 屬性
description: 是 EAP \_ 屬性結構，包含與驗證會話相關之預先決定的資料類型。
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "106968521"
---
# <a name="eap-attributes"></a>EAP 屬性

EAP 屬性是 [**eap \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) 結構，其中包含與驗證會話相關之預先決定的資料類型。 屬性是用來在 EAP 方法和要求者之間，或在 EAP 方法和驗證器之間傳達資訊。 EAP 方法的對等和驗證器執行可能會透過網路交換這些屬性。

主題 [**EAP \_ 屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)中會出現支援的屬性類型的完整清單。

## <a name="attributes-consumed-by-supplicants"></a>要求者使用的屬性

802.1 X 要求者會使用下列屬性類型。

-   **eatVendorSpecific**

PPP 用戶端要求者會使用下列屬性類型。

-   **eatMinimum**
-   **eatEAPTLV**

PPP 伺服器要求者會使用下列屬性類型。

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>方法匯出的屬性

EAP 方法可以匯出下列屬性類型。

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

下列屬性類型是由 EAP [傳輸層級安全性 (TLS) ](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (eap-tls) 方法匯出。

-   **eatCertificateOID**

以下是 [Microsoft 挑戰交握驗證通訊協定2.0 版](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (CHAPv2) 方法匯出的屬性類型。

-   **eatUserName**
-   **eatCredentialsChanged**

以下是網路原則伺服器 (NPS) 所使用的屬性類型。

-   **eatCertificateOID**

以下是受保護的可延伸 [驗證通訊協定（ (PEAP) ](/previous-versions/windows/embedded/ms899190(v=msdn.10)) 方法）匯出的屬性類型。

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**EAP \_ 屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 