---
title: 啟用群組原則
description: 瞭解如何藉由啟用群組原則來設定要求者。 查看要求者的考慮並查看其他可用的資源。
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a36d2d464ef4f29c1f021f5ee7d1fad4d820e5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812713"
---
# <a name="enabling-group-policy"></a>啟用群組原則

本主題說明如何藉由啟用群組原則來設定要求者。 EAPHost 要求者可以參與群組原則，以允許網路系統管理員集中設定其網路電腦。

要求者選擇參與群組原則的精確方法和機制是由要求者自行決定。 群組原則參與的機制範例包括用戶端/伺服器端延伸模組、系統管理範本等等。

## <a name="considerations-when-enabling-group-policy"></a>啟用群組原則時的考慮

這些是要求者與群組原則和 EAP 相關的考慮。

1.  EAP 設定應該盡可能地儲存為 XML，而不是二進位格式。 群組原則可能會套用至網域中的任何電腦，而且 EAP 方法設定和使用者資料不保證可在32位和64位處理器架構之間進行移植。 XML 會解決處理器架構界限問題，因為要求者在本機將處理器架構無關的 XML 轉換為設定的二進位標記法。

    如需詳細資訊，請參閱下列主題。

    -   [常見問題的一般問題](general-frequently-asked-questions.yml)
    -   [EAP 方法](eap-method-frequently-asked-questions.yml)的常見問題。
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  如果使用群組原則伺服器端延伸，此延伸模組會呼叫 [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) ，通常是用來判斷可用的方法，並為該原則產生適當的 EAP 設定。 原則接著會推送至套用原則的適當網路用戶端。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 EAP 方法消費者介面](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[為 EAP 方法執行 In-Band NAP 支援](enabling-in-band-nap-support.md)
</dt> <dt>

[為 EAP 方法執行 NAP 支援](implementing-nap-for-eap-methods.md)
</dt> <dt>

[在要求者和 EAP 方法之間傳送資料](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 




