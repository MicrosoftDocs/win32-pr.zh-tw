---
description: 原則模組是接收來自憑證服務之要求、評估這些要求，以及指定用來填滿這些要求之憑證的選擇性屬性的程式。
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: 原則模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945131"
---
# <a name="policy-modules"></a><span data-ttu-id="0cc32-103">原則模組</span><span class="sxs-lookup"><span data-stu-id="0cc32-103">Policy Modules</span></span>

<span data-ttu-id="0cc32-104">原則模組是接收來自憑證服務之要求、評估這些要求，以及指定用來填滿這些要求之憑證的選擇性屬性的程式。</span><span class="sxs-lookup"><span data-stu-id="0cc32-104">Policy modules are programs that receive requests from the Certificate Services, evaluate those requests, and specify optional properties of the certificates that are built to fill these requests.</span></span> <span data-ttu-id="0cc32-105">原則模組會實作為 [*動態連結程式庫*](../secgloss/d-gly.md) ， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="0cc32-105">A policy module is implemented as a [*dynamic-link library*](../secgloss/d-gly.md) (DLL).</span></span> <span data-ttu-id="0cc32-106">原則模組可以使用 [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 介面與憑證服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="0cc32-106">A policy module can use the [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface to communicate with Certificate Services.</span></span> <span data-ttu-id="0cc32-107">憑證服務會透過直接 COM 呼叫來與原則模組進行通訊，或者，如果此模組不支援透過自動化的直接 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cc32-107">Certificate Services communicates with a policy module by means of direct COM calls or, if the module does not support direct COM calls, by means of Automation.</span></span>

<span data-ttu-id="0cc32-108">原則模組可查看現有的憑證屬性和擴充功能，也可能會查看要求屬性和屬性。</span><span class="sxs-lookup"><span data-stu-id="0cc32-108">A policy module may view existing certificate properties and extensions, and it may also view request attributes and properties.</span></span> <span data-ttu-id="0cc32-109">此外，原則模組可能會設定或修改憑證延伸和 "NotBefore" 和 "NotAfter" 屬性，以及憑證主體 (RDN) 的 [*相對辨別名稱*](../secgloss/r-gly.md) （受限於特定限制）。</span><span class="sxs-lookup"><span data-stu-id="0cc32-109">In addition, a policy module may set or modify certificate extensions and "NotBefore" and "NotAfter" properties, as well as the [*relative distinguished name*](../secgloss/r-gly.md) (RDN) of a Certificate Subject, subject to certain restrictions.</span></span> <span data-ttu-id="0cc32-110">原則模組最後會發出或拒絕 [*憑證要求*](../secgloss/c-gly.md) ，或將其保留為擱置中。</span><span class="sxs-lookup"><span data-stu-id="0cc32-110">A policy module ultimately issues or denies the [*certificate request*](../secgloss/c-gly.md) or holds it pending.</span></span>

<span data-ttu-id="0cc32-111">撰寫自訂原則模組之前，請考慮使用其中一個預設原則模組。</span><span class="sxs-lookup"><span data-stu-id="0cc32-111">Before writing a custom policy module, consider using one of the default policy modules.</span></span> <span data-ttu-id="0cc32-112">憑證服務企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 和獨立 CA 都會隨附適當的預設原則模組。</span><span class="sxs-lookup"><span data-stu-id="0cc32-112">Both the Certificate Services enterprise [*certification authority*](../secgloss/c-gly.md) (CA) and stand-alone CA ship with an appropriate default policy module.</span></span> <span data-ttu-id="0cc32-113">企業和獨立的預設原則模組都會發出憑證要求 (雖然獨立的預設原則是將憑證擱置，直到系統管理員以手動方式發出) 為止。</span><span class="sxs-lookup"><span data-stu-id="0cc32-113">Both the enterprise and stand-alone default policy modules issue certificate requests (although the stand-alone default policy is to hold the certificate pending until it is manually issued by an administrator).</span></span> <span data-ttu-id="0cc32-114">企業憑證授權單位單位只能使用 Microsoft 提供的企業原則模組。</span><span class="sxs-lookup"><span data-stu-id="0cc32-114">An enterprise certification authority should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="0cc32-115">企業 CA 需要 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="0cc32-115">The enterprise CA requires Active Directory.</span></span> <span data-ttu-id="0cc32-116">預設原則模組的其他功能包括憑證範本、 [*存取控制清單*](../secgloss/a-gly.md) (ACL) 安全性的憑證範本，以確保只會將要求發給已授權、預先定義的延伸模組新增至已發行的憑證，以及支援智慧卡網域登入憑證。</span><span class="sxs-lookup"><span data-stu-id="0cc32-116">Additional features of its default policy module include certificate templates, [*access control list*](../secgloss/a-gly.md) (ACL) security on the certificate templates to ensure requests are issued to only those authorized, predefined extensions added to the issued certificate, and support for smart card domain logon certificates.</span></span>

<span data-ttu-id="0cc32-117">預設的獨立 CA 原則模組並不支援預設 enterprise 模組的許多功能，但它支援發行智慧卡憑證。</span><span class="sxs-lookup"><span data-stu-id="0cc32-117">The default stand-alone CA policy module does not support many of the features of the default enterprise module, but it does support the issuance of smart card certificates.</span></span> <span data-ttu-id="0cc32-118">如需特定詳細資料，以及預設原則模組的最新功能，請參閱產品檔。</span><span class="sxs-lookup"><span data-stu-id="0cc32-118">For specific details, as well as the most current capabilities of the default policy module, see the product documentation.</span></span>

<span data-ttu-id="0cc32-119">針對預設原則模組無法接受的安裝，憑證服務允許自訂原則模組。</span><span class="sxs-lookup"><span data-stu-id="0cc32-119">For installations where the default policy module is unacceptable, Certificate Services allows custom policy modules.</span></span> <span data-ttu-id="0cc32-120">如需詳細資訊，請參閱 [撰寫自訂原則模組](writing-custom-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="0cc32-120">For more information, see [Writing Custom Policy Modules](writing-custom-modules.md).</span></span>

 

 
