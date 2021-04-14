---
title: 在要求者和 EAP 方法之間傳送資料
description: 瞭解如何在要求者和 EAP 方法之間傳輸資料。 您可以使用 EAP 屬性來完成方法之間的資料傳輸。
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382882"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="bf891-104">在要求者和 EAP 方法之間傳送資料</span><span class="sxs-lookup"><span data-stu-id="bf891-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="bf891-105">使用 EAP 屬性可讓要求者和 EAP 方法之間的資料交換。</span><span class="sxs-lookup"><span data-stu-id="bf891-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="bf891-106">屬性耗用量</span><span class="sxs-lookup"><span data-stu-id="bf891-106">Attribute Consumption</span></span>

<span data-ttu-id="bf891-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 會取用直接傳遞給已設定 eap 方法的 eap 屬性。</span><span class="sxs-lookup"><span data-stu-id="bf891-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="bf891-108">同樣地，EAP 方法可以自由傳回動作程式碼，向要求者指出屬性可供使用，而且應該使用 [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes)收集屬性。</span><span class="sxs-lookup"><span data-stu-id="bf891-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="bf891-109">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="bf891-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="bf891-110">[EAP 對等要求者動作碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)。</span><span class="sxs-lookup"><span data-stu-id="bf891-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="bf891-111">[EAP 對等要求者原因代碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)。</span><span class="sxs-lookup"><span data-stu-id="bf891-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="bf891-112">[EAP 驗證器方法動作代碼](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)。</span><span class="sxs-lookup"><span data-stu-id="bf891-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="bf891-113">要求者必須忽略無法辨識或無法採取行動的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf891-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="bf891-114">使用 [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) 這些忽略的屬性會傳送回 EAPHOST 和 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="bf891-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="bf891-115">特定廠商屬性</span><span class="sxs-lookup"><span data-stu-id="bf891-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="bf891-116">使用廠商專屬的 EAP 屬性，EAP 方法和要求者可以參與資料交換以取得特定用途。</span><span class="sxs-lookup"><span data-stu-id="bf891-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="bf891-117">若要求者和方法不支援廠商專屬的屬性，則會忽略廠商專屬屬性。</span><span class="sxs-lookup"><span data-stu-id="bf891-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="bf891-118">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="bf891-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="bf891-119">[EAP 屬性](about-eap-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="bf891-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="bf891-120">[**EAP \_屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)。</span><span class="sxs-lookup"><span data-stu-id="bf891-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf891-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf891-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf891-122">設定 EAP 方法消費者介面</span><span class="sxs-lookup"><span data-stu-id="bf891-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="bf891-123">啟用群組原則</span><span class="sxs-lookup"><span data-stu-id="bf891-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="bf891-124">為 EAP 方法執行 In-Band NAP 支援</span><span class="sxs-lookup"><span data-stu-id="bf891-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="bf891-125">為 EAP 方法執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="bf891-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="bf891-126">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="bf891-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




