---
description: 適用于應用程式開發 Windows 安全性軟體和安全軟體發展的應用程式安全性評定建議，包括應用程式安全性測試。
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: 安全性 Api 的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978142"
---
# <a name="best-practices-for-the-security-apis"></a><span data-ttu-id="5dc12-103">安全性 Api 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5dc12-103">Best Practices for the Security APIs</span></span>

<span data-ttu-id="5dc12-104">為了協助開發安全的軟體，我們建議您在開發應用程式時使用下列最佳作法。</span><span class="sxs-lookup"><span data-stu-id="5dc12-104">To help develop secure software, we recommend that you use the following best practices when developing applications.</span></span> <span data-ttu-id="5dc12-105">如需詳細資訊，請參閱 [安全性開發人員中心](https://msdn.microsoft.com/security/default.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5dc12-105">For more information, see [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).</span></span>

## <a name="security-development-life-cycle"></a><span data-ttu-id="5dc12-106">安全性開發生命週期</span><span class="sxs-lookup"><span data-stu-id="5dc12-106">Security Development Life Cycle</span></span>

<span data-ttu-id="5dc12-107"> (SDL) 的 [安全性開發生命週期](/previous-versions/ms995349(v=msdn.10)) ，是將一系列以安全性為焦點的活動和交付專案，與軟體發展的每個階段進行協調的流程。</span><span class="sxs-lookup"><span data-stu-id="5dc12-107">The [Security Development Life Cycle](/previous-versions/ms995349(v=msdn.10)) (SDL) is a process that aligns a series of security-focused activities and deliverables to each phase of software development.</span></span> <span data-ttu-id="5dc12-108">這些活動和交付專案包括：</span><span class="sxs-lookup"><span data-stu-id="5dc12-108">These activities and deliverables include:</span></span>

-   <span data-ttu-id="5dc12-109">開發威脅模型</span><span class="sxs-lookup"><span data-stu-id="5dc12-109">Developing threat models</span></span>
-   <span data-ttu-id="5dc12-110">使用程式碼掃描工具</span><span class="sxs-lookup"><span data-stu-id="5dc12-110">Using code-scanning tools</span></span>
-   <span data-ttu-id="5dc12-111">進行程式碼審核和安全性測試</span><span class="sxs-lookup"><span data-stu-id="5dc12-111">Conducting code reviews and security testing</span></span>

<span data-ttu-id="5dc12-112">如需 SDL 的詳細資訊，請參閱 [Sdl Blog](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5dc12-112">For more information about the SDL, see the [SDL Blog](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).</span></span>

## <a name="threat-models"></a><span data-ttu-id="5dc12-113">威脅模型</span><span class="sxs-lookup"><span data-stu-id="5dc12-113">Threat Models</span></span>

<span data-ttu-id="5dc12-114">進行威脅模型分析可協助您在程式碼中找出潛在的攻擊點。</span><span class="sxs-lookup"><span data-stu-id="5dc12-114">Conducting a threat model analysis can help you discover potential points of attack in your code.</span></span> <span data-ttu-id="5dc12-115">如需有關威脅模型分析的詳細資訊，請參閱 Howard、Michael 和 LeBlanc、David \[ 2003 \] 、 *撰寫安全* 的程式碼、2d ed、ISBN 0-7356-1722-8、Microsoft 按壓、Redmond、華盛頓州。</span><span class="sxs-lookup"><span data-stu-id="5dc12-115">For more information about threat model analysis, see Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span> <span data-ttu-id="5dc12-116"> (此資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="5dc12-116">(This resource may not be available in some languages and countries.)</span></span>

## <a name="service-packs-and-security-updates"></a><span data-ttu-id="5dc12-117">Service Pack 和安全性更新</span><span class="sxs-lookup"><span data-stu-id="5dc12-117">Service Packs and Security Updates</span></span>

<span data-ttu-id="5dc12-118">組建和測試環境應該鏡像相同的 service pack 層級和目標使用者群的安全性更新。</span><span class="sxs-lookup"><span data-stu-id="5dc12-118">Build and test environments should mirror the same levels of service packs and security updates of the targeted user base.</span></span> <span data-ttu-id="5dc12-119">建議您為任何屬於組建和測試環境的 Microsoft 平臺或應用程式安裝最新的 service pack 和安全性更新，並鼓勵您的使用者針對完成的應用程式環境進行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="5dc12-119">We recommend that you install the latest service packs and security updates for any Microsoft platform or application that is part of your build and test environment and encourage your users to do the same for the finished application environment.</span></span> <span data-ttu-id="5dc12-120">如需有關 service pack 和安全性更新的詳細資訊，請參閱 [microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) 和 [microsoft 安全性](https://www.microsoft.com/security)。</span><span class="sxs-lookup"><span data-stu-id="5dc12-120">For more information about service packs and security updates, see [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) and [Microsoft Security](https://www.microsoft.com/security).</span></span>

## <a name="authorization"></a><span data-ttu-id="5dc12-121">授權</span><span class="sxs-lookup"><span data-stu-id="5dc12-121">Authorization</span></span>

<span data-ttu-id="5dc12-122">您應建立需要最低可能許可權的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5dc12-122">You should create applications that require the least possible privilege.</span></span> <span data-ttu-id="5dc12-123">使用最低許可權可能會降低惡意程式碼危害電腦系統的風險。</span><span class="sxs-lookup"><span data-stu-id="5dc12-123">Using the least possible privilege reduces the risk of malicious code compromising your computer system.</span></span> <span data-ttu-id="5dc12-124">如需在最低可能許可權層級中執行程式碼的詳細資訊，請參閱 [以特殊許可權](running-with-special-privileges.md)執行。</span><span class="sxs-lookup"><span data-stu-id="5dc12-124">For more information about running code in least possible privilege level, see [Running with Special Privileges](running-with-special-privileges.md).</span></span>

## <a name="more-information"></a><span data-ttu-id="5dc12-125">相關資訊</span><span class="sxs-lookup"><span data-stu-id="5dc12-125">More Information</span></span>

<span data-ttu-id="5dc12-126">如需最佳作法的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="5dc12-126">For more information about best practices, see the following topics.</span></span>



| <span data-ttu-id="5dc12-127">主題</span><span class="sxs-lookup"><span data-stu-id="5dc12-127">Topic</span></span>                                                                                                                        | <span data-ttu-id="5dc12-128">描述</span><span class="sxs-lookup"><span data-stu-id="5dc12-128">Description</span></span>                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dc12-129">以特殊許可權執行</span><span class="sxs-lookup"><span data-stu-id="5dc12-129">Running with Special Privileges</span></span>](running-with-special-privileges.md)<br/>                                            | <span data-ttu-id="5dc12-130">討論權限的安全性含意。</span><span class="sxs-lookup"><span data-stu-id="5dc12-130">Discusses security implications of privileges.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="5dc12-131">避免緩衝區溢位</span><span class="sxs-lookup"><span data-stu-id="5dc12-131">Avoiding Buffer Overruns</span></span>](avoiding-buffer-overruns.md)<br/>                                                          | <span data-ttu-id="5dc12-132">提供有關避免緩衝區溢位的資訊。</span><span class="sxs-lookup"><span data-stu-id="5dc12-132">Provides information about avoiding buffer overruns.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="5dc12-133">控制流程防護 (CFG) </span><span class="sxs-lookup"><span data-stu-id="5dc12-133">Control Flow Guard (CFG)</span></span>](control-flow-guard.md)<br/>                                                                | <span data-ttu-id="5dc12-134">討論記憶體損毀弱點。</span><span class="sxs-lookup"><span data-stu-id="5dc12-134">Discusses memory corruption vulnerabilities.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="5dc12-135">建立 DACL</span><span class="sxs-lookup"><span data-stu-id="5dc12-135">Creating a DACL</span></span>](creating-a-dacl.md)<br/>                                                                            | <span data-ttu-id="5dc12-136">說明如何使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) ，建立任意的存取控制清單 (DACL) 。</span><span class="sxs-lookup"><span data-stu-id="5dc12-136">Shows how to create a discretionary access control list (DACL) by using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span><br/> |
| [<span data-ttu-id="5dc12-137">處理密碼</span><span class="sxs-lookup"><span data-stu-id="5dc12-137">Handling Passwords</span></span>](handling-passwords.md)<br/>                                                                      | <span data-ttu-id="5dc12-138">討論使用密碼的安全性含意。</span><span class="sxs-lookup"><span data-stu-id="5dc12-138">Discusses security implications of using passwords.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="5dc12-139">如何優化您的 MSDN Library 搜尋</span><span class="sxs-lookup"><span data-stu-id="5dc12-139">How to Optimize Your MSDN Library Search</span></span>](how-to-optimize-your-msdn-library-search.md)<br/>                          | <span data-ttu-id="5dc12-140">討論在 MSDN Library 上搜尋安全性 SDK 內容的選項。</span><span class="sxs-lookup"><span data-stu-id="5dc12-140">Discusses options for searching Security SDK content on MSDN Library.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="5dc12-141">動態存取控制開發人員擴充性</span><span class="sxs-lookup"><span data-stu-id="5dc12-141">Dynamic Access Control developer extensibility</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | <span data-ttu-id="5dc12-142">適用于新動態存取控制解決方案的一些開發人員擴充性點的基本導向。</span><span class="sxs-lookup"><span data-stu-id="5dc12-142">Basic orientation to some of the developer extensibility points for the new Dynamic Access Control solutions.</span></span><br/>                                                                   |



 

 

