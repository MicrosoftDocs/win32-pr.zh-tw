---
title: 設計 NDF Helper 類別延伸模組
description: 本主題的目的是要透過 helper 類別擴充程式開發程式來提供一般的指引。
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932091"
---
# <a name="designing-ndf-helper-class-extensions"></a><span data-ttu-id="22a7b-103">設計 NDF Helper 類別延伸模組</span><span class="sxs-lookup"><span data-stu-id="22a7b-103">Designing NDF Helper Class Extensions</span></span>

<span data-ttu-id="22a7b-104">本主題的目的是要透過 helper 類別擴充程式開發程式來提供一般的指引。</span><span class="sxs-lookup"><span data-stu-id="22a7b-104">This topic is intended to provide generic guidance through the helper class extension development process.</span></span> <span data-ttu-id="22a7b-105">本主題中的指導方針適用于所有 helper 類別的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="22a7b-105">The guidance in this topic applies to all helper class extensions.</span></span> <span data-ttu-id="22a7b-106">如需更具體的指引，請參閱 [Windows 篩選平台](windows-filtering-platform-extensible-helper-class.md) 可延伸協助程式類別和 [802.11 無線診斷](802-11-wireless-diagnostics-extensible-helper-classes.md)可延伸協助程式類別。</span><span class="sxs-lookup"><span data-stu-id="22a7b-106">For more specific guidance, see [Windows Filtering Platform Extensible Helper Class](windows-filtering-platform-extensible-helper-class.md) and [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).</span></span>

## <a name="extending-ndf-functionality"></a><span data-ttu-id="22a7b-107">擴充 NDF 功能</span><span class="sxs-lookup"><span data-stu-id="22a7b-107">Extending NDF Functionality</span></span>

<span data-ttu-id="22a7b-108">Windows Vista 和更新版本隨附的各種協助程式類別，可診斷和修復各式各樣的問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-108">Windows Vista and later versions ship with a variety of helper classes already implemented that can diagnose and repair a wide range of issues.</span></span> <span data-ttu-id="22a7b-109">但有時候，協力廠商開發人員可能會想要擴充這些協助程式類別，以診斷並解決其特定產品和執行的特定問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-109">At times, however, third-party developers may wish to extend these helper classes to diagnose and resolve issues specific to their particular products and implementations.</span></span>

<span data-ttu-id="22a7b-110">下列 Microsoft NDF 協助程式類別是可擴充的。</span><span class="sxs-lookup"><span data-stu-id="22a7b-110">The following Microsoft NDF helper classes are extensible.</span></span>

-   [<span data-ttu-id="22a7b-111">Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="22a7b-111">Windows Filtering Platform</span></span>](windows-filtering-platform-extensible-helper-class.md)
-   [<span data-ttu-id="22a7b-112">無線安全性</span><span class="sxs-lookup"><span data-stu-id="22a7b-112">Wireless Security</span></span>](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a><span data-ttu-id="22a7b-113">執行 Helper 類別延伸模組</span><span class="sxs-lookup"><span data-stu-id="22a7b-113">Implementing a Helper Class Extension</span></span>

<span data-ttu-id="22a7b-114">Microsoft 發行了兩個介面，可用來開發 NDF 協助程式類別延伸模組。</span><span class="sxs-lookup"><span data-stu-id="22a7b-114">Microsoft ships two interfaces that can be used to develop NDF helper class extensions.</span></span>

<span data-ttu-id="22a7b-115">NDF 會呼叫 [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) 介面，以驗證它是否有所有必要的資訊，以及它是否已選擇正確的 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="22a7b-115">The [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface is called by NDF to validate that it has all required information and that it has chosen the correct helper class.</span></span> <span data-ttu-id="22a7b-116">它是透過 [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="22a7b-116">It accomplishes this through the [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) method.</span></span>

<span data-ttu-id="22a7b-117">NDF 會針對診斷程式期間發生的大部分活動呼叫 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) 介面。</span><span class="sxs-lookup"><span data-stu-id="22a7b-117">The [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface is called by NDF for most of the activities that occur during the diagnostic procedure.</span></span> <span data-ttu-id="22a7b-118">其中有幾個方法是必要的，但有些是選擇性的，而不是特定用途。</span><span class="sxs-lookup"><span data-stu-id="22a7b-118">Several of its methods are required, but others are optional for specific uses.</span></span>

<span data-ttu-id="22a7b-119">必要的方法包括 [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) 和 [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo)。</span><span class="sxs-lookup"><span data-stu-id="22a7b-119">The required methods include [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) and [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo).</span></span> <span data-ttu-id="22a7b-120">NDF 呼叫 **initialize** 以將金鑰參數傳送給 helper 類別延伸模組，以將其實例狀態初始化。</span><span class="sxs-lookup"><span data-stu-id="22a7b-120">NDF calls **Initialize** to send key parameters to the helper class extension to initialize its instance state.</span></span> <span data-ttu-id="22a7b-121">**GetDiagnosticsInfo** 可預估診斷可能花費的時間，以及是否需要模擬原始的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="22a7b-121">**GetDiagnosticsInfo** provides an estimate of how long the diagnosis may take and whether it requires impersonation of the original user context.</span></span>

<span data-ttu-id="22a7b-122">另一個方法 [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)則是呼叫，以在與 helper 類別對應的網路元件上執行診斷。</span><span class="sxs-lookup"><span data-stu-id="22a7b-122">Another method, [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), is called to perform diagnosis on the network component corresponding to the helper class.</span></span> <span data-ttu-id="22a7b-123">當 NDF 判斷正在進行的診斷或修復應停止時，就會呼叫 [**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) 。</span><span class="sxs-lookup"><span data-stu-id="22a7b-123">[**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) is called when NDF determines an ongoing diagnosis or repair should be stopped.</span></span> <span data-ttu-id="22a7b-124">[**清除**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) 作業可讓 ndf 釋放 helper 類別延伸模組在呼叫 [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) 之後所使用的 ndf 資源。</span><span class="sxs-lookup"><span data-stu-id="22a7b-124">[**Cleanup**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) allows NDF to release NDF resources that the helper class extension has used since the call to [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) was made.</span></span>

<span data-ttu-id="22a7b-125">如需其他方法的詳細資訊，請參閱 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)。</span><span class="sxs-lookup"><span data-stu-id="22a7b-125">For information on additional methods, see [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).</span></span>

<span data-ttu-id="22a7b-126">NDF 協助程式類別延伸模組是用來診斷和解決與特定應用程式或元件相關聯的連線問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-126">NDF helper class extensions are used to diagnose and resolve connectivity problems associated with a specific application or component.</span></span> <span data-ttu-id="22a7b-127">它們也會驗證解決嘗試的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="22a7b-127">They also validate the success or failure of a resolution attempt.</span></span>

<span data-ttu-id="22a7b-128">考慮使用 helper 類別延伸模組的開發人員應該執行下列工作。</span><span class="sxs-lookup"><span data-stu-id="22a7b-128">Developers considering the implementation of a helper class extension should perform the following tasks.</span></span>

-   <span data-ttu-id="22a7b-129">識別診斷和修復動作很有用的使用者案例。</span><span class="sxs-lookup"><span data-stu-id="22a7b-129">Identify user scenarios in which diagnostic and repair actions are helpful.</span></span>
-   <span data-ttu-id="22a7b-130">提供通常發生連線問題的解決方式。</span><span class="sxs-lookup"><span data-stu-id="22a7b-130">Provide resolutions to frequently encountered connectivity problems.</span></span>
-   <span data-ttu-id="22a7b-131">如果需要協助程式類別延伸，請在 NDF 中定義用來代表元件健康情況狀態的元件健全狀況模型。</span><span class="sxs-lookup"><span data-stu-id="22a7b-131">If a helper class extension is required, define a component health model used to represent the component's health state in NDF.</span></span>

## <a name="identify-user-scenarios"></a><span data-ttu-id="22a7b-132">識別使用者案例</span><span class="sxs-lookup"><span data-stu-id="22a7b-132">Identify User Scenarios</span></span>

<span data-ttu-id="22a7b-133">測試和使用應用程式可能已經提供協助程式類別延伸模組可能會診斷並可能修復的明顯模式。</span><span class="sxs-lookup"><span data-stu-id="22a7b-133">Testing and use of an application may have already provided discernable patterns that a helper class extension may be able to diagnose and possibly repair.</span></span> <span data-ttu-id="22a7b-134">應用程式開發人員可以使用這項資料來判斷最重要的連線問題，並找出可能發生連線問題的使用者案例。</span><span class="sxs-lookup"><span data-stu-id="22a7b-134">Application developers can use this data to determine the most important connectivity issues to address and to identify the user scenarios in which connectivity issues are likely to occur.</span></span>

<span data-ttu-id="22a7b-135">判斷每個問題的根本原因對於這部分的程式來說很重要。</span><span class="sxs-lookup"><span data-stu-id="22a7b-135">Determining the root cause of each problem is vital in this part of the process.</span></span> <span data-ttu-id="22a7b-136">這可能需要廣泛的研究，但將有助於建立更容易使用者和系統管理員使用的軟體。</span><span class="sxs-lookup"><span data-stu-id="22a7b-136">This may require extensive research, but will help create software that is far easier for users and administrators to use.</span></span> <span data-ttu-id="22a7b-137">如果找不到根本原因，則會變得很難或無法使用 helper 類別延伸來提供問題解決方式。</span><span class="sxs-lookup"><span data-stu-id="22a7b-137">If a root cause is not identified, it becomes difficult or impossible to offer problem resolution using the helper class extension.</span></span>

## <a name="provide-resolutions"></a><span data-ttu-id="22a7b-138">提供解決方案</span><span class="sxs-lookup"><span data-stu-id="22a7b-138">Provide Resolutions</span></span>

<span data-ttu-id="22a7b-139">在開發小組找出與軟體相關之問題的根本原因之後，下一步就是找出適當的解決措施，協助使用者盡可能有效率地解決問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-139">After a development team has identified the root causes of problems associated with their software, the next step is to identify the appropriate resolution actions for helping the user solve the problem as efficiently as possible.</span></span>

<span data-ttu-id="22a7b-140">並非所有的解決方案都需要協助程式類別延伸或自動執行的動作。</span><span class="sxs-lookup"><span data-stu-id="22a7b-140">Not all resolutions require that a helper class extension or automated action be created.</span></span> <span data-ttu-id="22a7b-141">在某些情況下，小組可能會判斷解決根本原因的最佳方法是修正或更新元件、提供元件的其他說明內容，或開發提供更佳長期解決方案的其他策略。</span><span class="sxs-lookup"><span data-stu-id="22a7b-141">In some cases, the team may determine that the best approach to resolving a root cause is to fix or update the component, provide additional help content for the component, or develop other strategies that provide better long-term solutions.</span></span>

<span data-ttu-id="22a7b-142">針對自動化動作很理想的問題，建立 NDF 協助程式類別延伸通常是絕佳的解決方案。</span><span class="sxs-lookup"><span data-stu-id="22a7b-142">For problems in which an automated action is ideal, creating an NDF helper class extension is often an excellent solution.</span></span>

<span data-ttu-id="22a7b-143">Helper 類別延伸會將根本原因和修復資訊的相關資訊傳回給使用者。</span><span class="sxs-lookup"><span data-stu-id="22a7b-143">Helper class extensions return information about root causes and repair information to users through NDF.</span></span> <span data-ttu-id="22a7b-144">用來描述根本原因和修復資訊的字串，對於非技術使用者來說，必須簡單且容易瞭解。</span><span class="sxs-lookup"><span data-stu-id="22a7b-144">The strings used to describe the root causes and repair information must be simple and easy for a non-technical user to understand.</span></span> <span data-ttu-id="22a7b-145">如需這些字串的詳細資訊，請參閱 [NDF 協助程式類別延伸消費者介面指導方針](user-interface-guidelines-for-ndf-helper-class-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="22a7b-145">For more information on these strings, see [User Interface Guidelines for NDF Helper Class Extensions](user-interface-guidelines-for-ndf-helper-class-extensions.md).</span></span>

## <a name="define-a-component-health-model"></a><span data-ttu-id="22a7b-146">定義元件健全狀況模型</span><span class="sxs-lookup"><span data-stu-id="22a7b-146">Define a Component Health Model</span></span>

<span data-ttu-id="22a7b-147">軟體發展人員應定義與網路問題管理能力相關聯的「健全狀況」等級。</span><span class="sxs-lookup"><span data-stu-id="22a7b-147">Software developers should define levels of "health" associated with the manageability of networking problems.</span></span> <span data-ttu-id="22a7b-148">用來開發 helper 類別的健康情況模型只會定義兩個層級的健全狀況：狀況良好和狀況不良。</span><span class="sxs-lookup"><span data-stu-id="22a7b-148">A health model used to develop helper classes defines just two levels of health: healthy and unhealthy.</span></span> <span data-ttu-id="22a7b-149">這些層級也可以套用至 NDF 協助程式類別延伸。</span><span class="sxs-lookup"><span data-stu-id="22a7b-149">These levels can also be applied to NDF helper class extensions.</span></span>

<span data-ttu-id="22a7b-150">狀況良好的元件表示沒有問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-150">A healthy component indicates an absence of problems.</span></span> <span data-ttu-id="22a7b-151">元件可能因為其本身的問題而被視為狀況不良，或因為相依的其他元件發生問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-151">A component can be considered unhealthy because of its own problems, or because of problems occurring in other components on which it depends.</span></span>



| <span data-ttu-id="22a7b-152">詞彙</span><span class="sxs-lookup"><span data-stu-id="22a7b-152">Term</span></span>                                                                                                                             | <span data-ttu-id="22a7b-153">描述</span><span class="sxs-lookup"><span data-stu-id="22a7b-153">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a7b-154"><span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth</span><span class="sxs-lookup"><span data-stu-id="22a7b-154"><span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth</span></span><br/>                         | <span data-ttu-id="22a7b-155">此狀態表示此元件無法接受的失敗層級，以及元件是否為問題。</span><span class="sxs-lookup"><span data-stu-id="22a7b-155">This state indicates an unacceptable level of failures from this component, and that the component is the problem.</span></span><br/>    |
| <span data-ttu-id="22a7b-156"><span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth 如下</span><span class="sxs-lookup"><span data-stu-id="22a7b-156"><span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth Below</span></span><br/> | <span data-ttu-id="22a7b-157">此狀態表示此元件相依的本機電腦群組件無法接受的失敗層級。</span><span class="sxs-lookup"><span data-stu-id="22a7b-157">This state indicates an unacceptable level of failures from a local machine component that this component depends on.</span></span><br/> |



 

<span data-ttu-id="22a7b-158">使用 NDF 進行診斷時，系統會詢問協助程式類別延伸系列的問題，以判斷其健康狀態的狀態。</span><span class="sxs-lookup"><span data-stu-id="22a7b-158">When diagnosis takes place using NDF, the helper class extension is asked a series of questions to determine its state of health.</span></span> <span data-ttu-id="22a7b-159">如果延伸模組回應狀況不良，則 NDF 會詢問問題、嘗試診斷問題、其位置，以及下一步的外觀。</span><span class="sxs-lookup"><span data-stu-id="22a7b-159">If the extension responds that it is unhealthy, NDF asks clarifying questions, trying to diagnose the problem, its location, and where to look next.</span></span> <span data-ttu-id="22a7b-160">每個協助程式類別都必須能夠回答低健康情況的問題，才能更妥善地導向適當的診斷活動。</span><span class="sxs-lookup"><span data-stu-id="22a7b-160">Each helper class must be able to answer the question of low health in order to better direct appropriate diagnostic activities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22a7b-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="22a7b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22a7b-162">Windows 篩選平台可擴充 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="22a7b-162">Windows Filtering Platform Extensible Helper Class</span></span>](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[<span data-ttu-id="22a7b-163">802.11 無線診斷可延伸的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="22a7b-163">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





