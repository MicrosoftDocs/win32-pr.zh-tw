---
title: 啟用群組原則
description: 瞭解如何藉由啟用群組原則來設定要求者。 查看要求者的考慮並查看其他可用的資源。
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382901"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="a0836-104">啟用群組原則</span><span class="sxs-lookup"><span data-stu-id="a0836-104">Enabling Group Policy</span></span>

<span data-ttu-id="a0836-105">本主題說明如何藉由啟用群組原則來設定要求者。</span><span class="sxs-lookup"><span data-stu-id="a0836-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="a0836-106">EAPHost 要求者可以參與群組原則，以允許網路系統管理員集中設定其網路電腦。</span><span class="sxs-lookup"><span data-stu-id="a0836-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="a0836-107">要求者選擇參與群組原則的精確方法和機制是由要求者自行決定。</span><span class="sxs-lookup"><span data-stu-id="a0836-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="a0836-108">群組原則參與的機制範例包括用戶端/伺服器端延伸模組、系統管理範本等等。</span><span class="sxs-lookup"><span data-stu-id="a0836-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="a0836-109">啟用群組原則時的考慮</span><span class="sxs-lookup"><span data-stu-id="a0836-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="a0836-110">這些是要求者與群組原則和 EAP 相關的考慮。</span><span class="sxs-lookup"><span data-stu-id="a0836-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="a0836-111">EAP 設定應該盡可能地儲存為 XML，而不是二進位格式。</span><span class="sxs-lookup"><span data-stu-id="a0836-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="a0836-112">群組原則可能會套用至網域中的任何電腦，而且 EAP 方法設定和使用者資料不保證可在32位和64位處理器架構之間進行移植。</span><span class="sxs-lookup"><span data-stu-id="a0836-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="a0836-113">XML 會解決處理器架構界限問題，因為要求者在本機將處理器架構無關的 XML 轉換為設定的二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="a0836-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="a0836-114">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="a0836-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="a0836-115">常見問題的一般問題</span><span class="sxs-lookup"><span data-stu-id="a0836-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="a0836-116">[EAP 方法](eap-method-frequently-asked-questions.md)的常見問題。</span><span class="sxs-lookup"><span data-stu-id="a0836-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="a0836-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="a0836-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="a0836-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="a0836-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="a0836-119">如果使用群組原則伺服器端延伸，此延伸模組會呼叫 [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) ，通常是用來判斷可用的方法，並為該原則產生適當的 EAP 設定。</span><span class="sxs-lookup"><span data-stu-id="a0836-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="a0836-120">原則接著會推送至套用原則的適當網路用戶端。</span><span class="sxs-lookup"><span data-stu-id="a0836-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0836-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0836-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0836-122">設定 EAP 方法消費者介面</span><span class="sxs-lookup"><span data-stu-id="a0836-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="a0836-123">為 EAP 方法執行 In-Band NAP 支援</span><span class="sxs-lookup"><span data-stu-id="a0836-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="a0836-124">為 EAP 方法執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="a0836-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="a0836-125">在要求者和 EAP 方法之間傳送資料</span><span class="sxs-lookup"><span data-stu-id="a0836-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="a0836-126">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="a0836-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




