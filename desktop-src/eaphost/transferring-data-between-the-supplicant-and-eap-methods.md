---
title: 在要求者和 EAP 方法之間傳送資料
description: 瞭解如何在要求者和 EAP 方法之間傳輸資料。 您可以使用 EAP 屬性來完成方法之間的資料傳輸。
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085649"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>在要求者和 EAP 方法之間傳送資料

使用 EAP 屬性可讓要求者和 EAP 方法之間的資料交換。

## <a name="attribute-consumption"></a>屬性耗用量

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 會取用直接傳遞給已設定 eap 方法的 eap 屬性。 同樣地，EAP 方法可以自由傳回動作程式碼，向要求者指出屬性可供使用，而且應該使用 [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)收集屬性。

如需詳細資訊，請參閱下列主題。

-   [EAP 對等要求者動作碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)。
-   [EAP 對等要求者原因代碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)。
-   [EAP Authenticator 方法動作代碼](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)。

要求者必須忽略無法辨識或無法採取行動的屬性。 使用 [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) 這些忽略的屬性會傳送回 EAPHOST 和 EAP 方法。

## <a name="vendor-specific-attributes"></a>特定廠商屬性

使用廠商專屬的 EAP 屬性，EAP 方法和要求者可以參與資料交換以取得特定用途。 若要求者和方法不支援廠商專屬的屬性，則會忽略廠商專屬屬性。

如需詳細資訊，請參閱下列主題。

-   [EAP 屬性](about-eap-attributes.md)。
-   [**EAP \_屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 EAP 方法消費者介面](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[啟用群組原則](enabling-group-policy.md)
</dt> <dt>

[為 EAP 方法執行 In-Band NAP 支援](enabling-in-band-nap-support.md)
</dt> <dt>

[為 EAP 方法執行 NAP 支援](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 




