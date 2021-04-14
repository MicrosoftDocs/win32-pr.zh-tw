---
description: 下列詞彙描述存在於遠端系統上的網域。
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: 主要和受信任的網域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511168"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="fa566-103">主要和受信任的網域</span><span class="sxs-lookup"><span data-stu-id="fa566-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="fa566-104">下列詞彙描述存在於遠端系統上的網域。</span><span class="sxs-lookup"><span data-stu-id="fa566-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="fa566-105">主要網域</span><span class="sxs-lookup"><span data-stu-id="fa566-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="fa566-106">受信任的網域</span><span class="sxs-lookup"><span data-stu-id="fa566-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="fa566-107">主要網域</span><span class="sxs-lookup"><span data-stu-id="fa566-107">Primary Domain</span></span>

<span data-ttu-id="fa566-108">主域是負責建立進一步信任關係和執行驗證 (，或將驗證要求傳遞至適當受信任網域) 的網域。</span><span class="sxs-lookup"><span data-stu-id="fa566-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="fa566-109">主網域中的網域控制站會處理或傳遞源自工作站的驗證要求。</span><span class="sxs-lookup"><span data-stu-id="fa566-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="fa566-110">當登入發生時，LSA 會檢查內建帳戶網域的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="fa566-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="fa566-111">如果要登入的帳戶不在這兩個網域中，則會將登入要求交給系統的主要網域。</span><span class="sxs-lookup"><span data-stu-id="fa566-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="fa566-112">受信任的網域</span><span class="sxs-lookup"><span data-stu-id="fa566-112">Trusted Domain</span></span>

<span data-ttu-id="fa566-113">受信任的網域是本機系統信任以驗證使用者的網域。</span><span class="sxs-lookup"><span data-stu-id="fa566-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="fa566-114">換句話說，如果使用者或應用程式是由受信任的網域驗證，則信任驗證網域的所有網域都會接受此驗證。</span><span class="sxs-lookup"><span data-stu-id="fa566-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="fa566-115">每個次級網域都會自動與主要網域有雙向信任關係。</span><span class="sxs-lookup"><span data-stu-id="fa566-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="fa566-116">根據預設，此信任是可轉移的，也就是說，如果系統信任網域 A，它也會信任網域 A 所信任的所有網域。</span><span class="sxs-lookup"><span data-stu-id="fa566-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="fa566-117">Windows 2000 之前的作業系統也支援單向信任，而不支援可轉移的雙向信任。</span><span class="sxs-lookup"><span data-stu-id="fa566-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="fa566-118"> (LSA) 的「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」具有物件類型 [**TrustedDomain**](the-trusteddomain-object-type.md)，可用來儲存信任關係的相關資訊，包括受信任網域的名稱和 [*安全性識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 、用於驗證要求的網域帳戶、名稱和 SID 轉譯要求，以及受信任網域中網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa566-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="fa566-119">在網域控制站上，LSA 會為本機系統所信任的每個網域建立 [**TrustedDomain**](the-trusteddomain-object-type.md) 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="fa566-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="fa566-120">例如，如果 Windows XP 工作站信任 Windows 2000 網域控制站，而該控制器接著信任其他四個系統，則使用可轉移信任連線的工作站在其本機系統上將會有五個 [**TrustedDomain**](the-trusteddomain-object-type.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fa566-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 
