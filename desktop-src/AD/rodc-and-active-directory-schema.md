---
title: Read-Only Dc 和 Active Directory 架構
description: Windows Server 2008 引進了一種新類型的網域控制站， (RODC) 的唯讀網域控制站。
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093455"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a><span data-ttu-id="9819d-103">Read-Only Dc 和 Active Directory 架構</span><span class="sxs-lookup"><span data-stu-id="9819d-103">Read-Only DCs and the Active Directory Schema</span></span>

<span data-ttu-id="9819d-104">Windows Server 2008 引進了一種新類型的網域控制站， (RODC) 的唯讀網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9819d-104">Windows Server 2008 introduces a new type of domain controller, the Read-only Domain Controller (RODC).</span></span> <span data-ttu-id="9819d-105">這會提供網域控制站，以便在無法放置完整網域控制站的分公司中使用。</span><span class="sxs-lookup"><span data-stu-id="9819d-105">This provides a domain controller for use at branch offices where a full domain controller cannot be placed.</span></span> <span data-ttu-id="9819d-106">其目的是讓分公司的使用者登入，並執行諸如檔案/印表機共用的工作，即使沒有中樞網站的網路連線。</span><span class="sxs-lookup"><span data-stu-id="9819d-106">The intent is to allow users in the branch offices to logon and perform tasks like file/printer sharing even when there is no network connectivity to hub sites.</span></span>

<span data-ttu-id="9819d-107">RODC 不會變更架構的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9819d-107">RODC does not change the way schema is used.</span></span> <span data-ttu-id="9819d-108">不過，值得一提的是，架構支援 Read-Only 部分屬性集 (RO-PAS) ，也稱為 RODC 已篩選屬性集，這是基於安全性考慮而不會複寫至 Rodc 的特殊屬性集。</span><span class="sxs-lookup"><span data-stu-id="9819d-108">However, it is worthwhile to mention that the schema supports a Read-Only Partial Attribute Set (RO-PAS), also referred to as an RODC filtered attribute set, which is a special attribute set that is NOT replicated to RODCs for security reasons.</span></span> <span data-ttu-id="9819d-109">RO-PAS 會透過 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性在架構中定義。</span><span class="sxs-lookup"><span data-stu-id="9819d-109">RO-PAS are defined in the schema via the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span>

## <a name="rodc-filtered-attribute-set"></a><span data-ttu-id="9819d-110">RODC 已篩選屬性集</span><span class="sxs-lookup"><span data-stu-id="9819d-110">RODC filtered attribute set</span></span>

<span data-ttu-id="9819d-111">某些使用 [Active Directory Domain Services](active-directory-domain-services.md) 作為資料存放區的應用程式可能會有類似認證的資料 (例如密碼、認證或加密金鑰) 不應儲存在 Read-Only 網域控制站上的應用程式，以免 RODC 遭竊或遭到盜用。</span><span class="sxs-lookup"><span data-stu-id="9819d-111">Some applications that use [Active Directory Domain Services](active-directory-domain-services.md) as a data store may have credential-like data (such as passwords, credentials, or encryption keys) that should not be stored on a Read-Only Domain Controller in case the RODC is stolen or compromised.</span></span> <span data-ttu-id="9819d-112">對於這種類型的應用程式，您可以將屬性新增至 RODC 已篩選屬性集，以防止它複寫至樹系中的 Rodc，並將該屬性標示為機密，以移除讀取已驗證使用者群組成員之資料的能力 (包括任何 Rodc) 。</span><span class="sxs-lookup"><span data-stu-id="9819d-112">For this type of application, you can add the attribute to the RODC filtered attribute set to prevent it from replicating to RODCs in the forest, and mark the attribute as confidential, which removes the ability to read the data for members of the Authenticated Users group (including any RODCs).</span></span>

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a><span data-ttu-id="9819d-113">新增屬性至 RODC 已篩選屬性集</span><span class="sxs-lookup"><span data-stu-id="9819d-113">Adding attributes to the RODC filtered attribute set</span></span>

<span data-ttu-id="9819d-114">RODC 已篩選屬性集為動態屬性集，不會複寫至樹系中的任何 RODC。</span><span class="sxs-lookup"><span data-stu-id="9819d-114">The RODC filtered attribute set is a dynamic set of attributes that is not replicated to any RODCs in the forest.</span></span> <span data-ttu-id="9819d-115">您可以在執行 Windows Server 2008 的架構主機上設定 RODC 已篩選屬性集。</span><span class="sxs-lookup"><span data-stu-id="9819d-115">You can configure the RODC filtered attribute set on a schema master that runs Windows Server 2008.</span></span> <span data-ttu-id="9819d-116">當禁止將屬性複寫至 RODC 時，若 RODC 遭竊或被盜用，就可避免資料不慎外洩。</span><span class="sxs-lookup"><span data-stu-id="9819d-116">When the attributes are prevented from replicating to RODCs, that data cannot be exposed unnecessarily if an RODC is stolen or compromised.</span></span>

<span data-ttu-id="9819d-117">您無法將重要的系統屬性新增至 RODC 已篩選屬性集中。</span><span class="sxs-lookup"><span data-stu-id="9819d-117">You cannot add system-critical attributes to the RODC filtered attribute set.</span></span> <span data-ttu-id="9819d-118">AD DS、本機安全性授權單位 (LSA)、安全性帳戶管理員 (SAM)，以及任何 Microsoft 特定的安全性服務提供者 (例如，Kerberos 驗證通訊協定) 正常運作所需的屬性，即是重要系統屬性。</span><span class="sxs-lookup"><span data-stu-id="9819d-118">An attribute is system critical if it is required for AD DS, Local Security Authority (LSA), Security Accounts Manager (SAM), and any of Microsoft-specific Security Service Providers, such as the Kerberos authentication protocol, to function properly.</span></span> <span data-ttu-id="9819d-119">在 Beta 3 之後的 Windows Server 2008 版本中，系統關鍵屬性具有 (schemaFlagsEx 屬性值的 schemaFlagsEx 屬性值 & 0x1 = **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="9819d-119">In releases of Windows Server 2008 after Beta 3, a system-critical attribute has a schemaFlagsEx attribute value of (schemaFlagsEx attribute value & 0x1 = **TRUE**).</span></span>

<span data-ttu-id="9819d-120">如需將屬性新增至 RODC 已篩選屬性集的逐步指示，請參閱 [rodc 逐步指南的附錄 D]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="9819d-120">For step by step instructions to adding attributes to the RODC filtered attribute set, see [Appendix D of the step-by-step guide for RODCs]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).</span></span>

## <a name="marking-attributes-as-confidential"></a><span data-ttu-id="9819d-121">將屬性標示為機密</span><span class="sxs-lookup"><span data-stu-id="9819d-121">Marking attributes as confidential</span></span>

<span data-ttu-id="9819d-122">此外，設定為 RODC 已篩選屬性集之一部分的任何屬性，建議您也將其標示為機密。</span><span class="sxs-lookup"><span data-stu-id="9819d-122">In addition, it is recommended that you also mark as confidential any attributes that you configure as part of the RODC filtered attribute set.</span></span> <span data-ttu-id="9819d-123">若要將屬性標示為機密，必須移除 Authenticated Users 群組對於該屬性的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="9819d-123">To mark an attribute confidential, you have to remove the Read permission for the attribute for the Authenticated Users group.</span></span> <span data-ttu-id="9819d-124">將屬性標示為機密，可移除讀取類似認證的資料所需的權限。當 RODC 被盜用時，可提供額外的保護。</span><span class="sxs-lookup"><span data-stu-id="9819d-124">Marking the attribute as confidential provides an additional safeguard against an RODC that is compromised by removing the permissions that are necessary to read the credential-like data.</span></span> <span data-ttu-id="9819d-125">如需將屬性標示為機密的詳細資訊，請參閱 [Microsoft 知識庫中的文章 922836]( https://support.microsoft.com/kb/922836)。</span><span class="sxs-lookup"><span data-stu-id="9819d-125">For more information about marking attributes as confidential, see [article 922836 in the Microsoft Knowledge Base]( https://support.microsoft.com/kb/922836).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9819d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="9819d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9819d-127">唯讀網域控制站逐步指南</span><span class="sxs-lookup"><span data-stu-id="9819d-127">Step-by-Step Guide for Read-only Domain Controllers</span></span>]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 