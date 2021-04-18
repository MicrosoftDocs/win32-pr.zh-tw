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
# <a name="eap-attributes"></a><span data-ttu-id="d7934-103">EAP 屬性</span><span class="sxs-lookup"><span data-stu-id="d7934-103">EAP Attributes</span></span>

<span data-ttu-id="d7934-104">EAP 屬性是 [**eap \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) 結構，其中包含與驗證會話相關之預先決定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="d7934-105">屬性是用來在 EAP 方法和要求者之間，或在 EAP 方法和驗證器之間傳達資訊。</span><span class="sxs-lookup"><span data-stu-id="d7934-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="d7934-106">EAP 方法的對等和驗證器執行可能會透過網路交換這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7934-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="d7934-107">主題 [**EAP \_ 屬性 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)中會出現支援的屬性類型的完整清單。</span><span class="sxs-lookup"><span data-stu-id="d7934-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="d7934-108">要求者使用的屬性</span><span class="sxs-lookup"><span data-stu-id="d7934-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="d7934-109">802.1 X 要求者會使用下列屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="d7934-110">**eatVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="d7934-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="d7934-111">PPP 用戶端要求者會使用下列屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="d7934-112">**eatMinimum**</span><span class="sxs-lookup"><span data-stu-id="d7934-112">**eatMinimum**</span></span>
-   <span data-ttu-id="d7934-113">**eatEAPTLV**</span><span class="sxs-lookup"><span data-stu-id="d7934-113">**eatEAPTLV**</span></span>

<span data-ttu-id="d7934-114">PPP 伺服器要求者會使用下列屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="d7934-115">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d7934-115">**eatUserName**</span></span>
-   <span data-ttu-id="d7934-116">**eatReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="d7934-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="d7934-117">**eatState**</span><span class="sxs-lookup"><span data-stu-id="d7934-117">**eatState**</span></span>
-   <span data-ttu-id="d7934-118">**eatSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="d7934-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="d7934-119">**eatEAPMessage**</span><span class="sxs-lookup"><span data-stu-id="d7934-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="d7934-120">方法匯出的屬性</span><span class="sxs-lookup"><span data-stu-id="d7934-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="d7934-121">EAP 方法可以匯出下列屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="d7934-122">**eatClearTextPassword**</span><span class="sxs-lookup"><span data-stu-id="d7934-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="d7934-123">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="d7934-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="d7934-124">**eatMethodId**</span><span class="sxs-lookup"><span data-stu-id="d7934-124">**eatMethodId**</span></span>

<span data-ttu-id="d7934-125">下列屬性類型是由 EAP [傳輸層級安全性 (TLS) ](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (eap-tls) 方法匯出。</span><span class="sxs-lookup"><span data-stu-id="d7934-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="d7934-126">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="d7934-126">**eatCertificateOID**</span></span>

<span data-ttu-id="d7934-127">以下是 [Microsoft 挑戰交握驗證通訊協定2.0 版](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (CHAPv2) 方法匯出的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="d7934-128">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d7934-128">**eatUserName**</span></span>
-   <span data-ttu-id="d7934-129">**eatCredentialsChanged**</span><span class="sxs-lookup"><span data-stu-id="d7934-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="d7934-130">以下是網路原則伺服器 (NPS) 所使用的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="d7934-131">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="d7934-131">**eatCertificateOID**</span></span>

<span data-ttu-id="d7934-132">以下是受保護的可延伸 [驗證通訊協定（ (PEAP) ](/previous-versions/windows/embedded/ms899190(v=msdn.10)) 方法）匯出的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="d7934-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="d7934-133">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d7934-133">**eatUserName**</span></span>
-   <span data-ttu-id="d7934-134">**eatPEAPEmbeddedEAPTypeId**</span><span class="sxs-lookup"><span data-stu-id="d7934-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="d7934-135">**eatPEAPFastRoamedSession**</span><span class="sxs-lookup"><span data-stu-id="d7934-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="d7934-136">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="d7934-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7934-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7934-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7934-138">**EAP \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="d7934-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="d7934-139">**EAP \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d7934-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 