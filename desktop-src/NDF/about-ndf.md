---
title: 關於 NDF
description: 網路診斷架構 (NDF) 會在網路系統管理員和電腦使用者發生時處理常見的網路問題，藉此減少其介入。
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672727"
---
# <a name="about-ndf"></a><span data-ttu-id="701a5-103">關於 NDF</span><span class="sxs-lookup"><span data-stu-id="701a5-103">About NDF</span></span>

<span data-ttu-id="701a5-104">網路診斷架構 (NDF) 會在網路系統管理員和電腦使用者發生時處理常見的網路問題，藉此減少其介入。</span><span class="sxs-lookup"><span data-stu-id="701a5-104">The Network Diagnostics Framework (NDF) reduces the involvement of network administrators and computer users by handling common network issues as they occur.</span></span> <span data-ttu-id="701a5-105">使用 NDF 的診斷和修復功能，使用者和系統管理員就不需要額外的工具，就能處理一些相當常見的問題。</span><span class="sxs-lookup"><span data-stu-id="701a5-105">By using NDF's diagnostic and repair capabilities, users and administrators do not need additional tools in order to handle some relatively common problems.</span></span> <span data-ttu-id="701a5-106">NDF 隨附于 Windows Vista、Windows Server 2008 和更新版本中。</span><span class="sxs-lookup"><span data-stu-id="701a5-106">NDF ships as part of Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="701a5-107">當系統開機 (但無法在安全模式中執行時，就可以使用此功能) 。</span><span class="sxs-lookup"><span data-stu-id="701a5-107">It is available whenever a system is booted (but cannot run in Safe Mode).</span></span>

## <a name="ndf-helper-classes"></a><span data-ttu-id="701a5-108">NDF Helper 類別</span><span class="sxs-lookup"><span data-stu-id="701a5-108">NDF Helper Classes</span></span>

<span data-ttu-id="701a5-109">NDF 包含協助程式類別，可在發生網路問題時進行診斷。</span><span class="sxs-lookup"><span data-stu-id="701a5-109">NDF includes helper classes that diagnose networking issues as they occur.</span></span> <span data-ttu-id="701a5-110">這些協助程式類別都包含至少一個元件或應用程式的疑難排解所需的邏輯。</span><span class="sxs-lookup"><span data-stu-id="701a5-110">Each of these helper classes contains the logic required to troubleshoot at least one component or application.</span></span>

<span data-ttu-id="701a5-111">個別的 NDF helper 類別會執行診斷會話的主要工作。</span><span class="sxs-lookup"><span data-stu-id="701a5-111">Individual NDF helper classes perform the primary tasks of the diagnostics session.</span></span> <span data-ttu-id="701a5-112">每個 helper 類別都是一種程式碼單位，其設計目的是要評估其各自網路元件的某個健全狀況。</span><span class="sxs-lookup"><span data-stu-id="701a5-112">Each helper class is a unit of code designed to evaluate one health aspect of its respective network component.</span></span> <span data-ttu-id="701a5-113">Helper 類別也瞭解有哪些可用的修復選項可用來還原元件的健全狀況，以及任何特定修復選項的成本和風險。</span><span class="sxs-lookup"><span data-stu-id="701a5-113">The helper class also understands what possible repair options are available to restore the health of the component, as well as the cost and risk of any particular repair option.</span></span>

<span data-ttu-id="701a5-114">每個 helper 類別都會插入整體網路診斷架構中。</span><span class="sxs-lookup"><span data-stu-id="701a5-114">Each helper class plugs into the overall Network Diagnostics Framework.</span></span> <span data-ttu-id="701a5-115">如果協力廠商網路元件包含 NDF 協助程式類別，則使用 NDF 的其他應用程式可以解析該元件的問題，而不需要他們擁有該元件的任何特定知識。</span><span class="sxs-lookup"><span data-stu-id="701a5-115">If a third-party network component includes an NDF helper class, problems with that component can be resolved by other applications using NDF, without requiring them to have any specific knowledge of that component.</span></span>

<span data-ttu-id="701a5-116">由 Microsoft 開發的協助程式類別可為軟體發展人員提供主要的診斷和修復功能。</span><span class="sxs-lookup"><span data-stu-id="701a5-116">The helper classes developed by Microsoft provide software developers with the primary diagnostic and repair functionality.</span></span> <span data-ttu-id="701a5-117">另外還有一組小型的 Api 可讓開發人員用來診斷使用 NDF 的網路問題。</span><span class="sxs-lookup"><span data-stu-id="701a5-117">There is also a small set of APIs that developers can use to diagnose network problems using NDF.</span></span> <span data-ttu-id="701a5-118">如需詳細資訊，請參閱 [Ndf 功能](ndf-functions.md) 和 [ndf 診斷範例](ndf-diagnostics-example.md)。</span><span class="sxs-lookup"><span data-stu-id="701a5-118">For more information, see [NDF Functions](ndf-functions.md) and [NDF Diagnostics Example](ndf-diagnostics-example.md).</span></span>

## <a name="extensible-helper-classes"></a><span data-ttu-id="701a5-119">可擴充的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="701a5-119">Extensible Helper Classes</span></span>

<span data-ttu-id="701a5-120">在某些情況下，應用程式開發人員可以提供更具體的診斷和修復功能。</span><span class="sxs-lookup"><span data-stu-id="701a5-120">In some cases, more specific diagnostic and repair functionality can be provided by application developers.</span></span>

<span data-ttu-id="701a5-121">某些 Microsoft 的 NDF 協助程式類別是設計來擴充，以提供額外的診斷和修復功能。</span><span class="sxs-lookup"><span data-stu-id="701a5-121">Some of Microsoft's NDF helper classes are designed to be extended to provide additional diagnostic and repair capabilities.</span></span> <span data-ttu-id="701a5-122">這表示開發人員可以包含使用 NDF 診斷和修復功能的功能，來疑難排解其軟體或硬體特有的問題。</span><span class="sxs-lookup"><span data-stu-id="701a5-122">This means that developers can include functionality to use NDF diagnostic and repair capabilities to troubleshoot issues specific to their software or hardware.</span></span>

<span data-ttu-id="701a5-123">例如，Microsoft 的無線團隊提供可延伸的協助程式類別，可讓任何協力廠商無線廠商為其特定硬體和/或軟體新增特定的疑難排解邏輯。</span><span class="sxs-lookup"><span data-stu-id="701a5-123">For example, the wireless team at Microsoft provides an extensible helper class that allows any third party wireless vendors to add specific troubleshooting logic for their specific hardware and/or software.</span></span> <span data-ttu-id="701a5-124">他們可以藉由開發 NDF 協助程式類別延伸來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="701a5-124">They can do this by developing an NDF helper class extension.</span></span> <span data-ttu-id="701a5-125">如需詳細資訊，請參閱 [802.11 無線診斷可延伸 Helper 類別](802-11-wireless-diagnostics-extensible-helper-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="701a5-125">For more information, see [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).</span></span>

<span data-ttu-id="701a5-126">根據定義，NDF 協助程式類別延伸會擴充現有可延伸 helper 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="701a5-126">An NDF helper class extension, by definition, extends the functionality of an existing extensible helper class.</span></span> <span data-ttu-id="701a5-127">如果協助程式類別不可延伸，則無法為該 helper 類別撰寫延伸模組。</span><span class="sxs-lookup"><span data-stu-id="701a5-127">If a helper class is not extensible, no one can write an extension for that helper class.</span></span>

## <a name="benefits-of-helper-class-extensions"></a><span data-ttu-id="701a5-128">Helper 類別擴充功能的優點</span><span class="sxs-lookup"><span data-stu-id="701a5-128">Benefits of Helper Class Extensions</span></span>

<span data-ttu-id="701a5-129">NDF 提供數個獨特的優點，以鼓勵網路元件開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="701a5-129">NDF offers several distinct advantages to encourage its use by network component developers.</span></span> <span data-ttu-id="701a5-130">清單頂端是廠商軟體的客戶將會釋出一些自己的疑難排解資源，並降低擁有權總成本。</span><span class="sxs-lookup"><span data-stu-id="701a5-130">At the top of the list is that customers of vendor software will free up some of their own troubleshooting resources and reduce the total cost of ownership.</span></span> <span data-ttu-id="701a5-131">妥善撰寫的 helper 類別延伸也提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="701a5-131">A well-written helper class extension also provides the following benefits:</span></span>

-   <span data-ttu-id="701a5-132">可讓小組判斷其元件是否不是連線問題的原因。</span><span class="sxs-lookup"><span data-stu-id="701a5-132">Allows a team to determine when their component is not the cause of a connectivity issue.</span></span> <span data-ttu-id="701a5-133">例如，網路功能通常是針對連線問題所應該過度，而這些問題實際上不是網路元件失敗的結果。</span><span class="sxs-lookup"><span data-stu-id="701a5-133">For example, networking is often blamed for connectivity problems that are not actually the result of a networking component failure.</span></span> <span data-ttu-id="701a5-134">藉由撰寫協助程式類別擴充功能，小組可以更輕鬆地排除特定的元件，使其成為連線失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="701a5-134">By writing a helper class extension, a team can more easily rule out a particular component as the cause of a connectivity failure.</span></span>
-   <span data-ttu-id="701a5-135">可讓小組快速診斷和偵測元件中的問題。</span><span class="sxs-lookup"><span data-stu-id="701a5-135">Allows a team to quickly diagnose and debug a problem within the component.</span></span> <span data-ttu-id="701a5-136">如果有協助程式類別被撰寫來執行所有必要的標準診斷步驟，則可以刪除花在偵錯工具和疑難排解的時間。</span><span class="sxs-lookup"><span data-stu-id="701a5-136">Time spent debugging and troubleshooting can be eliminated if a helper class is written to perform all of the standard diagnostic steps that would be required anyway.</span></span>
-   <span data-ttu-id="701a5-137">免除撰寫和支援一次性工具以診斷問題的需求。</span><span class="sxs-lookup"><span data-stu-id="701a5-137">Eliminates the need to write and support one-off tools to diagnose problems.</span></span> <span data-ttu-id="701a5-138">Helper 類別可以是元件診斷功能和資訊收集技術的中央存放庫。</span><span class="sxs-lookup"><span data-stu-id="701a5-138">A helper class can be the central repository for a component's diagnostic capabilities and information gathering techniques.</span></span>
-   <span data-ttu-id="701a5-139">讓應用程式可以使用元件專屬的診斷功能，而不需要他們直接瞭解元件。</span><span class="sxs-lookup"><span data-stu-id="701a5-139">Makes component-specific diagnostics available to applications, without requiring them to have any direct knowledge about the component.</span></span>

 

 




