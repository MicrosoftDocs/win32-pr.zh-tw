---
title: Help
description: 使用 [說明] 作為輔助機制，以協助使用者完成及更清楚地瞭解工作 \ 郵件; 這是 UI 本身的主要機制。 套用這些指導方針，讓內容真正實用且容易找到。
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 907494e9a97ccaf51e4eba463c34e49854b14a81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556721"
---
# <a name="help"></a><span data-ttu-id="73fda-104">Help</span><span class="sxs-lookup"><span data-stu-id="73fda-104">Help</span></span>

> [!NOTE]
> <span data-ttu-id="73fda-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="73fda-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="73fda-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="73fda-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="73fda-107">使用「說明」做為次要機制，以協助使用者完成及更瞭解主要機制成為 UI 本身的工作。</span><span class="sxs-lookup"><span data-stu-id="73fda-107">Use Help as a secondary mechanism to help users complete and better understand tasks the primary mechanism being the UI itself.</span></span> <span data-ttu-id="73fda-108">套用這些指導方針，讓內容真正實用且容易找到。</span><span class="sxs-lookup"><span data-stu-id="73fda-108">Apply these guidelines to make the content truly helpful and easy to find.</span></span>

<span data-ttu-id="73fda-109">說明系統是由各種類型的內容所組成，其設計目的是要協助使用者無法完成工作、想要更詳細地瞭解概念，或需要比 UI 提供更多的技術詳細資料。</span><span class="sxs-lookup"><span data-stu-id="73fda-109">A Help system is composed of various types of content designed to assist users when they are unable to complete a task, want to understand a concept in more detail, or need more technical details than are available in the UI.</span></span>

<span data-ttu-id="73fda-110">在本文中，我們將說明做為 UI 的次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="73fda-110">In this article, we refer to Help as secondary to UI.</span></span> <span data-ttu-id="73fda-111">UI 是主要的，因為這是使用者第一次嘗試解決其問題的地方。</span><span class="sxs-lookup"><span data-stu-id="73fda-111">The UI is primary because that is where users first try to solve their problems.</span></span> <span data-ttu-id="73fda-112">只有在無法使用 UI 完成工作時，他們才會洽詢說明系統。</span><span class="sxs-lookup"><span data-stu-id="73fda-112">They consult the Help system only if they can't accomplish their task with the UI.</span></span>

![<span data-ttu-id="73fda-113">[windows 說明及支援] 頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-113">screen shot of windows help and support page</span></span> ](images/winenv-help-image1.png)

<span data-ttu-id="73fda-114">[Windows 說明及支援] 首頁，可從 [開始] 功能表取得。</span><span class="sxs-lookup"><span data-stu-id="73fda-114">The Windows Help and Support home page, available from the Start menu.</span></span>

<span data-ttu-id="73fda-115">**注意：** 與 [樣式和語氣](text-style-tone.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="73fda-115">**Note:** Guidelines related to [style and tone](text-style-tone.md) are presented in a separate article.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="73fda-116">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="73fda-116">Is this the right user interface?</span></span>

<span data-ttu-id="73fda-117">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="73fda-117">To decide, consider these questions:</span></span>

-   <span data-ttu-id="73fda-118">**您的目標使用者的動機為何？**</span><span class="sxs-lookup"><span data-stu-id="73fda-118">**How motivated are your target users?**</span></span> <span data-ttu-id="73fda-119">更具動機的是探索您程式的功能，並成為中繼或甚至是資深的使用者，而他們越願意透過諮詢說明主題來研究問題的答案。</span><span class="sxs-lookup"><span data-stu-id="73fda-119">The more highly motivated they are to discover functionality of your program and become intermediate or even advanced users of it, the more willing they will be to research answers to their questions by consulting Help topics.</span></span>
-   <span data-ttu-id="73fda-120">**您是否使用說明來修正不正確的 UI？**</span><span class="sxs-lookup"><span data-stu-id="73fda-120">**Are you using Help to fix a bad UI?**</span></span> <span data-ttu-id="73fda-121">您的 UI 愈好，越少的使用者就會尋求其他協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-121">The better your UI, the less users will seek additional help.</span></span> <span data-ttu-id="73fda-122">如果您的程式有很清楚、實用的主要 UI (（例如，不含術語的錯誤訊息、正確撰寫的嚮導，以及明確的對話方塊）) ，您可能完全不需要次要說明系統。</span><span class="sxs-lookup"><span data-stu-id="73fda-122">If your program has very clear, helpful primary UI (such as jargon-free error messages, well-written wizards, and unambiguous dialog boxes), you may not need a secondary Help system at all.</span></span>
-   <span data-ttu-id="73fda-123">**您的程式相當簡單嗎？**</span><span class="sxs-lookup"><span data-stu-id="73fda-123">**Is your program relatively simple?**</span></span> <span data-ttu-id="73fda-124">如果是的話，請考慮將所有必要的協助內容併入您的主要 UI 介面中。</span><span class="sxs-lookup"><span data-stu-id="73fda-124">If so, consider incorporating all necessary assistance content into your primary UI surfaces.</span></span> <span data-ttu-id="73fda-125">使用者更可能在執行複雜工作的程式中尋求其他協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-125">Users are more likely to seek additional help in programs that perform complex tasks.</span></span>
-   <span data-ttu-id="73fda-126">**您的應用程式適用于開發人員、IT 專業人員或其他軟體專家嗎？**</span><span class="sxs-lookup"><span data-stu-id="73fda-126">**Is your application intended for developers, IT professionals, or other software experts?**</span></span> <span data-ttu-id="73fda-127">這些使用者傾向于提供程式設計語言慣例的參考說明，以及熟悉功能的深入概念說明。</span><span class="sxs-lookup"><span data-stu-id="73fda-127">These users tend to expect reference Help for programming language conventions and in-depth conceptual Help for mastery of features.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="73fda-128">設計概念</span><span class="sxs-lookup"><span data-stu-id="73fda-128">Design concepts</span></span>

<span data-ttu-id="73fda-129">如果您決定在程式中包含說明，請將它整合到您的整體設計中。</span><span class="sxs-lookup"><span data-stu-id="73fda-129">If you decide to include Help in your program, integrate it into your overall design.</span></span> <span data-ttu-id="73fda-130">說明介面應該簡單、有效率且相關;它應該可以讓使用者輕鬆地取得協助，然後返回其工作。</span><span class="sxs-lookup"><span data-stu-id="73fda-130">The Help interface should be simple, efficient, and relevant; it should enable users to get help easily and then return to their task.</span></span> <span data-ttu-id="73fda-131">以使用者的時間來思考您的說明系統：先將基本協助直接併入您的 UI，然後在更詳細的說明中建立清楚且一致的進入點，以最小化中斷。</span><span class="sxs-lookup"><span data-stu-id="73fda-131">Think of your Help system in terms of users' time: minimize disruption first by anticipating where they will encounter problems in your program, then solving those problems by incorporating fundamental assistance directly into your UI, and creating clear and consistent entry points into your more detailed Help.</span></span>

<span data-ttu-id="73fda-132">Windows 協助是根據這些原則所設計。</span><span class="sxs-lookup"><span data-stu-id="73fda-132">Windows assistance was designed according to these principles.</span></span> <span data-ttu-id="73fda-133">以下是 Windows 說明使用者體驗的一些設計變更：</span><span class="sxs-lookup"><span data-stu-id="73fda-133">Here are some of the design changes to the Windows Help user experience:</span></span>

-   <span data-ttu-id="73fda-134">有更多可探索的進入點可協助您從主要 UI (特別是 UI 介面（例如對話方塊、錯誤訊息和) 的次要資料庫）的新說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-134">More discoverable entry points to Help from the primary UI (especially new Help links from UI surfaces such as dialog boxes, error messages, and wizards).</span></span> <span data-ttu-id="73fda-135">說明連結會帶您直接前往 [說明] 中的相關主題。</span><span class="sxs-lookup"><span data-stu-id="73fda-135">Help links take you directly to the pertinent topic in Help.</span></span>
-   <span data-ttu-id="73fda-136">在大部分主控台中樞頁面的右上角，以及 shell 資料夾都有提供 [說明] 按鈕圖示。</span><span class="sxs-lookup"><span data-stu-id="73fda-136">A Help button icon is available in the upper-right corner of most Control Panel hub pages, as well as shell folders.</span></span>
-   <span data-ttu-id="73fda-137">使用者可以在線上時，選擇取得 Windows 線上說明及支援的最新說明內容。</span><span class="sxs-lookup"><span data-stu-id="73fda-137">Users can choose to get the most up-to-date Help content from Windows Online Help and Support when they're online.</span></span>
-   <span data-ttu-id="73fda-138">說明主題現在是以工作為基礎，而不是以功能為主，讓使用者可以快速且有效率地完成其工作。</span><span class="sxs-lookup"><span data-stu-id="73fda-138">Help topics are now task-based rather than feature-focused, so that users can accomplish their tasks quickly and efficiently.</span></span>
-   <span data-ttu-id="73fda-139">說明主題現在主要是以已知的最上層使用者案例為基礎。</span><span class="sxs-lookup"><span data-stu-id="73fda-139">Help topics are now largely based on known top user scenarios.</span></span>
-   <span data-ttu-id="73fda-140">使用真實世界的語言，說明主題具有更寬鬆且非正式的 [語氣](text-style-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="73fda-140">Help topics have a more relaxed and informal [tone](text-style-tone.md), using real-world language.</span></span>
-   <span data-ttu-id="73fda-141">說明主題的設計目的是為了有效掃描，因為使用者很少會讀取單字的單字內容。</span><span class="sxs-lookup"><span data-stu-id="73fda-141">Help topics are designed for effective scanning, as users rarely read the content word-for-word.</span></span>

### <a name="an-analogy-for-help"></a><span data-ttu-id="73fda-142">說明的類比</span><span class="sxs-lookup"><span data-stu-id="73fda-142">An analogy for Help</span></span>

<span data-ttu-id="73fda-143">若要更深入地瞭解如何設計您的說明系統，請考慮與日常生活的對比。</span><span class="sxs-lookup"><span data-stu-id="73fda-143">To think in greater depth about designing your Help system, consider an analogy from everyday life.</span></span> <span data-ttu-id="73fda-144">您會在不熟悉的城市中遺失。</span><span class="sxs-lookup"><span data-stu-id="73fda-144">You are lost in an unfamiliar city.</span></span> <span data-ttu-id="73fda-145">您該怎麼辦？</span><span class="sxs-lookup"><span data-stu-id="73fda-145">What do you do?</span></span> <span data-ttu-id="73fda-146">許多會回應如下：</span><span class="sxs-lookup"><span data-stu-id="73fda-146">Many would react like this:</span></span>

-   <span data-ttu-id="73fda-147">取得導向;尋找地標、街道號 (名稱和指向) 位置的指標。</span><span class="sxs-lookup"><span data-stu-id="73fda-147">Get oriented; look for landmarks, street signs (names and pointers to places).</span></span>
-   <span data-ttu-id="73fda-148">尋找地圖。</span><span class="sxs-lookup"><span data-stu-id="73fda-148">Look for maps.</span></span>
-   <span data-ttu-id="73fda-149">最後，做為最後的手段，請要求指示或打電話給 friend。</span><span class="sxs-lookup"><span data-stu-id="73fda-149">Finally, as a last resort, ask for directions or call a friend.</span></span>

<span data-ttu-id="73fda-150">城市的「介面」設計會影響您的協助需求。</span><span class="sxs-lookup"><span data-stu-id="73fda-150">The design of the city's "interface" affects your need for assistance.</span></span> <span data-ttu-id="73fda-151">有條理的街道、明確方向 (醫院、機場、博物館和郵局) 的指標，以及清楚的地理功能或大樓等清楚的地標，可協助您找到您的方式。</span><span class="sxs-lookup"><span data-stu-id="73fda-151">Well-labeled streets, explicit directions (pointers to hospitals, airports, museums, and the post office), and clear landmarks such as prominent geographical features or buildings help you find your way.</span></span>

<span data-ttu-id="73fda-152">您會在最後手段時要求協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-152">You ask for help as a last resort.</span></span> <span data-ttu-id="73fda-153">這表示城市的「介面」因設計不佳而造成混淆。</span><span class="sxs-lookup"><span data-stu-id="73fda-153">It's an indication that the city's "interface" has failed by being poorly designed and confusing.</span></span> <span data-ttu-id="73fda-154">您較有可能在具有特定標籤的位置中要求協助，以建議效益。</span><span class="sxs-lookup"><span data-stu-id="73fda-154">You are more likely to ask for help in a place that has a specific label that suggests helpfulness.</span></span> <span data-ttu-id="73fda-155">例如，您比較有可能在標示為「方向」或「資訊」的位置，在像城市廳一樣的地方提出協助，即使是城市廳的任何人都能提供指引。</span><span class="sxs-lookup"><span data-stu-id="73fda-155">For example, you are more likely to ask for help in a place labeled "Directions" or "Information" than a general place like the City Hall even though just about anyone at City Hall could give you directions.</span></span>

<span data-ttu-id="73fda-156">當您尋求協助時，很可能會感到挫折，而只想要取得您想要的目的地。</span><span class="sxs-lookup"><span data-stu-id="73fda-156">When you ask for help, chances are you are frustrated and just want to get to your intended destination.</span></span> <span data-ttu-id="73fda-157">您可能不打算花時間來導覽城市或學習其歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="73fda-157">You probably aren't in the mood to spend time taking a tour of the city or learning about its history.</span></span> <span data-ttu-id="73fda-158">此外，您的動機取決於工作的重要性。</span><span class="sxs-lookup"><span data-stu-id="73fda-158">Further, your motivation depends on the importance of the task.</span></span> <span data-ttu-id="73fda-159">如果您嘗試找出旅館的房間，您將會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="73fda-159">If you are trying to find your hotel room, you will do whatever it takes.</span></span> <span data-ttu-id="73fda-160">但是，如果您的目標是要找出稍微重要的一點，您很可能只會在適當的努力之後放棄。</span><span class="sxs-lookup"><span data-stu-id="73fda-160">However, if your goal is to find a place of minor importance, most likely you will just give up after a modest effort.</span></span>

<span data-ttu-id="73fda-161">在真正的空間中找出您的所有層面，都對應到使用者在您的程式虛擬空間中的一般方式。</span><span class="sxs-lookup"><span data-stu-id="73fda-161">All of these aspects of finding your way in real space correspond to how users typically find their way in the virtual space of your program.</span></span> <span data-ttu-id="73fda-162">在主要 UI 之外搜尋說明的本質是 disorienting;您最好透過設計完善的 UI 和智慧型的「街道符號」來緩和這類體驗，以將使用者導向所需的答案。</span><span class="sxs-lookup"><span data-stu-id="73fda-162">Seeking help beyond the primary UI is by its very nature disorienting; do your best to mitigate such an experience by well-designed UI and intelligent "street signs" to direct users to the answers they need.</span></span>

### <a name="designing-ui-so-that-help-is-unnecessary"></a><span data-ttu-id="73fda-163">設計 UI 讓您不需要協助</span><span class="sxs-lookup"><span data-stu-id="73fda-163">Designing UI so that Help is unnecessary</span></span>

<span data-ttu-id="73fda-164">請先嘗試以下列方式提供不必要的協助：</span><span class="sxs-lookup"><span data-stu-id="73fda-164">Try to make Help unnecessary in the first place, by:</span></span>

-   <span data-ttu-id="73fda-165">讓您輕鬆探索和執行一般工作。</span><span class="sxs-lookup"><span data-stu-id="73fda-165">Making common tasks easy to discover and perform.</span></span>
-   <span data-ttu-id="73fda-166">提供明確的 [主要指示](text-ui.md)。</span><span class="sxs-lookup"><span data-stu-id="73fda-166">Providing clear [main instructions](text-ui.md).</span></span>
-   <span data-ttu-id="73fda-167">提供明確、精確的控制項標籤，其為目標和工作導向。</span><span class="sxs-lookup"><span data-stu-id="73fda-167">Providing clear, concise control labels that are goal- and task-oriented.</span></span>
-   <span data-ttu-id="73fda-168">在需要時提供補充指示和說明。</span><span class="sxs-lookup"><span data-stu-id="73fda-168">Providing supplemental instructions and explanations where needed.</span></span>
-   <span data-ttu-id="73fda-169">使用受限制為有效選擇的控制項、提供適當的預設值、處理所有輸入格式，以及防止錯誤，來預測肇因問題。</span><span class="sxs-lookup"><span data-stu-id="73fda-169">Anticipating avoidable problems by using controls constrained to valid choices, providing suitable default values, handling all input formats, and preventing errors.</span></span>
-   <span data-ttu-id="73fda-170">撰寫錯誤訊息，為使用者提供清楚的解決方案或動作。</span><span class="sxs-lookup"><span data-stu-id="73fda-170">Writing error messages that provide a clear solution or action for the user to take.</span></span>
-   <span data-ttu-id="73fda-171">避免混淆的 UI 設計，例如流程較差的工作，或使用已停用的控制項，因此沒有明顯的原因。</span><span class="sxs-lookup"><span data-stu-id="73fda-171">Avoiding confusing UI designs, such as tasks with poor flow or using controls that are disabled for no apparent reason.</span></span>
-   <span data-ttu-id="73fda-172">及早在開發週期中使用寫入器和編輯器，在整個程式中建立高品質且一致的 [UI 文字](text-ui.md) 。</span><span class="sxs-lookup"><span data-stu-id="73fda-172">Working with writers and editors early in the development cycle to create high-quality, consistent [UI text](text-ui.md) throughout your program.</span></span>

<span data-ttu-id="73fda-173">使用者應該不需要移到其他地方來瞭解如何使用您的 UI。</span><span class="sxs-lookup"><span data-stu-id="73fda-173">Users shouldn't have to go somewhere else to figure out how to use your UI.</span></span> <span data-ttu-id="73fda-174">將基本資訊直接新增至主要 UI，而不是強迫使用者立即內容和 [說明] 窗格中的使用者。</span><span class="sxs-lookup"><span data-stu-id="73fda-174">Add essential information directly into the primary UI, rather than forcing users out of their immediate context and into the Help pane.</span></span> <span data-ttu-id="73fda-175">如果重要資訊只存在於說明主題中，使用者很有可能不會看到它。</span><span class="sxs-lookup"><span data-stu-id="73fda-175">If important information exists only in a Help topic, there's a good chance that users won't see it.</span></span> <span data-ttu-id="73fda-176">如需選擇性且更詳細的資訊，請使用主要 UI 的 [說明] 連結，以取得補充協助的相關說明主題。</span><span class="sxs-lookup"><span data-stu-id="73fda-176">For information that is optional and more explanatory, use Help links from the primary UI to the relevant Help topic for supplemental assistance.</span></span>

### <a name="considering-user-motivation"></a><span data-ttu-id="73fda-177">考慮使用者動機</span><span class="sxs-lookup"><span data-stu-id="73fda-177">Considering user motivation</span></span>

<span data-ttu-id="73fda-178">針對大部分的使用者，速度和效率都是良好程式的最重要優點。</span><span class="sxs-lookup"><span data-stu-id="73fda-178">For most users, speed and efficiency are among the paramount virtues of good programs.</span></span> <span data-ttu-id="73fda-179">使用者想要完成工作。</span><span class="sxs-lookup"><span data-stu-id="73fda-179">Users want to get their work done.</span></span> <span data-ttu-id="73fda-180">一般而言，他們對於學習程式和技術並不感興趣，其耐心等候的時間只是因為該計畫提供自己的興趣，並解決手邊的問題。</span><span class="sxs-lookup"><span data-stu-id="73fda-180">Generally, they are not interested in learning about the program and the technology for its own sake; their patience extends only insofar as that program serves their own interests and solves problems at hand.</span></span>

<span data-ttu-id="73fda-181">將您的說明系統設計成符合使用者的動機。</span><span class="sxs-lookup"><span data-stu-id="73fda-181">Design your Help system to match your users' motivation.</span></span> <span data-ttu-id="73fda-182">例如，假設有一個 strolled 的使用者，最多可達一間的 kiosk。</span><span class="sxs-lookup"><span data-stu-id="73fda-182">For example, consider a user who has strolled up to a kiosk at a museum.</span></span> <span data-ttu-id="73fda-183">如果她無法快速地執行此工作，則可能只是放棄並離開。</span><span class="sxs-lookup"><span data-stu-id="73fda-183">If she cannot figure out how to perform the task quickly, she is likely just to give up and walk away.</span></span> <span data-ttu-id="73fda-184">她不太可能花時間使用說明。</span><span class="sxs-lookup"><span data-stu-id="73fda-184">She is unlikely to spend time using Help.</span></span> <span data-ttu-id="73fda-185">或者，高度動機的使用者對於研究您的說明系統以取得答案所花的時間會有更高的承受度。</span><span class="sxs-lookup"><span data-stu-id="73fda-185">Alternatively, a highly-motivated user has a higher tolerance for time spent researching your Help system for answers.</span></span> <span data-ttu-id="73fda-186">例如，必須平衡書籍的商務使用者可能願意查閱說明內容，以充分利用這個新的會計應用程式。</span><span class="sxs-lookup"><span data-stu-id="73fda-186">A business user who must balance the books, for example, is probably willing to consult Help content to get the most out of that new accounting application.</span></span>

### <a name="writing-content-for-scanning"></a><span data-ttu-id="73fda-187">寫入內容以進行掃描</span><span class="sxs-lookup"><span data-stu-id="73fda-187">Writing content for scanning</span></span>

<span data-ttu-id="73fda-188">撰寫說明主題，瞭解這些主題將會掃描是否有特定的資訊，而非單字的讀取字。</span><span class="sxs-lookup"><span data-stu-id="73fda-188">Write Help topics knowing that they will be scanned for specific information, not read word-for-word.</span></span> <span data-ttu-id="73fda-189">簡潔地撰寫、快速地取得點數，並提供使用者可採取行動的資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-189">Write concisely, getting to the point quickly, and providing information that users can act on.</span></span>

-   <span data-ttu-id="73fda-190">以一致的格式撰寫使用編號步驟的「使用說明」主題，讓使用者辨識他們正在取得程式性協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-190">Write "how-to" topics using numbered steps in a consistent format so that users recognize they are getting procedural assistance.</span></span>
-   <span data-ttu-id="73fda-191">撰寫參考主題，並使用資料表（例如）來呈現 UI 選項或語言語法，以方便掃描。</span><span class="sxs-lookup"><span data-stu-id="73fda-191">Write reference topics with ease-of-scanning in mind, using tables, for example, to present UI options or language syntax.</span></span>
-   <span data-ttu-id="73fda-192">撰寫以子標題邏輯方式組織的概念主題，讓使用者可以略過較不感興趣的整個區段。</span><span class="sxs-lookup"><span data-stu-id="73fda-192">Write conceptual topics that are logically organized by subheadings, so that the user can skip whole sections of lesser interest.</span></span>

<span data-ttu-id="73fda-193">在所有說明內容中，您可以更輕鬆地掃描專案符號清單，而非文字的標準段落區塊;但請謹慎使用專案符號清單，而不是未經組織材質的 crutch。</span><span class="sxs-lookup"><span data-stu-id="73fda-193">In all Help content, it is easier to scan bulleted lists than standard paragraph blocks of text; use bullet lists judiciously, though, not as a crutch for unorganized material.</span></span>

### <a name="creating-content-that-matters"></a><span data-ttu-id="73fda-194">建立重要內容</span><span class="sxs-lookup"><span data-stu-id="73fda-194">Creating content that matters</span></span>

<span data-ttu-id="73fda-195">假設沒有任何協助系統可預期每個使用者可能有的每個問題，請將大部分的內容放在最重要的案例中，以供您的目標使用者使用。</span><span class="sxs-lookup"><span data-stu-id="73fda-195">Given that no Help system can anticipate every question that every user might have, focus most of the content on answering the top questions in the top scenarios for your target users.</span></span> <span data-ttu-id="73fda-196">例如，在其他工作中，有效搜尋及如何建立網路連線 () 可能會有高度搜尋的主題。</span><span class="sxs-lookup"><span data-stu-id="73fda-196">For example, effective searching and how to establish network connectivity (among other tasks) may be highly sought-after topics.</span></span> <span data-ttu-id="73fda-197">此外，請將焦點放在您最常使用的使用者案例中，而不是為自己的工作記錄一項功能或技術。</span><span class="sxs-lookup"><span data-stu-id="73fda-197">Also, focus on tasks within your top user scenarios, rather than documenting a feature or technology exhaustively for its own sake.</span></span>

<span data-ttu-id="73fda-198">**秘訣：** 技術支援是協助內容的絕佳來源。</span><span class="sxs-lookup"><span data-stu-id="73fda-198">**Tip:** Technical support is a good source for Help content.</span></span> <span data-ttu-id="73fda-199">技術支援人員通常會記錄有關使用者嘗試 (和無法完成) 的特定程式或工作的常見問題記錄。</span><span class="sxs-lookup"><span data-stu-id="73fda-199">Help desks often keep records of frequently asked questions about particular programs or tasks that users are trying (and failing) to accomplish.</span></span>

<span data-ttu-id="73fda-200">不需要為 UI 中的每個功能提供協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-200">It isn't necessary to provide help for every feature in the UI.</span></span> <span data-ttu-id="73fda-201">**無用可協助您建立所有專案的說明。**</span><span class="sxs-lookup"><span data-stu-id="73fda-201">**Quite often, unhelpful Help results from trying to create Help for everything.**</span></span> <span data-ttu-id="73fda-202">如果 UI 的設計是妥善的，則這些說明主題大部分都不會有説明。他們只會重新聲明明顯的。</span><span class="sxs-lookup"><span data-stu-id="73fda-202">If the UI is well designed, most of these Help topics won't be very helpful; they will just restate the obvious.</span></span>

<span data-ttu-id="73fda-203">如果有一種以上的方法可以執行工作，則在大部分情況下，您可以只記錄缺乏經驗的使用者所使用的最常見方式。</span><span class="sxs-lookup"><span data-stu-id="73fda-203">If there is more than one way to perform a task, in most cases you can just document the most common way used by inexperienced users.</span></span> <span data-ttu-id="73fda-204">這種情況的例外狀況包括協助工具考慮 (記載滑鼠動作的鍵盤對應專案，例如) 和平臺考慮 (針對 tablet 外型規格進行記錄，例如，或針對命令列可以用來取代圖形使用者介面) 的伺服器環境考慮。</span><span class="sxs-lookup"><span data-stu-id="73fda-204">Exceptions to this include accessibility considerations (documenting keyboard equivalents of mouse actions, for example), and platform considerations (documenting for the tablet form factor, for example, or for server environments in which the command line can substitute for the graphical user interface).</span></span>

<span data-ttu-id="73fda-205">請記住，使用者通常不會覺得它們所遇到的問題與您一樣。</span><span class="sxs-lookup"><span data-stu-id="73fda-205">Remember that users often don't think of the problems they are encountering in exactly the same terms as you do.</span></span> <span data-ttu-id="73fda-206">例如，使用者可能會發現，將本身視為「帳戶」很奇怪。</span><span class="sxs-lookup"><span data-stu-id="73fda-206">For example, users may find it strange to think of themselves as an "account."</span></span> <span data-ttu-id="73fda-207">請務必設計您的搜尋和編制索引功能，然後再考慮可能的術語變化和同義字。</span><span class="sxs-lookup"><span data-stu-id="73fda-207">Be sure to design your search and indexing functionality, then, to account for likely terminology variations and synonyms.</span></span>

<span data-ttu-id="73fda-208">不過，在主要 UI 和說明系統之間，如果不相同，則詞彙應該非常類似。</span><span class="sxs-lookup"><span data-stu-id="73fda-208">Between the primary UI and the Help system, though, terms should be very similar if not identical.</span></span> <span data-ttu-id="73fda-209">當說明系統語言與其在螢幕上看到的內容不緊密關聯時，使用者可能會感到困惑。</span><span class="sxs-lookup"><span data-stu-id="73fda-209">Users can be confused when the Help system language doesn't correlate very closely to what they are seeing on the screen.</span></span>

### <a name="writing-compelling-help-link-text"></a><span data-ttu-id="73fda-210">撰寫吸引人的說明連結文字</span><span class="sxs-lookup"><span data-stu-id="73fda-210">Writing compelling Help link text</span></span>

<span data-ttu-id="73fda-211">當您從主要 UI 連結到說明主題時，請務必撰寫吸引人的說明連結文字。</span><span class="sxs-lookup"><span data-stu-id="73fda-211">When you link to a Help topic from your primary UI, be sure to write compelling Help link text.</span></span> <span data-ttu-id="73fda-212">清除和特定語言激勵信賴度。</span><span class="sxs-lookup"><span data-stu-id="73fda-212">Clear and specific language inspires confidence.</span></span> <span data-ttu-id="73fda-213">使用者傾向于將一般說明連結 (具有「說明」一字或「深入瞭解」的按鈕) 將不會產生正確的資訊，而不需要投入大量的時間。</span><span class="sxs-lookup"><span data-stu-id="73fda-213">Users tend to believe that generic Help links (a button with the word "Help" or "Learn more" on it) will not lead to the right information without a significant investment of time.</span></span>

<span data-ttu-id="73fda-214">**如果您只進行五件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="73fda-214">**If you do only five things...**</span></span>

1.  <span data-ttu-id="73fda-215">設計您的 UI，讓使用者不需要協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-215">Design your UI so that users don't need Help.</span></span>
2.  <span data-ttu-id="73fda-216">藉由將主要問題的內容放在目標使用者的最上層案例中，讓您的協助更加實用。</span><span class="sxs-lookup"><span data-stu-id="73fda-216">Make your Help helpful by focusing the content on the top questions in the top scenarios for your target users.</span></span>
3.  <span data-ttu-id="73fda-217">顯示說明內容，以便輕鬆地進行掃描。</span><span class="sxs-lookup"><span data-stu-id="73fda-217">Present the Help content so that it is easy to scan.</span></span>
4.  <span data-ttu-id="73fda-218">瞭解您不需要為 UI 中的每一項功能提供協助。</span><span class="sxs-lookup"><span data-stu-id="73fda-218">Understand that you don't have to provide help for every feature in the UI.</span></span>
5.  <span data-ttu-id="73fda-219">讓協助進入點可供探索且吸引人。</span><span class="sxs-lookup"><span data-stu-id="73fda-219">Make the Help entry points discoverable and compelling.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="73fda-220">使用模式</span><span class="sxs-lookup"><span data-stu-id="73fda-220">Usage patterns</span></span>

<span data-ttu-id="73fda-221">不同類型的內容提供不同的用途。</span><span class="sxs-lookup"><span data-stu-id="73fda-221">Different kinds of content serve different purposes.</span></span>



|                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73fda-222">**程式說明**</span><span class="sxs-lookup"><span data-stu-id="73fda-222">**Procedural Help**</span></span><br/> <span data-ttu-id="73fda-223">提供執行工作的步驟。</span><span class="sxs-lookup"><span data-stu-id="73fda-223">provides the steps for carrying out a task.</span></span> <br/>                       | <span data-ttu-id="73fda-224">程式說明應著重于「如何」資訊，而不是「什麼」或「原因」。</span><span class="sxs-lookup"><span data-stu-id="73fda-224">Procedural help should focus on "how" information rather than "what" or "why."</span></span> <br/> ![<span data-ttu-id="73fda-225">[刪除暫存檔案] 說明頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-225">screen shot of 'delete temporary files' help page</span></span> ](images/winenv-help-image2.png)<br/> <span data-ttu-id="73fda-226">在此範例中，「說明」主題說明如何使用「磁片清理公用程式」的功能，並提供依序執行的步驟。</span><span class="sxs-lookup"><span data-stu-id="73fda-226">In this example, the Help topic describes how to use a feature of the Disk Cleanup utility, providing steps to follow in sequence.</span></span><br/>                                              |
| <span data-ttu-id="73fda-227">**概念說明**</span><span class="sxs-lookup"><span data-stu-id="73fda-227">**Conceptual Help**</span></span><br/> <span data-ttu-id="73fda-228">提供背景資訊、功能總覽或流程。</span><span class="sxs-lookup"><span data-stu-id="73fda-228">provides background information, feature overviews, or processes.</span></span> <br/> | <span data-ttu-id="73fda-229">概念說明應提供完成工作所需的「什麼」或「原因」資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-229">Conceptual help should provide "what" or "why" information beyond that needed to complete a task.</span></span> <br/> ![<span data-ttu-id="73fda-230">[桌面 (總覽) ] 說明頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-230">screen shot of 'the desktop (overview)' help page</span></span> ](images/winenv-help-image3.png)<br/> <span data-ttu-id="73fda-231">在此範例中，說明主題會定義桌上型電腦的內容，並提供其包含內容以及使用者與其互動原因的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="73fda-231">In this example, the Help topic defines what the desktop is, and provides additional detail about what it contains and why users interact with it.</span></span><br/>           |
| <span data-ttu-id="73fda-232">**參考說明**</span><span class="sxs-lookup"><span data-stu-id="73fda-232">**Reference Help**</span></span><br/> <span data-ttu-id="73fda-233">作為線上參考書。</span><span class="sxs-lookup"><span data-stu-id="73fda-233">serves as an online reference book.</span></span> <br/>                                | <span data-ttu-id="73fda-234">您可以使用參考說明來記錄程式設計語言或程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="73fda-234">You can use reference help to document a programming language or programming interfaces.</span></span> <br/> ![<span data-ttu-id="73fda-235">[標記慣例] 說明頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-235">screen shot of 'notational conventions' help page</span></span> ](images/winenv-help-image4.png)<br/> <span data-ttu-id="73fda-236">在此範例中，說明主題會列出用於此特定語言或應用程式的印刷樣式慣例，並在容易掃描的表格中提供資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-236">In this example, the Help topic lists typographic conventions in use for this particular language or application, providing the information in an easy-to-scan table.</span></span><br/> |



 

## <a name="guidelines"></a><span data-ttu-id="73fda-237">指導方針</span><span class="sxs-lookup"><span data-stu-id="73fda-237">Guidelines</span></span>

### <a name="entry-points"></a><span data-ttu-id="73fda-238">進入點</span><span class="sxs-lookup"><span data-stu-id="73fda-238">Entry points</span></span>

-   <span data-ttu-id="73fda-239">**連結到特定的相關說明主題。**</span><span class="sxs-lookup"><span data-stu-id="73fda-239">**Link to specific, relevant Help topics.**</span></span> <span data-ttu-id="73fda-240">請勿連結至說明首頁、目錄、搜尋結果清單，或只連結至其他頁面的頁面。</span><span class="sxs-lookup"><span data-stu-id="73fda-240">Don't link to the Help home page, the table of contents, a list of search results, or a page that just links to other pages.</span></span> <span data-ttu-id="73fda-241">請避免連結到結構化為大型常見問題清單的頁面，因為它會強制使用者搜尋符合他們所選連結的頁面。</span><span class="sxs-lookup"><span data-stu-id="73fda-241">Avoid linking to pages structured as a large list of frequently asked questions, because it forces users to search for the one that matches the link they clicked.</span></span> <span data-ttu-id="73fda-242">請勿連結至與手邊無關的特定說明主題。</span><span class="sxs-lookup"><span data-stu-id="73fda-242">Don't link to specific Help topics that aren't relevant and helpful to the task at hand.</span></span> <span data-ttu-id="73fda-243">永遠不會連結到空白頁面。</span><span class="sxs-lookup"><span data-stu-id="73fda-243">Never link to empty pages.</span></span>
-   <span data-ttu-id="73fda-244">**請勿將說明連結放在每個視窗或頁面上以達到一致性。**</span><span class="sxs-lookup"><span data-stu-id="73fda-244">**Don't put Help links on every window or page for the sake of consistency.**</span></span> <span data-ttu-id="73fda-245">在一個地方提供說明連結並不表示您必須在所有地方提供它們。</span><span class="sxs-lookup"><span data-stu-id="73fda-245">Providing a Help link in one place doesn't mean that you have to provide them everywhere.</span></span>
-   <span data-ttu-id="73fda-246">**使用對話方塊、錯誤訊息、嚮導和屬性工作表的 [說明] 連結。**</span><span class="sxs-lookup"><span data-stu-id="73fda-246">**Use Help links for dialog boxes, error messages, wizards, and property sheets.**</span></span> <span data-ttu-id="73fda-247">如果說明連結適用于特定控制項，請將其放在其下靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="73fda-247">If the Help link applies to specific controls, place it under them, left-aligned.</span></span> <span data-ttu-id="73fda-248">如果 [說明] 連結套用至整個視窗，請將它放在視窗內容區域的左下角。</span><span class="sxs-lookup"><span data-stu-id="73fda-248">If the Help link applies to the entire window, place it at the bottom left corner of the window's content area.</span></span>

    ![<span data-ttu-id="73fda-249">具有群組方塊的屬性工作表螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-249">screen shot of property sheet with group box</span></span> ](images/winenv-help-image5.png)

    <span data-ttu-id="73fda-250">在此範例中，第二個說明連結會套用至控制項群組。</span><span class="sxs-lookup"><span data-stu-id="73fda-250">In this example, the second Help link applies to a group of controls.</span></span>

    ![<span data-ttu-id="73fda-251">[屬性工作表] 和 [說明] 連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-251">screen shot of property sheet and help link</span></span> ](images/winenv-help-image6.png)

    <span data-ttu-id="73fda-252">在此範例中，[說明] 連結會套用至整個視窗。</span><span class="sxs-lookup"><span data-stu-id="73fda-252">In this example, the Help link applies to the entire window.</span></span>

-   <span data-ttu-id="73fda-253">**您可以使用 [說明] 連結，而不是一般文字參考，以便在技術上可行時使用**</span><span class="sxs-lookup"><span data-stu-id="73fda-253">**Use Help links instead of generic textual references to Help whenever technically possible.**</span></span>

    <span data-ttu-id="73fda-254">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-254">**Correct:**</span></span>

    <span data-ttu-id="73fda-255">如何修復磁片錯誤？</span><span class="sxs-lookup"><span data-stu-id="73fda-255">How can I repair disk errors?</span></span>

    <span data-ttu-id="73fda-256">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-256">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-257">如需修復磁片錯誤的詳細資訊，請參閱說明及支援。</span><span class="sxs-lookup"><span data-stu-id="73fda-257">For more information about repairing disk errors, see Help and Support.</span></span>

-   <span data-ttu-id="73fda-258">**針對 [控制台] 專案的中樞頁面，使用 [說明] 按鈕和 [說明] 圖示。**</span><span class="sxs-lookup"><span data-stu-id="73fda-258">**Use a Help button with the Help icon for the hub pages of control panel items.**</span></span> <span data-ttu-id="73fda-259">將它放置在右上角。</span><span class="sxs-lookup"><span data-stu-id="73fda-259">Place it in the upper-right corner.</span></span> <span data-ttu-id="73fda-260">這些按鈕沒有標籤，但是具有可讀取說明的工具提示。</span><span class="sxs-lookup"><span data-stu-id="73fda-260">These buttons don't have a label, but have a tooltip that reads Help.</span></span>

    ![<span data-ttu-id="73fda-261">具有 [說明] 按鈕之控制台專案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-261">screen shot of control panel item with help button</span></span> ](images/winenv-help-image7.png)

    <span data-ttu-id="73fda-262">具有 [說明] 按鈕的 [控制台] 專案。</span><span class="sxs-lookup"><span data-stu-id="73fda-262">A control panel item with a Help button.</span></span>

-   <span data-ttu-id="73fda-263">**F1 說明是選擇性的。**</span><span class="sxs-lookup"><span data-stu-id="73fda-263">**F1 Help is optional.**</span></span> <span data-ttu-id="73fda-264">使用者習慣于透過按 F1 鍵（在標準鍵盤上標示為「說明」）來尋找與螢幕上 UI 立即內容相關的說明資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-264">Users have grown accustomed to finding Help information related to the immediate context of the UI on the screen by pressing the F1 key, which is labeled Help on standard keyboards.</span></span> <span data-ttu-id="73fda-265">如果您的使用方式研究顯示使用者預期會找到它，或您的程式 UI 很複雜，可受益于內容相關的協助，您可以包含 F1 說明。</span><span class="sxs-lookup"><span data-stu-id="73fda-265">You can include F1 Help if, for example, usability studies show that your users expect to find it, or your program UI is complex enough to benefit from contextual assistance.</span></span>
-   <span data-ttu-id="73fda-266">**具有功能表列的程式可以有 [說明] 功能表分類。**</span><span class="sxs-lookup"><span data-stu-id="73fda-266">**Programs with menu bars can have a Help menu category.**</span></span> <span data-ttu-id="73fda-267">如需說明功能表的指導方針，請參閱 [功能表](cmd-menus.md)。</span><span class="sxs-lookup"><span data-stu-id="73fda-267">For Help menu guidelines, see [Menus](cmd-menus.md).</span></span>

    ![<span data-ttu-id="73fda-268">從功能表列存取 [說明] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-268">screen shot of help accessed from menu bar</span></span> ](images/winenv-help-image8.png)

    <span data-ttu-id="73fda-269">在此範例中，Windows 繪圖配件有一個 [說明] 功能表類別。</span><span class="sxs-lookup"><span data-stu-id="73fda-269">In this example, the Windows Paint accessory has a Help menu category.</span></span>

-   <span data-ttu-id="73fda-270">**針對鍵盤協助工具，提供 [說明] 按鈕和連結的定位停駐點。**</span><span class="sxs-lookup"><span data-stu-id="73fda-270">**For keyboard accessibility, provide tab stops for Help buttons and links.**</span></span>
-   <span data-ttu-id="73fda-271">[說明] 按鈕和連結行為應如下所示： [說明] 窗格隨即開啟，並顯示專用的說明主題。叫用 [說明] 窗格的 UI 應該保持開啟狀態，以保留內容相關體驗。</span><span class="sxs-lookup"><span data-stu-id="73fda-271">Help button and link behavior should be as follows: Help pane opens and a dedicated Help topic is displayed; the UI that invoked the Help pane should remain open to preserve the contextual experience.</span></span>
-   <span data-ttu-id="73fda-272">**請勿使用下列過時的說明進入點樣式：「深入瞭解」或「深入瞭解 ...」標題列上的連結、一般說明按鈕，以及即時線上說明按鈕。**</span><span class="sxs-lookup"><span data-stu-id="73fda-272">**Don't use the following obsolete Help entry point styles: "Learn more" or "Learn more about..." links, generic Help buttons, and context-sensitive Help buttons on the title bar.**</span></span> <span data-ttu-id="73fda-273">雖然過去曾使用過這些功能，但可用性研究已判定使用者通常會忽略這些專案。</span><span class="sxs-lookup"><span data-stu-id="73fda-273">Although they have been used in the past, usability studies have determined that users tend to ignore them.</span></span> <span data-ttu-id="73fda-274">請改用特定說明主題的連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-274">Use links to specific Help topics instead.</span></span> <span data-ttu-id="73fda-275">如需撰寫良好說明連結的指導方針，請參閱說明 [連結](#text)。</span><span class="sxs-lookup"><span data-stu-id="73fda-275">For guidelines about writing good Help links, see [Help links](#text).</span></span>

    <span data-ttu-id="73fda-276">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-276">**Incorrect:**</span></span>

    ![<span data-ttu-id="73fda-277">具有 [深入瞭解] 連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-277">screen shot of dialog box with a 'learn more' link</span></span> ](images/winenv-help-image9.png)

    <span data-ttu-id="73fda-278">請勿使用「深入瞭解」或「深入瞭解 ...」連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-278">Don't use "Learn more" or "Learn more about..." links.</span></span>

    <span data-ttu-id="73fda-279">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-279">**Incorrect:**</span></span>

    ![<span data-ttu-id="73fda-280">[認可] 按鈕旁 [說明] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-280">screen shot of help button beside commit buttons</span></span> ](images/winenv-help-image10.png)

    <span data-ttu-id="73fda-281">請勿使用一般的 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="73fda-281">Don't use generic Help buttons.</span></span>

    <span data-ttu-id="73fda-282">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-282">**Incorrect:**</span></span>

    ![<span data-ttu-id="73fda-283">標題列上問號圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-283">screen shot of question-mark icon on title bar</span></span> ](images/winenv-help-image11.png)

    <span data-ttu-id="73fda-284">請勿使用標題列上的即時線上說明按鈕。</span><span class="sxs-lookup"><span data-stu-id="73fda-284">Don't use context-sensitive Help buttons on the title bar.</span></span>

### <a name="content"></a><span data-ttu-id="73fda-285">Content</span><span class="sxs-lookup"><span data-stu-id="73fda-285">Content</span></span>

-   <span data-ttu-id="73fda-286">**請勿建立明顯的內容。**</span><span class="sxs-lookup"><span data-stu-id="73fda-286">**Don't create obvious content.**</span></span> <span data-ttu-id="73fda-287">重複主要 UI 中的 [說明] 主題不會增加價值。</span><span class="sxs-lookup"><span data-stu-id="73fda-287">Help topics that repeat what is in the primary UI don't add value.</span></span>
-   <span data-ttu-id="73fda-288">**請勿建立使用者無法以某種方式採取行動的內容。**</span><span class="sxs-lookup"><span data-stu-id="73fda-288">**Don't create content that the user can't act on in some way.**</span></span>
    -   <span data-ttu-id="73fda-289">**例外狀況：** 有些概念內容會提供重要的背景資訊，而不一定會導致使用者的動作。</span><span class="sxs-lookup"><span data-stu-id="73fda-289">**Exception:** Some conceptual content delivers important background information without necessarily leading to user action.</span></span>
-   <span data-ttu-id="73fda-290">**避免發生問題的模糊解決問題。**</span><span class="sxs-lookup"><span data-stu-id="73fda-290">**Avoid vague resolutions to problems.**</span></span> <span data-ttu-id="73fda-291">例如，「洽詢您的系統管理員」或「重新安裝應用程式」通常會讓使用者感到不快。</span><span class="sxs-lookup"><span data-stu-id="73fda-291">For example, "contact your system administrator" or "reinstall the application" tend to frustrate users.</span></span>
    -   <span data-ttu-id="73fda-292">**例外狀況：** 如果這是唯一實用的解決方案，建議您聯繫系統管理員，系統管理員則會預期會與問題聯繫。</span><span class="sxs-lookup"><span data-stu-id="73fda-292">**Exception:** Recommend contacting the system administrator if that is the only practical solution, and system administrators expect to be contacted for the problem.</span></span>
-   <span data-ttu-id="73fda-293">**避免可解決極不太可能使用者案例的內容。**</span><span class="sxs-lookup"><span data-stu-id="73fda-293">**Avoid content that addresses highly unlikely user scenarios.**</span></span> <span data-ttu-id="73fda-294">針對您預期的一般使用方式，開發您的主要說明內容。請注意預期使用方式的重要例外狀況，但會將此內容視為較低的優先順序。</span><span class="sxs-lookup"><span data-stu-id="73fda-294">Develop your main Help content for what you anticipate will be normal usage; note important exceptions to expected usage, but treat this content as a lower priority.</span></span>
-   <span data-ttu-id="73fda-295">**收集您的使用者意見反應，瞭解您的說明主題有多有用。**</span><span class="sxs-lookup"><span data-stu-id="73fda-295">**Gather feedback from your users about how helpful your Help topics are.**</span></span> <span data-ttu-id="73fda-296">允許使用者對個別主題進行評分。</span><span class="sxs-lookup"><span data-stu-id="73fda-296">Allow users to rate individual topics.</span></span> <span data-ttu-id="73fda-297">在您的檔上進行 [可用性研究](glossary.md) ，以確定涉及品質和內容可搜尋性的問題。</span><span class="sxs-lookup"><span data-stu-id="73fda-297">Conduct [usability studies](glossary.md) on your documentation to ascertain problems involving quality and discoverability of content.</span></span>
    -   <span data-ttu-id="73fda-298">**秘訣：** 使用者意見反應也是產生更多以工作為基礎之內容的好方法，著重于使用者實際使用您的程式，而不是以功能為基礎的內容，只著重于技術的描述。</span><span class="sxs-lookup"><span data-stu-id="73fda-298">**Tip:** User feedback is also a great way to generate more task-based content, focused on what users are actually doing with your program, as opposed to feature-based content, focused simply on a description of the technology.</span></span>
-   <span data-ttu-id="73fda-299">**提供多種方式來存取您的內容。**</span><span class="sxs-lookup"><span data-stu-id="73fda-299">**Provide multiple ways of accessing your content.**</span></span> <span data-ttu-id="73fda-300">目錄、索引和 [搜尋](ctrl-search-boxes.md) 機制是改善探索能力的三種最常見方法。</span><span class="sxs-lookup"><span data-stu-id="73fda-300">A table of contents, an index, and a [search](ctrl-search-boxes.md) mechanism are three of the most common methods of improving discoverability.</span></span>
-   <span data-ttu-id="73fda-301">**如果有一種以上的方法可以執行工作，則在大部分情況下，您可以只記錄缺乏經驗的使用者所使用的最常見方式。**</span><span class="sxs-lookup"><span data-stu-id="73fda-301">**If there is more than one way to perform a task, in most cases you can just document the most common way used by inexperienced users.**</span></span>

### <a name="icons"></a><span data-ttu-id="73fda-302">圖示</span><span class="sxs-lookup"><span data-stu-id="73fda-302">Icons</span></span>

-   <span data-ttu-id="73fda-303">只針對 Explorer 視窗和 [控制台] 專案的 [中樞] 頁面使用 [說明] 圖示。</span><span class="sxs-lookup"><span data-stu-id="73fda-303">Use the Help icon only for Explorer windows and the hub pages of control panel items.</span></span> <span data-ttu-id="73fda-304">請勿將說明圖示用於說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-304">Don't use the Help icon with Help links.</span></span>

<span data-ttu-id="73fda-305">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-305">**Correct:**</span></span>

![<span data-ttu-id="73fda-306">具有問號圖示之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-306">screen shot of window with question-mark icon</span></span> ](images/winenv-help-image12.png)

<span data-ttu-id="73fda-307">在此範例中，Windows 檔案總管視窗會使用說明圖示來提供協助的存取權。</span><span class="sxs-lookup"><span data-stu-id="73fda-307">In this example, a Windows Explorer window uses a Help icon to provide access to Help.</span></span>

<span data-ttu-id="73fda-308">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-308">**Incorrect:**</span></span>

![<span data-ttu-id="73fda-309">左面板中具有說明圖示之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-309">screen shot of window with help icon in left panel</span></span> ](images/winenv-help-image13.png)

<span data-ttu-id="73fda-310">在此範例中，左下角的 [說明] 圖示會以不正確的方式使用說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-310">In this example, the Help icon on the lower-left is used incorrectly with a Help link.</span></span>

## <a name="text"></a><span data-ttu-id="73fda-311">Text</span><span class="sxs-lookup"><span data-stu-id="73fda-311">Text</span></span>

<span data-ttu-id="73fda-312">**說明連結**</span><span class="sxs-lookup"><span data-stu-id="73fda-312">**Help links**</span></span>

-   <span data-ttu-id="73fda-313">提供與說明主題內容相關的特定資訊，視需要使用盡可能精確的文字。</span><span class="sxs-lookup"><span data-stu-id="73fda-313">Provide specific information about the content of the Help topic, using as much relevant, concise text as necessary.</span></span> <span data-ttu-id="73fda-314">使用者通常會忽略一般說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-314">Users often ignore generic Help links.</span></span> <span data-ttu-id="73fda-315">請確定連結的結果是可預測的使用者，結果不應驚訝。</span><span class="sxs-lookup"><span data-stu-id="73fda-315">Make sure the results of the link are predictable users shouldn't be surprised by the results.</span></span>

    -   <span data-ttu-id="73fda-316">**例外狀況：** 您可以使用 [詳細資訊] 來補充直接在 UI 中的指示，特別是如果在 [說明] 連結中提供特定資訊會導致不必要的重複，或讓連結較不吸引人。</span><span class="sxs-lookup"><span data-stu-id="73fda-316">**Exception:** You can use "More information" to supplement instructions that are directly in the UI, especially if providing specific information in the Help link leads to unnecessary repetition or makes the link less compelling.</span></span>

    <span data-ttu-id="73fda-317">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-317">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-318">強式密碼具有至少六個混合的大寫字母、數位及符號。</span><span class="sxs-lookup"><span data-stu-id="73fda-318">A strong password has at least six mixed-case letters, numbers, and symbols.</span></span> <span data-ttu-id="73fda-319">什麼是強式密碼？</span><span class="sxs-lookup"><span data-stu-id="73fda-319">What is a strong password?</span></span>

    <span data-ttu-id="73fda-320">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-320">**Correct:**</span></span>

    <span data-ttu-id="73fda-321">強式密碼具有至少六個混合的大寫字母、數位及符號。</span><span class="sxs-lookup"><span data-stu-id="73fda-321">A strong password has at least six mixed-case letters, numbers, and symbols.</span></span> <span data-ttu-id="73fda-322">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="73fda-322">More information</span></span>

    <span data-ttu-id="73fda-323">在不正確的範例中，說明連結是重複的。</span><span class="sxs-lookup"><span data-stu-id="73fda-323">In the incorrect example, the Help link is repetitive.</span></span> <span data-ttu-id="73fda-324">它會詢問已回答的問題。</span><span class="sxs-lookup"><span data-stu-id="73fda-324">It asks a question that is really already answered.</span></span>

-   <span data-ttu-id="73fda-325">在可能的情況下，請在說明內容所回答的主要問題方面，片語說明連結文字。</span><span class="sxs-lookup"><span data-stu-id="73fda-325">Whenever possible, phrase Help link text in terms of the primary question answered by the Help content.</span></span> <span data-ttu-id="73fda-326">請勿使用「深入瞭解」、「告訴我更多資訊」或「取得此措辭的協助」。</span><span class="sxs-lookup"><span data-stu-id="73fda-326">Don't use "Learn more about," "Tell me more about," or "Get help with this" phrasing.</span></span>

    <span data-ttu-id="73fda-327">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-327">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-328">深入瞭解如何新增例外狀況</span><span class="sxs-lookup"><span data-stu-id="73fda-328">Learn more about adding exceptions</span></span>

    <span data-ttu-id="73fda-329">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-329">**Correct:**</span></span>

    <span data-ttu-id="73fda-330">允許例外狀況的風險有哪些？</span><span class="sxs-lookup"><span data-stu-id="73fda-330">What are the risks of allowing exceptions?</span></span>

    <span data-ttu-id="73fda-331">如何? 新增例外狀況？</span><span class="sxs-lookup"><span data-stu-id="73fda-331">How do I add exceptions?</span></span>

    <span data-ttu-id="73fda-332">在正確的範例中，連結的片語是說明主題所回答的主要問題。</span><span class="sxs-lookup"><span data-stu-id="73fda-332">In the correct examples, the link is phrased in terms of the primary question answered by the Help topic.</span></span>

-   <span data-ttu-id="73fda-333">如果您可以簡潔地摘要最相關的資訊，請將摘要直接放在 UI 中，而不是使用說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-333">If the most relevant information can be summarized succinctly, put the summary directly in the UI instead of using a Help link.</span></span> <span data-ttu-id="73fda-334">不過，您可以使用 [說明] 連結來提供補充資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-334">However, you can use a Help link to provide supplemental information.</span></span>

    <span data-ttu-id="73fda-335">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-335">**Incorrect:**</span></span>

    ![<span data-ttu-id="73fda-336">[強式密碼] 連結的螢幕擷取畫面？</span><span class="sxs-lookup"><span data-stu-id="73fda-336">screen shot of link to what is a strong password?</span></span> ](images/winenv-help-image14.png)

    <span data-ttu-id="73fda-337">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-337">**Correct:**</span></span>

    ![<span data-ttu-id="73fda-338">有關密碼的補充文字螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-338">screen shot of supplemental text about passwords</span></span> ](images/winenv-help-image15.png)

    <span data-ttu-id="73fda-339">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="73fda-339">**Better:**</span></span>

    ![<span data-ttu-id="73fda-340">具有詳細資訊連結的文字螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="73fda-340">screen shot of text with link to more information</span></span> ](images/winenv-help-image16.png)

    <span data-ttu-id="73fda-341">正確的範例會簡潔地摘要說明資訊，大幅改善使用者將讀取此資訊的可能性。</span><span class="sxs-lookup"><span data-stu-id="73fda-341">The correct example summarizes the Help information succinctly, greatly improving the likelihood that users will read it.</span></span> <span data-ttu-id="73fda-342">更好的範例會提供 [說明] 連結，以取得此複雜主題的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="73fda-342">The better example provides a Help link for more information on this complex subject.</span></span>

-   <span data-ttu-id="73fda-343">清楚指出協助的片語說明連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-343">Phrase Help links to clearly indicate assistance.</span></span> <span data-ttu-id="73fda-344">說明連結絕對不能像動作連結一樣閱讀。</span><span class="sxs-lookup"><span data-stu-id="73fda-344">Help links should never read like action links.</span></span>
-   <span data-ttu-id="73fda-345">使用連結文字的整個說明連結，而不只是關鍵字。</span><span class="sxs-lookup"><span data-stu-id="73fda-345">Use the entire Help link for the link text, not just the keywords.</span></span>

    <span data-ttu-id="73fda-346">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-346">**Correct:**</span></span>

    <span data-ttu-id="73fda-347">允許例外狀況的風險有哪些？</span><span class="sxs-lookup"><span data-stu-id="73fda-347">What are the risks of allowing exceptions?</span></span>

    <span data-ttu-id="73fda-348">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-348">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-349">允許例外狀況的風險有哪些？</span><span class="sxs-lookup"><span data-stu-id="73fda-349">What are the risks of allowing exceptions?</span></span>

    <span data-ttu-id="73fda-350">在正確的範例中，連結文字會使用整個說明連結句子。</span><span class="sxs-lookup"><span data-stu-id="73fda-350">In the correct example, the entire Help link sentence is used for the link text.</span></span>

    -   <span data-ttu-id="73fda-351">**例外狀況：** 外部網站的 [說明] 連結應該只使用網站或頁面的名稱做為連結。</span><span class="sxs-lookup"><span data-stu-id="73fda-351">**Exception:** Help links to external Web sites should simply use the name of the site or page as the link.</span></span> <span data-ttu-id="73fda-352">任何導入網站名稱的文字都不需要包含在連結本身。</span><span class="sxs-lookup"><span data-stu-id="73fda-352">Any text introducing the name of the site need not be included in the link itself.</span></span>

-   <span data-ttu-id="73fda-353">說明連結不需要完全符合說明主題標題，但是兩者之間應該有很強且明顯的連接。</span><span class="sxs-lookup"><span data-stu-id="73fda-353">Help links don't have to match Help topic headings exactly, but there should be a strong and obvious connection between the two.</span></span> <span data-ttu-id="73fda-354">基於這個原因，設計成對的連結和標題。</span><span class="sxs-lookup"><span data-stu-id="73fda-354">Design links and headings in pairs for this reason.</span></span>

    <span data-ttu-id="73fda-355">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-355">**Correct:**</span></span>

    <span data-ttu-id="73fda-356">如何改進這項功能的效能？</span><span class="sxs-lookup"><span data-stu-id="73fda-356">How can I improve the performance of this feature?</span></span> <span data-ttu-id="73fda-357"> (連結文字) </span><span class="sxs-lookup"><span data-stu-id="73fda-357">(link text)</span></span>

    <span data-ttu-id="73fda-358">設定這項功能以獲得最佳效能 (主題標題) </span><span class="sxs-lookup"><span data-stu-id="73fda-358">Configuring this feature for optimal performance (topic heading)</span></span>

    <span data-ttu-id="73fda-359">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-359">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-360">如何改進這項功能的效能？</span><span class="sxs-lookup"><span data-stu-id="73fda-360">How can I improve the performance of this feature?</span></span> <span data-ttu-id="73fda-361"> (連結文字) </span><span class="sxs-lookup"><span data-stu-id="73fda-361">(link text)</span></span>

    <span data-ttu-id="73fda-362">本功能的完整總覽 (主題標題) </span><span class="sxs-lookup"><span data-stu-id="73fda-362">Complete overview of this feature (topic heading)</span></span>

    <span data-ttu-id="73fda-363">在不正確的範例中，[說明] 主題標題的範圍明顯不同于 [說明] 連結文字的範圍，而且可能會 disorienting。</span><span class="sxs-lookup"><span data-stu-id="73fda-363">In the incorrect example, the Help topic heading substantially differs in scope from the Help link text, and could be disorienting.</span></span>

-   <span data-ttu-id="73fda-364">如果說明內容已上線，請在連結文字中將其清除。</span><span class="sxs-lookup"><span data-stu-id="73fda-364">If the Help content is online, make that clear in the link text.</span></span> <span data-ttu-id="73fda-365">這樣做有助於讓連結的結果成為可預測的結果。</span><span class="sxs-lookup"><span data-stu-id="73fda-365">Doing so helps make the result of the links predictable.</span></span>

    <span data-ttu-id="73fda-366">**正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-366">**Correct:**</span></span>

    <span data-ttu-id="73fda-367">如需其他格式和工具，請移至 Microsoft 網站。</span><span class="sxs-lookup"><span data-stu-id="73fda-367">For additional formats and tools, go to the Microsoft Web site.</span></span>

    <span data-ttu-id="73fda-368">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="73fda-368">**Incorrect:**</span></span>

    <span data-ttu-id="73fda-369">我可以在哪裡找到其他格式與工具？</span><span class="sxs-lookup"><span data-stu-id="73fda-369">Where can I find additional formats and tools?</span></span>

-   <span data-ttu-id="73fda-370">使用完整句子。</span><span class="sxs-lookup"><span data-stu-id="73fda-370">Use complete sentences.</span></span>
-   <span data-ttu-id="73fda-371">請勿使用結尾標點符號，但問號除外。</span><span class="sxs-lookup"><span data-stu-id="73fda-371">Don't use ending punctuation, except for question marks.</span></span>
-   <span data-ttu-id="73fda-372">請勿使用省略號來取得說明連結或命令。</span><span class="sxs-lookup"><span data-stu-id="73fda-372">Don't use ellipses for Help links or commands.</span></span>

<span data-ttu-id="73fda-373">**說明內容**</span><span class="sxs-lookup"><span data-stu-id="73fda-373">**Help content**</span></span>

-   <span data-ttu-id="73fda-374">使用粗體將 UI 元素格式化，以方便識別。</span><span class="sxs-lookup"><span data-stu-id="73fda-374">Format UI elements using bold to make them easy to identify.</span></span> <span data-ttu-id="73fda-375">這特別適用于程式說明主題，可讓使用者透過程式進行掃描，並快速查看相關的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="73fda-375">This is especially useful for procedural Help topics, allowing users to scan through procedures and quickly see pertinent UI elements.</span></span>
-   <span data-ttu-id="73fda-376">使用斜體格式化字幕。</span><span class="sxs-lookup"><span data-stu-id="73fda-376">Format captions using italic.</span></span> <span data-ttu-id="73fda-377">這適用于從簡短文字說明中獲益的資料表、美工圖案、螢幕擷取畫面和其他圖形元素。</span><span class="sxs-lookup"><span data-stu-id="73fda-377">This applies to tables, art, screenshots, and other graphic elements that benefit from brief textual explanation.</span></span>
-   <span data-ttu-id="73fda-378">如需說明，請參閱 [說明]。</span><span class="sxs-lookup"><span data-stu-id="73fda-378">Refer to Help simply as Help.</span></span> <span data-ttu-id="73fda-379">一般而言，除非您實際參考網站上的內容，否則請不要使用「線上說明」片語。</span><span class="sxs-lookup"><span data-stu-id="73fda-379">Generally, don't use the phrase online Help unless you are in fact referring to content on your Web site.</span></span>

 

