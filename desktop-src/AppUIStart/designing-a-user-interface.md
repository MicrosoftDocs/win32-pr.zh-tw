---
title: 設計消費者介面
description: 本節詳細說明一些與設計 Windows 應用程式之 UI 相關聯的工作。
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463452"
---
# <a name="designing-a-user-interface"></a><span data-ttu-id="2b489-103">設計消費者介面</span><span class="sxs-lookup"><span data-stu-id="2b489-103">Designing a User Interface</span></span>

<span data-ttu-id="2b489-104">本節詳細說明一些與設計 Windows 應用程式之 UI 相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="2b489-104">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span>

-   [<span data-ttu-id="2b489-105">簡介</span><span class="sxs-lookup"><span data-stu-id="2b489-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2b489-106">功能需求</span><span class="sxs-lookup"><span data-stu-id="2b489-106">Functional Requirements</span></span>](#functional-requirements)
-   [<span data-ttu-id="2b489-107">使用者分析</span><span class="sxs-lookup"><span data-stu-id="2b489-107">User Analysis</span></span>](#user-analysis)
    -   [<span data-ttu-id="2b489-108">問題陳述</span><span class="sxs-lookup"><span data-stu-id="2b489-108">Problem Statements</span></span>](#problem-statements)
    -   [<span data-ttu-id="2b489-109">優先 級</span><span class="sxs-lookup"><span data-stu-id="2b489-109">Priorities</span></span>](#priorities)
-   [<span data-ttu-id="2b489-110">概念設計</span><span class="sxs-lookup"><span data-stu-id="2b489-110">Conceptual Design</span></span>](#conceptual-design)
-   [<span data-ttu-id="2b489-111">邏輯設計</span><span class="sxs-lookup"><span data-stu-id="2b489-111">Logical Design</span></span>](#logical-design)
-   [<span data-ttu-id="2b489-112">實體設計</span><span class="sxs-lookup"><span data-stu-id="2b489-112">Physical Design</span></span>](#physical-design)

## <a name="introduction"></a><span data-ttu-id="2b489-113">簡介</span><span class="sxs-lookup"><span data-stu-id="2b489-113">Introduction</span></span>

<span data-ttu-id="2b489-114">UI 設計可以分為三個基本元素：功能、美學和效能。</span><span class="sxs-lookup"><span data-stu-id="2b489-114">UI design can be divided into three essential elements : functionality, aesthetics, and performance.</span></span>

<span data-ttu-id="2b489-115">通常，應用程式開發期間的主要焦點是功能。</span><span class="sxs-lookup"><span data-stu-id="2b489-115">More often than not, the primary focus during application development is functionality.</span></span> <span data-ttu-id="2b489-116">應用程式是否可供使用？</span><span class="sxs-lookup"><span data-stu-id="2b489-116">Is the application usable?</span></span> <span data-ttu-id="2b489-117">是否可讓使用者完成工作？</span><span class="sxs-lookup"><span data-stu-id="2b489-117">Does it enable users to complete tasks?</span></span> <span data-ttu-id="2b489-118">不過，功能只是故事的一部分。</span><span class="sxs-lookup"><span data-stu-id="2b489-118">However, functionality is only a part of the story.</span></span>

<span data-ttu-id="2b489-119">美學說明如何顯示及呈現專案，以及將專案傳達給使用者的樣式。</span><span class="sxs-lookup"><span data-stu-id="2b489-119">Aesthetics describe how things are shown and presented, the style in which things are communicated to the user.</span></span> <span data-ttu-id="2b489-120">美學是非常主觀的，而且比功能需求和效能度量更難以量化。</span><span class="sxs-lookup"><span data-stu-id="2b489-120">Aesthetics are very subjective and much more difficult to quantify than functional requirements and performance metrics.</span></span> <span data-ttu-id="2b489-121">美學通常會細分為簡單的選擇-色彩彼此互補的方式，或 UI 元素傳達其意義的方式，通常會影響人對某些事物的感覺，並影響其使用方式。</span><span class="sxs-lookup"><span data-stu-id="2b489-121">Aesthetics typically come down to simple choices—how colors complement each other or how UI elements convey their meaning—that often affect the way a person feels about something and influence how successful they are using it.</span></span>

<span data-ttu-id="2b489-122">效能不僅以速度來測量，也能以可靠性來測量。</span><span class="sxs-lookup"><span data-stu-id="2b489-122">Performance is measured by not only speed, but also reliability.</span></span> <span data-ttu-id="2b489-123">如果應用程式的外觀和感覺很棒，很容易使用，但重複當機，可能不會成功。</span><span class="sxs-lookup"><span data-stu-id="2b489-123">If an application looks and feels great, is easy to use, but crashes repeatedly, it likely won't be very successful.</span></span> <span data-ttu-id="2b489-124">應用程式必須為使用者提供可靠性的完全信心。</span><span class="sxs-lookup"><span data-stu-id="2b489-124">The application has to provide a user with full confidence in its reliability.</span></span>

<span data-ttu-id="2b489-125">以下是一些可對 Windows 應用程式成功 UI 造成影響的設計階段工作。</span><span class="sxs-lookup"><span data-stu-id="2b489-125">The following are some design phase tasks that can contribute to a successful UI for a Windows application.</span></span>

## <a name="functional-requirements"></a><span data-ttu-id="2b489-126">功能需求</span><span class="sxs-lookup"><span data-stu-id="2b489-126">Functional Requirements</span></span>

<span data-ttu-id="2b489-127">在設計階段早期考慮下列建議，以將使用者體驗優化到最廣泛的物件：</span><span class="sxs-lookup"><span data-stu-id="2b489-127">Consider the following suggestions early in the design phase to optimize the user experience across the broadest audience possible:</span></span>

-   <span data-ttu-id="2b489-128">遵循 UI 設計指導方針。</span><span class="sxs-lookup"><span data-stu-id="2b489-128">Follow UI design guidelines.</span></span>

    <span data-ttu-id="2b489-129">熟悉 [Windows 使用者經驗互動指導方針](../uxguide/guidelines.md) ，並在應用程式 UI 的設計、執行和測試進行時經常參考它們。</span><span class="sxs-lookup"><span data-stu-id="2b489-129">Become familiar with the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md) and refer to them often as the design, implementation, and testing of the application UI progresses.</span></span>

-   <span data-ttu-id="2b489-130">確定 UI 可供存取。</span><span class="sxs-lookup"><span data-stu-id="2b489-130">Ensure that the UI is accessible.</span></span>

    <span data-ttu-id="2b489-131">請務必將協助工具從產品生命週期的開頭整合至 UI 設計。</span><span class="sxs-lookup"><span data-stu-id="2b489-131">Be sure to integrate accessibility into the UI design from the beginning of the product lifecycle.</span></span> <span data-ttu-id="2b489-132">修整協助工具的成本極高，因為存取範圍開發的一部分需要注意架構層級。</span><span class="sxs-lookup"><span data-stu-id="2b489-132">Retrofitting accessibility can be extremely costly because part of accessibility development requires attention at the architectural level.</span></span> <span data-ttu-id="2b489-133">如需詳細資訊，請下載 [適用于協助工具電子書的工程軟體](https://www.microsoft.com/download/details.aspx?id=19262)。</span><span class="sxs-lookup"><span data-stu-id="2b489-133">For more information, download the [Engineering Software for Accessibility eBook](https://www.microsoft.com/download/details.aspx?id=19262).</span></span>

-   <span data-ttu-id="2b489-134">支援國際市場。</span><span class="sxs-lookup"><span data-stu-id="2b489-134">Support the international marketplace.</span></span>

    <span data-ttu-id="2b489-135">Windows 包含可在 Windows 應用程式中支援許多文化特性和書寫語言的技術。</span><span class="sxs-lookup"><span data-stu-id="2b489-135">Windows includes technologies that enable support for many cultures and written languages in a Windows application.</span></span> <span data-ttu-id="2b489-136">如果應用程式的目標是國際市場，請務必將國際化支援包含在專案開頭的 UI 設計中。</span><span class="sxs-lookup"><span data-stu-id="2b489-136">If the application is targeting the international marketplace, it is important to include internationalization support in the UI design from the beginning of the project.</span></span> <span data-ttu-id="2b489-137">如需詳細資訊，請參閱 [Windows 應用程式的國際化](../intl/international-support.md)。</span><span class="sxs-lookup"><span data-stu-id="2b489-137">For more information, see [Internationalization for Windows Applications](../intl/international-support.md).</span></span>

## <a name="user-analysis"></a><span data-ttu-id="2b489-138">使用者分析</span><span class="sxs-lookup"><span data-stu-id="2b489-138">User Analysis</span></span>

<span data-ttu-id="2b489-139">設計成功介面的一個重要步驟，就是在撰寫任何程式碼之前，先對使用者的需要和應用程式的需要有基本的瞭解。</span><span class="sxs-lookup"><span data-stu-id="2b489-139">A critical step in designing a successful interface is attaining a basic understanding of what users need and want from an application before writing any code.</span></span> <span data-ttu-id="2b489-140">請記住，應用程式的潛在使用者已經以某種方式進行工作，而現有的工具和程式應該盡可能完整地理解。</span><span class="sxs-lookup"><span data-stu-id="2b489-140">Remember, potential users of an application are already doing their job in some way and existing tools and processes should be understood as fully as possible.</span></span> <span data-ttu-id="2b489-141">請勿完全考慮這些問題而設計。</span><span class="sxs-lookup"><span data-stu-id="2b489-141">Do not design without fully considering these issues.</span></span>

<span data-ttu-id="2b489-142">最簡單且最非正式的方法是與產品的預期使用者交談。</span><span class="sxs-lookup"><span data-stu-id="2b489-142">The simplest and most informal approach is talking to the intended users of the product.</span></span> <span data-ttu-id="2b489-143">直接從來源取得資訊-避免使用經理或主管作為實際取用者的 proxy。</span><span class="sxs-lookup"><span data-stu-id="2b489-143">Get information directly from the source–avoid using managers or executives as proxies for actual consumers.</span></span> <span data-ttu-id="2b489-144">請考慮讓一小組的開發人員和計畫經理對其工作場所中的使用者付費，讓他們有機會討論他們的工作，並使用其目前的工具來收集他們所面臨之問題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2b489-144">Consider having small groups of developers and program managers pay informal visits to users in their workplaces where there is an opportunity to discuss how they work and gather details of the issues they face with their current tools.</span></span>

<span data-ttu-id="2b489-145">請記住，請勿詢問前置或偏差問題，因為這會直接影響使用者意見反應的品質和有效性。</span><span class="sxs-lookup"><span data-stu-id="2b489-145">Remember, do not to ask leading or biased questions as this will directly affect the quality and validity of the user feedback.</span></span> <span data-ttu-id="2b489-146">在此階段撰寫問題時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="2b489-146">Keep the following in mind when composing questions during this phase:</span></span>

-   <span data-ttu-id="2b489-147">誰是使用者？</span><span class="sxs-lookup"><span data-stu-id="2b489-147">Who are our users?</span></span> <span data-ttu-id="2b489-148">他們有哪些技能和知識？</span><span class="sxs-lookup"><span data-stu-id="2b489-148">What skills and knowledge do they have?</span></span>
-   <span data-ttu-id="2b489-149">我們可以使用不同的資料來源來瞭解他們的體驗嗎？</span><span class="sxs-lookup"><span data-stu-id="2b489-149">What different sources of data can we use to understand their experience?</span></span>
-   <span data-ttu-id="2b489-150">他們將使用我們的產品完成哪些目標和工作？</span><span class="sxs-lookup"><span data-stu-id="2b489-150">What goals and tasks will they use our product to complete?</span></span>
-   <span data-ttu-id="2b489-151">我們所做的假設是什麼，我們要如何驗證呢？</span><span class="sxs-lookup"><span data-stu-id="2b489-151">What assumptions are we making and how can we verify them?</span></span>
-   <span data-ttu-id="2b489-152">我們有哪些資料來源？</span><span class="sxs-lookup"><span data-stu-id="2b489-152">What sources of data do we have?</span></span> <span data-ttu-id="2b489-153"> (的可用性研究和啟發學習法評估是不錯的起點。 ) </span><span class="sxs-lookup"><span data-stu-id="2b489-153">(Usability studies and heuristic evaluations are good places to start.)</span></span>

### <a name="problem-statements"></a><span data-ttu-id="2b489-154">問題陳述</span><span class="sxs-lookup"><span data-stu-id="2b489-154">Problem Statements</span></span>

<span data-ttu-id="2b489-155">一旦收集了所有使用者意見反應，請分析並將其納入相關的問題和需求中。</span><span class="sxs-lookup"><span data-stu-id="2b489-155">Once all user feedback has been collected, analyze and distill it into related issues and requirements.</span></span> <span data-ttu-id="2b489-156">請儘量避免在此時考慮解決方案。</span><span class="sxs-lookup"><span data-stu-id="2b489-156">Try to avoid thinking about solutions at this point.</span></span> <span data-ttu-id="2b489-157">請確定已完整識別問題，而不只是徵兆。</span><span class="sxs-lookup"><span data-stu-id="2b489-157">Make sure the problems are fully identified, not just the symptoms.</span></span>

<span data-ttu-id="2b489-158">針對每個問題或需求，撰寫一份句子問題陳述 (從使用者的觀點來) 看，通常會有很大的説明。</span><span class="sxs-lookup"><span data-stu-id="2b489-158">It is often helpful to compose a list of one sentence problem statements (from the users perspective) for each issue or requirement.</span></span> <span data-ttu-id="2b489-159">例如，「將編輯方塊寬度調整為15個字元」並不是問題。</span><span class="sxs-lookup"><span data-stu-id="2b489-159">For example, "Resize edit box width to 15 characters" is not a problem.</span></span> <span data-ttu-id="2b489-160">但是「太難輸入長的搜尋字詞」是有效的問題陳述。</span><span class="sxs-lookup"><span data-stu-id="2b489-160">But "It is too difficult to type in long search terms" is a valid problem statement.</span></span> <span data-ttu-id="2b489-161">差別很大。</span><span class="sxs-lookup"><span data-stu-id="2b489-161">The difference is dramatic.</span></span> <span data-ttu-id="2b489-162">請不要同時定義方案和問題：通常會遺失真正的問題。</span><span class="sxs-lookup"><span data-stu-id="2b489-162">Try not to define the solution and the problem at the same time: often the real problem is lost.</span></span> <span data-ttu-id="2b489-163">在此範例中，有許多其他方式可解決搜尋詞彙的問題，包括變更編輯方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="2b489-163">In this example, there may be many other ways to solve the problem of search terms, including changing the size of the edit box.</span></span> <span data-ttu-id="2b489-164">一律牢記替代的解決方案。</span><span class="sxs-lookup"><span data-stu-id="2b489-164">Always keep alternative solutions in mind.</span></span>

<span data-ttu-id="2b489-165">以下是問題陳述的其他範例：</span><span class="sxs-lookup"><span data-stu-id="2b489-165">The following are additional examples of problem statements:</span></span>

-   <span data-ttu-id="2b489-166">很難從網站的某個區段流覽至另一個區段。</span><span class="sxs-lookup"><span data-stu-id="2b489-166">It is difficult to navigate from one section of the Web site to another.</span></span>
-   <span data-ttu-id="2b489-167">使用者必須等候太長的時間才能載入軟體。</span><span class="sxs-lookup"><span data-stu-id="2b489-167">Users have to wait too long for the software to load.</span></span>
-   <span data-ttu-id="2b489-168">我們的安全性錯誤訊息很難理解。</span><span class="sxs-lookup"><span data-stu-id="2b489-168">Our security error messages are difficult to understand.</span></span>
-   <span data-ttu-id="2b489-169">註冊頁面上有太多問題，使用者通常會放棄它。</span><span class="sxs-lookup"><span data-stu-id="2b489-169">The registration page has too many questions, and users often abandon it.</span></span>
-   <span data-ttu-id="2b489-170">在網站索引上尋找特定產品太難完成。</span><span class="sxs-lookup"><span data-stu-id="2b489-170">Finding a specific product on the site index is too hard to complete.</span></span>

<span data-ttu-id="2b489-171">如果問題陳述的範圍很廣，可能會有許多創新、富有創意的方法可以解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="2b489-171">If the problem statements are broad enough, there are likely to be many innovative and creative ways to solve them.</span></span>

### <a name="priorities"></a><span data-ttu-id="2b489-172">優先順序</span><span class="sxs-lookup"><span data-stu-id="2b489-172">Priorities</span></span>

<span data-ttu-id="2b489-173">取得專案清單以及依優先權排名它們的動作，會定義發行。</span><span class="sxs-lookup"><span data-stu-id="2b489-173">The act of taking a list of items, and ranking them by priority, defines a release.</span></span> <span data-ttu-id="2b489-174">若沒有明確的優先順序，小組可能會對抗和對抗應完成的作業，以及應剪下的專案。</span><span class="sxs-lookup"><span data-stu-id="2b489-174">Without clear priorities, teams may fight and argue over what things should be done and what things should be cut.</span></span> <span data-ttu-id="2b489-175">與設定優先順序相關的工作應該可以更輕鬆地完成研究，但這一直是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="2b489-175">The work involved in setting priorities should be easier with the research complete, but it's always a challenge.</span></span>

<span data-ttu-id="2b489-176">設定優先順序必須能夠評估至少三個準則：排程、小組和商務。</span><span class="sxs-lookup"><span data-stu-id="2b489-176">Setting priorities requires the ability to evaluate on at least three criteria: schedule, team, and business.</span></span> <span data-ttu-id="2b489-177">專案可能會設定預先定義的排程，以限制可以完成的工作大小和規模。</span><span class="sxs-lookup"><span data-stu-id="2b489-177">There may be a predefined schedule set for the project, which limits the size and scale of the work that can be done.</span></span> <span data-ttu-id="2b489-178">可能需要重寫半程式碼基底的問題，不應該在小型發行週期期間嘗試。</span><span class="sxs-lookup"><span data-stu-id="2b489-178">A problem that is likely to require rewriting half the code-base should not be attempted during a small release cycle.</span></span>

<span data-ttu-id="2b489-179">小組的組成和本質會定義可以完成的工作類型。</span><span class="sxs-lookup"><span data-stu-id="2b489-179">The makeup and nature of a team defines what kinds of work can be done.</span></span> <span data-ttu-id="2b489-180">小組有哪些其他承諾？</span><span class="sxs-lookup"><span data-stu-id="2b489-180">What other commitments does the team have?</span></span> <span data-ttu-id="2b489-181">小組是否有設計人員或可用性工程師？</span><span class="sxs-lookup"><span data-stu-id="2b489-181">Is there a designer or usability engineer on the team?</span></span> <span data-ttu-id="2b489-182">小組有哪些技能可以設計 Web 或 UI？</span><span class="sxs-lookup"><span data-stu-id="2b489-182">What skills with Web or UI design does the team have?</span></span> <span data-ttu-id="2b489-183">最後，最重要的是商務考慮。</span><span class="sxs-lookup"><span data-stu-id="2b489-183">Last, and most important, are business considerations.</span></span> <span data-ttu-id="2b489-184">此專案的收益目標為何？</span><span class="sxs-lookup"><span data-stu-id="2b489-184">What are the revenue goals for this project?</span></span> <span data-ttu-id="2b489-185">誰是競爭者？</span><span class="sxs-lookup"><span data-stu-id="2b489-185">Who are the competitors?</span></span> <span data-ttu-id="2b489-186">解決特定問題的優點有哪些？</span><span class="sxs-lookup"><span data-stu-id="2b489-186">What are the advantages of solving certain problems?</span></span> <span data-ttu-id="2b489-187">哪些合作關係可以偽造？</span><span class="sxs-lookup"><span data-stu-id="2b489-187">What partnerships can be forged?</span></span> <span data-ttu-id="2b489-188">您也應該先識別任何其他考慮，再排列清單的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2b489-188">Any other considerations should also be identified before prioritizing the list.</span></span>

<span data-ttu-id="2b489-189">一旦設定優先順序之後，問題陳述的清單就會設定產品的方向，並確保開發是以正確的領域為目標。</span><span class="sxs-lookup"><span data-stu-id="2b489-189">Once prioritized, the list of problem statements sets the direction for the product and ensures that development is targeted in the right areas.</span></span>

## <a name="conceptual-design"></a><span data-ttu-id="2b489-190">概念設計</span><span class="sxs-lookup"><span data-stu-id="2b489-190">Conceptual Design</span></span>

<span data-ttu-id="2b489-191">一般而言，在概念設計階段中不會處理 UI。</span><span class="sxs-lookup"><span data-stu-id="2b489-191">Typically, the UI is not addressed in the conceptual design phase.</span></span> <span data-ttu-id="2b489-192">不過，這個階段的確需要完整的商務模型，而且必須具備完整的使用者設定檔和使用案例，才能成功使用使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="2b489-192">However, this phase does require a thorough business model with complete user profiles and usage scenarios which are imperative for a successful user experience.</span></span>

## <a name="logical-design"></a><span data-ttu-id="2b489-193">邏輯設計</span><span class="sxs-lookup"><span data-stu-id="2b489-193">Logical Design</span></span>

<span data-ttu-id="2b489-194">「邏輯設計」階段是開發支援概念設計的初始原型。</span><span class="sxs-lookup"><span data-stu-id="2b489-194">The logical design phase is when the initial prototypes that support the conceptual design are developed.</span></span>

<span data-ttu-id="2b489-195">在這個階段中，也會識別在開發期間使用的特定硬體和軟體技術，以判斷最終產品中 UI 的功能。</span><span class="sxs-lookup"><span data-stu-id="2b489-195">The specific hardware and software technologies to be used during development are also identified in this phase, which can determine the capabilities of the UI in the final product.</span></span> <span data-ttu-id="2b489-196">如需詳細資訊，請參閱 [消費者介面技術](user-interface-technologies-for-windows-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="2b489-196">For more information, see [User Interface Technologies](user-interface-technologies-for-windows-applications.md).</span></span>

<span data-ttu-id="2b489-197">除了開發工具之外，您應識別出應用程式的目標各種硬體需求和外型規格。</span><span class="sxs-lookup"><span data-stu-id="2b489-197">In addition to the development tools, the various hardware requirements and form factors that are to be targeted by the application should be identified.</span></span>

## <a name="physical-design"></a><span data-ttu-id="2b489-198">實體設計</span><span class="sxs-lookup"><span data-stu-id="2b489-198">Physical Design</span></span>

<span data-ttu-id="2b489-199">實體設計階段會決定如何針對邏輯設計中所識別的特定硬體和外型規格來執行 UI 設計。</span><span class="sxs-lookup"><span data-stu-id="2b489-199">The physical design phase determines how a UI design is to be implemented for the specific hardware and form factors that were identified in the logical design.</span></span>

<span data-ttu-id="2b489-200">在這個階段中，硬體或外型規格的限制可能會在需要對設計進行大幅改進的 UI 上引進非預期的條件約束。</span><span class="sxs-lookup"><span data-stu-id="2b489-200">It is during this phase that hardware or form factor limitations might introduce unexpected constraints on the UI that require significant refinements to the design.</span></span>

 

 