---
title: 首次執行經驗
description: 在理想的第一個經驗中，使用者會立即安裝您的程式並立即使用它，而不需要回答一連串問題或學習一大堆問題。
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c965ae77507b0041d17cabb34c4f53dc8216c134
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195692"
---
# <a name="first-experience"></a><span data-ttu-id="e5b99-103">首次執行經驗</span><span class="sxs-lookup"><span data-stu-id="e5b99-103">First Experience</span></span>

> [!NOTE]
> <span data-ttu-id="e5b99-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="e5b99-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="e5b99-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="e5b99-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="e5b99-106">在理想的第一個經驗中，使用者會立即安裝您的程式並立即使用它，而不需要回答一連串問題或學習一大堆問題。</span><span class="sxs-lookup"><span data-stu-id="e5b99-106">In the ideal first experience, users install your program and use it productively immediately, without answering a bunch of questions or learning a bunch of things.</span></span>

<span data-ttu-id="e5b99-107">第一個體驗使用者介面可協助使用者從第一次暴露到新程式或功能，再轉換成日常使用。</span><span class="sxs-lookup"><span data-stu-id="e5b99-107">A first experience user interface helps users transition from their first exposure to a new program or feature to everyday usage.</span></span>

<span data-ttu-id="e5b99-108">針對 Windows 程式，當使用者執行安裝程式時，會發生初次首次體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-108">For Windows programs, the initial first experience occurs when users run the Setup program.</span></span> <span data-ttu-id="e5b99-109">安裝程式通常：</span><span class="sxs-lookup"><span data-stu-id="e5b99-109">Setup programs typically:</span></span>

-   <span data-ttu-id="e5b99-110">要求使用者接受 (EULA) 的使用者授權合約。</span><span class="sxs-lookup"><span data-stu-id="e5b99-110">Require the user to accept an End User License Agreement (EULA).</span></span>
-   <span data-ttu-id="e5b99-111">索取產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5b99-111">Ask for a product key.</span></span>
-   <span data-ttu-id="e5b99-112">顯示必要的設定相關選項，包括安裝選用的軟體。</span><span class="sxs-lookup"><span data-stu-id="e5b99-112">Present required configuration-related options, including installation of optional software.</span></span>
-   <span data-ttu-id="e5b99-113">將軟體複製到使用者的硬碟。</span><span class="sxs-lookup"><span data-stu-id="e5b99-113">Copy the software to the user's hard disk.</span></span>
-   <span data-ttu-id="e5b99-114">提供適用于所有使用者的程式選項。</span><span class="sxs-lookup"><span data-stu-id="e5b99-114">Present program options that apply to all users.</span></span>

![<span data-ttu-id="e5b99-115">[輸入產品金鑰] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-115">screen shot of 'type your product key' dialog box</span></span> ](images/exper-first-exper-image1.png)

<span data-ttu-id="e5b99-116">一般 Windows 安裝經驗的一部分。</span><span class="sxs-lookup"><span data-stu-id="e5b99-116">Part of a typical Windows setup experience.</span></span>

<span data-ttu-id="e5b99-117">第一個經驗接著會繼續使用程式或功能。</span><span class="sxs-lookup"><span data-stu-id="e5b99-117">The first experience then continues to the first use of the program or feature.</span></span> <span data-ttu-id="e5b99-118">第一次使用體驗可以：</span><span class="sxs-lookup"><span data-stu-id="e5b99-118">This first use experience can:</span></span>

-   <span data-ttu-id="e5b99-119">提供僅適用于目前使用者的程式選項。</span><span class="sxs-lookup"><span data-stu-id="e5b99-119">Present program options that apply only to the current user.</span></span>
-   <span data-ttu-id="e5b99-120">提供產品或功能教學課程。</span><span class="sxs-lookup"><span data-stu-id="e5b99-120">Offer product or feature tutorials.</span></span>

![<span data-ttu-id="e5b99-121">[歡迎中心] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-121">screen shot of 'welcome center' dialog box</span></span> ](images/exper-first-exper-image2.png)

<span data-ttu-id="e5b99-122">第一個使用體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-122">The first use experience.</span></span>

<span data-ttu-id="e5b99-123">**注意：**[程式選項](win-property-win.md)的相關指導方針會以個別文章的形式出現。</span><span class="sxs-lookup"><span data-stu-id="e5b99-123">**Note:** Guidelines related to [program options](win-property-win.md) are presented in a separate article.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="e5b99-124">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="e5b99-124">Is this the right user interface?</span></span>

<span data-ttu-id="e5b99-125">若要決定，請考慮下列問題。</span><span class="sxs-lookup"><span data-stu-id="e5b99-125">To decide, consider the following questions.</span></span>

### <a name="setup-experience"></a><span data-ttu-id="e5b99-126">設定體驗</span><span class="sxs-lookup"><span data-stu-id="e5b99-126">Setup experience</span></span>

<span data-ttu-id="e5b99-127">適用下列條件嗎？</span><span class="sxs-lookup"><span data-stu-id="e5b99-127">Do the following conditions apply?</span></span>

-   <span data-ttu-id="e5b99-128">使用程式需要正確的設定，並套用至所有使用者。</span><span class="sxs-lookup"><span data-stu-id="e5b99-128">The correct settings are required to use the program, and they apply to all users.</span></span>
-   <span data-ttu-id="e5b99-129">這些設定會自訂核心體驗，或自訂對使用者個人身分識別的重要體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-129">The settings customize a core experience, or one that is crucial to the user's personal identification with the program.</span></span>
-   <span data-ttu-id="e5b99-130">沒有安全的預設值，使用者可能會選擇不是預設值的設定，或預設設定需要使用者同意。</span><span class="sxs-lookup"><span data-stu-id="e5b99-130">There is no safe default, the user is likely to choose settings that aren't the default, or the default settings require user consent.</span></span>
-   <span data-ttu-id="e5b99-131">在安裝之後，使用者不太可能會變更設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-131">The user is unlikely to change settings after setup.</span></span>
-   <span data-ttu-id="e5b99-132">變更設定需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="e5b99-132">Changing the settings requires elevation.</span></span>

<span data-ttu-id="e5b99-133">如果是，請考慮在安裝體驗期間呈現設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-133">If so, consider presenting the settings during the setup experience.</span></span>

### <a name="first-use-experience"></a><span data-ttu-id="e5b99-134">首次使用體驗</span><span class="sxs-lookup"><span data-stu-id="e5b99-134">First use experience</span></span>

<span data-ttu-id="e5b99-135">適用下列條件嗎？</span><span class="sxs-lookup"><span data-stu-id="e5b99-135">Do the following conditions apply?</span></span>

-   <span data-ttu-id="e5b99-136">使用程式或功能時，需要正確的設定或工作，並將它們套用至個別使用者。</span><span class="sxs-lookup"><span data-stu-id="e5b99-136">The correct settings or tasks are required to use the program or feature, and they apply to individual users.</span></span>
-   <span data-ttu-id="e5b99-137">這些設定會自訂核心體驗，或自訂對使用者個人身分識別的重要體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-137">The settings customize a core experience, or one that is crucial to the user's personal identification with the program.</span></span>
-   <span data-ttu-id="e5b99-138">沒有安全的預設值，使用者可能會選擇不是預設值的設定，或預設設定需要使用者同意。</span><span class="sxs-lookup"><span data-stu-id="e5b99-138">There is no safe default, the user is likely to choose settings that aren't the default, or the default settings require user consent.</span></span>
-   <span data-ttu-id="e5b99-139">在程式的內容中，使用者可能會比安裝程式更好的選擇。</span><span class="sxs-lookup"><span data-stu-id="e5b99-139">Users are likely to make better choices within the context of the program than within setup.</span></span>
-   <span data-ttu-id="e5b99-140">使用者不太可能使用選項來變更設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-140">The user is unlikely to change settings using Options.</span></span>

<span data-ttu-id="e5b99-141">如果是的話，請考慮在第一次使用程式或功能時，呈現工作和設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-141">If so, consider presenting the tasks and settings during the first use experience of the program or feature.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="e5b99-142">設計概念</span><span class="sxs-lookup"><span data-stu-id="e5b99-142">Design concepts</span></span>

<span data-ttu-id="e5b99-143">在理想的第一個經驗中，使用者安裝您的程式 (或甚至是在不需要安裝) 的情況下啟動，並立即以有效率的方式使用它，而不需回答一連串問題或學習一堆問題。</span><span class="sxs-lookup"><span data-stu-id="e5b99-143">In the ideal first experience, users install your program (or even just start it if it doesn't require installation) and use it productively immediately without answering a bunch of questions or learning a bunch of things.</span></span>

<span data-ttu-id="e5b99-144">這很適合用於大部分的程式，因此您應該在可以的情況下，盡力取得這項理想的體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-144">This ideal is obtainable for most programs, so you should strive for this ideal experience whenever you can.</span></span> <span data-ttu-id="e5b99-145">不過，對於需要大量系統整合、有許多選用功能或有隱私權含意的程式來說，通常無法使用這個目標。</span><span class="sxs-lookup"><span data-stu-id="e5b99-145">However, this goal is often not obtainable for programs that require significant system integration, have many optional features, or have privacy implications.</span></span> <span data-ttu-id="e5b99-146">例如，如果您的程式具有可能會向未受信任的物件顯示個人資訊的功能，則可 [信賴](https://www.microsoft.com/mscorp/twc/default.mspx) 運算的原則會要求您先取得使用者同意，才能啟用這些功能。</span><span class="sxs-lookup"><span data-stu-id="e5b99-146">For example, if your program has features that might reveal personal information to untrusted parties, the tenets of [trustworthy computing](https://www.microsoft.com/mscorp/twc/default.mspx) require that you obtain user consent before enabling these features.</span></span>

### <a name="questions-arent-choices"></a><span data-ttu-id="e5b99-147">問題不是選擇</span><span class="sxs-lookup"><span data-stu-id="e5b99-147">Questions aren't choices</span></span>

<span data-ttu-id="e5b99-148">問題需要回應，使用者才能繼續。</span><span class="sxs-lookup"><span data-stu-id="e5b99-148">Questions require responses they must be answered before users can proceed.</span></span> <span data-ttu-id="e5b99-149">第一次體驗期間的問題是使用者必須跳過的問題，使用者才能有效率地使用您的程式。</span><span class="sxs-lookup"><span data-stu-id="e5b99-149">Questions during the first experience are hurdles that users must jump over before they can use your program productively.</span></span> <span data-ttu-id="e5b99-150">相反地，選擇是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e5b99-150">By contrast, choices are optional.</span></span> <span data-ttu-id="e5b99-151">使用者不需要對其進行回應，也可以選擇只在想要時查看。</span><span class="sxs-lookup"><span data-stu-id="e5b99-151">Users don't have to respond to them, or can choose to see them only when they want to.</span></span>

<span data-ttu-id="e5b99-152">因此，在安裝程式的主要流程中所顯示的設定是問題，而主要設定流程之外或 [程式選項] 對話方塊中的設定則是選擇。</span><span class="sxs-lookup"><span data-stu-id="e5b99-152">Thus, settings presented in the main flow of a setup wizard are questions, whereas settings outside the main setup flow or in a program options dialog box are choices.</span></span> <span data-ttu-id="e5b99-153">不必要的問題讓程式的第一次體驗變得繁瑣且冗長，有效地免除使用者開始使用您的程式時的正面預期和驚喜。</span><span class="sxs-lookup"><span data-stu-id="e5b99-153">Unnecessary questions make your program's first experience cumbersome and long, effectively eliminating the positive anticipation and excitement users have about getting started with your program.</span></span>

### <a name="use-the-first-experience-when-you-must"></a><span data-ttu-id="e5b99-154">當您需要時，請使用第一次體驗</span><span class="sxs-lookup"><span data-stu-id="e5b99-154">Use the first experience when you must</span></span>

<span data-ttu-id="e5b99-155">當您必須在第一次體驗期間向使用者呈現設定和工作，但通常有更好的替代方案：</span><span class="sxs-lookup"><span data-stu-id="e5b99-155">Present settings and tasks to users during the first experiences when you must, but usually there are better alternatives:</span></span>



|                                             |                                                                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b99-156">**首次體驗**</span><span class="sxs-lookup"><span data-stu-id="e5b99-156">**First experience**</span></span><br/>             | <span data-ttu-id="e5b99-157">**替代方案**</span><span class="sxs-lookup"><span data-stu-id="e5b99-157">**Alternatives**</span></span><br/>                                                                                                                        |
| <span data-ttu-id="e5b99-158">設定問題</span><span class="sxs-lookup"><span data-stu-id="e5b99-158">Setup questions</span></span><br/>                  | <span data-ttu-id="e5b99-159">選取適當的預設值。</span><span class="sxs-lookup"><span data-stu-id="e5b99-159">Select appropriate defaults.</span></span><br/> <span data-ttu-id="e5b99-160">允許使用者從程式選項變更。</span><span class="sxs-lookup"><span data-stu-id="e5b99-160">Allow users to change from program options.</span></span><br/> <span data-ttu-id="e5b99-161">提供一般的 vs 自訂安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="e5b99-161">Provide typical vs. custom setup paths.</span></span> <br/> |
| <span data-ttu-id="e5b99-162">第一個使用問題</span><span class="sxs-lookup"><span data-stu-id="e5b99-162">First use questions</span></span><br/>              | <span data-ttu-id="e5b99-163">選取適當的預設值，並允許使用者從程式選項變更。</span><span class="sxs-lookup"><span data-stu-id="e5b99-163">Select appropriate defaults, and allow users to change from program options.</span></span><br/>                                                            |
| <span data-ttu-id="e5b99-164">第一次使用工作</span><span class="sxs-lookup"><span data-stu-id="e5b99-164">First use tasks</span></span><br/>                  | <span data-ttu-id="e5b99-165">改為呈現內容。</span><span class="sxs-lookup"><span data-stu-id="e5b99-165">Present contextually instead.</span></span><br/>                                                                                                           |
| <span data-ttu-id="e5b99-166">首次使用功能公告</span><span class="sxs-lookup"><span data-stu-id="e5b99-166">First use feature advertisements</span></span><br/> | <span data-ttu-id="e5b99-167">讓最常見且最重要的工作更容易探索和內容相關。</span><span class="sxs-lookup"><span data-stu-id="e5b99-167">Make the most common and important tasks discoverable and contextual.</span></span><br/>                                                                   |
| <span data-ttu-id="e5b99-168">第一個使用教學課程</span><span class="sxs-lookup"><span data-stu-id="e5b99-168">First use tutorials</span></span><br/>              | <span data-ttu-id="e5b99-169">使程式功能一目了然。</span><span class="sxs-lookup"><span data-stu-id="e5b99-169">Make program features self-explanatory.</span></span><br/>                                                                                                 |
| <span data-ttu-id="e5b99-170">產品註冊</span><span class="sxs-lookup"><span data-stu-id="e5b99-170">Product registration</span></span><br/>             | <span data-ttu-id="e5b99-171">在 [說明] 功能表和 [關於] 方塊中提供命令。</span><span class="sxs-lookup"><span data-stu-id="e5b99-171">Provide command in Help menu and About box.</span></span><br/>                                                                                             |



 

<span data-ttu-id="e5b99-172">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-172">**If you do only one thing...**</span></span>

<span data-ttu-id="e5b99-173">儘量簡化您的第一個經驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-173">Keep your first experience as simple as possible.</span></span> <span data-ttu-id="e5b99-174">立即讓您的程式正常運作。</span><span class="sxs-lookup"><span data-stu-id="e5b99-174">Get your program working right away.</span></span> <span data-ttu-id="e5b99-175">選擇安全、安全、方便使用的預設值，並在安裝期間詢問問題，並只在您必須時才使用。</span><span class="sxs-lookup"><span data-stu-id="e5b99-175">Choose safe, secure, convenient defaults and ask questions during setup and first use only when you must.</span></span>

<span data-ttu-id="e5b99-176">您只有一個機會可以成為良好的第一印象，而第一印象是持續的印象。</span><span class="sxs-lookup"><span data-stu-id="e5b99-176">You have only one chance to make a good first impression and that first impression is lasting.</span></span>

## <a name="guidelines"></a><span data-ttu-id="e5b99-177">指導方針</span><span class="sxs-lookup"><span data-stu-id="e5b99-177">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="e5b99-178">一般</span><span class="sxs-lookup"><span data-stu-id="e5b99-178">General</span></span>

-   <span data-ttu-id="e5b99-179">**限制使用程式或功能所需之工作和設定的第一種體驗，而且只有在沒有更好的替代方案時才包含這些專案。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-179">**Limit first experiences to tasks and settings required to use a program or feature, and only include these when there is no better alternative.**</span></span> <span data-ttu-id="e5b99-180">請參閱上表以瞭解替代方案。</span><span class="sxs-lookup"><span data-stu-id="e5b99-180">See the previous table for alternatives.</span></span>
    -   <span data-ttu-id="e5b99-181">**例外狀況：** 將個人化或程式自訂設定新增至第一個體驗，如果他們的自訂是核心體驗的一部分，或對使用者的個人身分識別來說很重要。</span><span class="sxs-lookup"><span data-stu-id="e5b99-181">**Exception:** Add personalization or program customization settings to the first experience if their customization is part of the core experience or crucial to the user's personal identification with the program.</span></span>

![<span data-ttu-id="e5b99-182">[輸入電腦名稱稱] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-182">screen shot of 'type a computer name' dialog box</span></span> ](images/exper-first-exper-image3.png)

<span data-ttu-id="e5b99-183">Windows 會在安裝期間要求使用者輸入電腦名稱稱和選擇背景，因為這些設定有助於形成與產品的情緒連接。</span><span class="sxs-lookup"><span data-stu-id="e5b99-183">Windows asks users for the computer name and choice of background during setup because these settings help form an emotional connection to the product.</span></span>

-   <span data-ttu-id="e5b99-184">如果工作和設定適用于所有使用者，或變更設定需要提高許可權，**請使用其安裝體驗**。</span><span class="sxs-lookup"><span data-stu-id="e5b99-184">**Use the setup experience** for tasks and settings if they apply to all users or changing settings requires elevation.</span></span>
-   <span data-ttu-id="e5b99-185">如果工作和設定適用于個別使用者，**請使用第一次使用體驗**。</span><span class="sxs-lookup"><span data-stu-id="e5b99-185">**Use the first use experience** for tasks and settings if they apply to individual users.</span></span>

### <a name="presentation"></a><span data-ttu-id="e5b99-186">簡報</span><span class="sxs-lookup"><span data-stu-id="e5b99-186">Presentation</span></span>

-   <span data-ttu-id="e5b99-187">**偏好選用的工作和設定，以進行必要的工作和設定。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-187">**Prefer optional tasks and settings to required tasks and settings.**</span></span> <span data-ttu-id="e5b99-188">避免強制使用者設定您的程式。</span><span class="sxs-lookup"><span data-stu-id="e5b99-188">Avoid forcing users to configure your program.</span></span>

    ![<span data-ttu-id="e5b99-189">[找到新硬體] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-189">screen shot of 'found new hardware' dialog box</span></span> ](images/exper-first-exper-image4.png)

    <span data-ttu-id="e5b99-190">[找到新硬體] 對話方塊可讓您選擇是否要安裝驅動程式軟體，而不是讓它成為必要的工作。</span><span class="sxs-lookup"><span data-stu-id="e5b99-190">The Found New Hardware dialog box makes it optional to install driver software instead of making it a required task.</span></span>

-   <span data-ttu-id="e5b99-191">**在實際執行時，從主要工作流程中，採取選擇性的工作和設定。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-191">**Take optional tasks and settings out of the main task flow whenever practical.**</span></span> <span data-ttu-id="e5b99-192">例如，許多安裝程式都會提供自訂安裝路徑，以從主要工作流程中移除不常變更的設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-192">For example, many setup programs provide a custom installation path to remove infrequently changed settings from the main task flow.</span></span>

    ![<span data-ttu-id="e5b99-193">完整和自訂選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-193">screen shot of full and custom radio buttons</span></span> ](images/exper-first-exper-image5.png)

    <span data-ttu-id="e5b99-194">如果使用者不想要自訂安裝，可協助主要工作流程的安裝體驗。</span><span class="sxs-lookup"><span data-stu-id="e5b99-194">A setup experience that facilitates main task flow if the user does not intend to customize the installation.</span></span>

-   <span data-ttu-id="e5b99-195">**使用工作和設定來避免使用者負荷：**</span><span class="sxs-lookup"><span data-stu-id="e5b99-195">**Don't overwhelm users with tasks and settings:**</span></span>
    -   <span data-ttu-id="e5b99-196">**從簡入繁。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-196">**Start simple.**</span></span> <span data-ttu-id="e5b99-197">從簡單的個人化設定開始，到更複雜、技術工作和設定的進度。</span><span class="sxs-lookup"><span data-stu-id="e5b99-197">Begin with simple, personalization settings and progress towards more complex, technical tasks and settings.</span></span> <span data-ttu-id="e5b99-198">例如，Windows 安裝程式會以個人資訊為開頭，並以網路設定結尾。</span><span class="sxs-lookup"><span data-stu-id="e5b99-198">For example, Windows setup starts with personal information and ends with network configuration.</span></span>
    -   <span data-ttu-id="e5b99-199">如果工作和設定只適用于不是主要程式的基本功能，**請使用工作和設定的內容優先經驗**。</span><span class="sxs-lookup"><span data-stu-id="e5b99-199">**Use a contextual first experience** for tasks and settings if they apply only to features that aren't fundamental to the main program.</span></span>

        ![<span data-ttu-id="e5b99-200">[音訊和影片設定] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-200">screen shot of 'audio and video setup' dialog box</span></span> ](images/exper-first-exper-image6.png)

        <span data-ttu-id="e5b99-201">Windows Live Messenger 具有適用于音訊和影片的內容設定，因為次要功能會使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="e5b99-201">Windows Live Messenger has a contextual setup for audio and video because they are used by secondary features.</span></span>

-   <span data-ttu-id="e5b99-202">**不要一次呈現所有內容。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-202">**Don't present everything all at once.**</span></span> <span data-ttu-id="e5b99-203">合併以使用單一 UI，而不是使用多個 UI 介面，或在不同的時間（而不是一次）顯示工作。</span><span class="sxs-lookup"><span data-stu-id="e5b99-203">Consolidate to use a single UI instead of multiple UI surfaces, or display tasks at different times instead of all at once.</span></span>

    <span data-ttu-id="e5b99-204">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="e5b99-204">**Incorrect:**</span></span>

    ![<span data-ttu-id="e5b99-205">五個重迭對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-205">screen shot of five overlapping dialog boxes</span></span> ](images/exper-first-exper-image7.png)

    <span data-ttu-id="e5b99-206">在此範例中，第一個使用經驗很龐大。</span><span class="sxs-lookup"><span data-stu-id="e5b99-206">In this example, the first use experience is overwhelming.</span></span>

-   <span data-ttu-id="e5b99-207">**以使用者的目標和工作（而不是技術方面）表達問題和選項。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-207">**Express questions and options in terms of users' goals and tasks, not in terms of technology.**</span></span> <span data-ttu-id="e5b99-208">提供使用者瞭解並清楚區分的選項。</span><span class="sxs-lookup"><span data-stu-id="e5b99-208">Provide options that users understand and clearly differentiate.</span></span> <span data-ttu-id="e5b99-209">請務必提供足夠的資訊，讓使用者做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="e5b99-209">Make sure to provide enough information for users to make informed decisions.</span></span>
-   <span data-ttu-id="e5b99-210">**如果不清楚需要個人資訊，請解釋您的程式需要資訊的原因，以及其使用方式。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-210">**If the need for personal information isn't obvious, explain why your program needs the information and how it will be used.**</span></span>

    ![<span data-ttu-id="e5b99-211">指出電子郵件地址使用的文字螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-211">screen shot of text stating e-mail address use</span></span> ](images/exper-first-exper-image8.png)

    <span data-ttu-id="e5b99-212">在此範例中，電子商務應用程式會說明如何使用個人資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b99-212">In this example, an e-commerce application explains how personal information will be used.</span></span>

-   <span data-ttu-id="e5b99-213">**只有在使用者無法有效率地執行其他工作時，才會顯示第一個全螢幕體驗。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-213">**Present first experiences full screen only if users can't productively perform other tasks.**</span></span> <span data-ttu-id="e5b99-214">例如，Windows 安裝程式會以全螢幕顯示，以防止使用者在安裝 Windows 時執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="e5b99-214">For example, Windows setup is presented full screen to discourage users from performing other tasks while Windows is being installed.</span></span> <span data-ttu-id="e5b99-215">大部分的第一個體驗都不應該是全螢幕。</span><span class="sxs-lookup"><span data-stu-id="e5b99-215">Most first experiences shouldn't be full screen.</span></span>

### <a name="settings"></a><span data-ttu-id="e5b99-216">設定</span><span class="sxs-lookup"><span data-stu-id="e5b99-216">Settings</span></span>

-   <span data-ttu-id="e5b99-217">**針對所有設定，請選取最安全的 (，以防止遺失資料或系統存取) 、最安全且私用的值。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-217">**For all settings, select the safest (to prevent loss of data or system access), most secure and private value by default.**</span></span> <span data-ttu-id="e5b99-218">如果安全性和安全性不是因素，請選取最有可能或方便的值。</span><span class="sxs-lookup"><span data-stu-id="e5b99-218">If safety and security aren't factors, select the most likely or convenient value.</span></span> <span data-ttu-id="e5b99-219">選擇良好的預設值是簡化第一個體驗的有效方式。</span><span class="sxs-lookup"><span data-stu-id="e5b99-219">Choosing good defaults is an effective way to simplify the first experience.</span></span>
-   <span data-ttu-id="e5b99-220">**要求使用者加入宣告：**</span><span class="sxs-lookup"><span data-stu-id="e5b99-220">**Require users to opt in for:**</span></span>

    -   <span data-ttu-id="e5b99-221">具有法律含意的設定，例如 (Eula) 的使用者授權合約。</span><span class="sxs-lookup"><span data-stu-id="e5b99-221">Settings with legal implications, such as end user licensing agreements (EULAs).</span></span> <span data-ttu-id="e5b99-222">這類設定不能有預設選項。</span><span class="sxs-lookup"><span data-stu-id="e5b99-222">Such settings can't have default selections.</span></span>
    -   <span data-ttu-id="e5b99-223">執行自動系統組態變更的功能，例如 Windows 自動更新。</span><span class="sxs-lookup"><span data-stu-id="e5b99-223">Features that perform automatic system configuration changes, such as Windows automatic updates.</span></span>
    -   <span data-ttu-id="e5b99-224">顯示個人識別資訊 (PII) 或系統資訊的功能。</span><span class="sxs-lookup"><span data-stu-id="e5b99-224">Features that reveal personally identifiable information (PII) or system information.</span></span>
    -   <span data-ttu-id="e5b99-225">除了將專案新增至 [開始] 功能表之外，使用者桌面的變更，例如將圖示新增至桌面或快速啟動列。</span><span class="sxs-lookup"><span data-stu-id="e5b99-225">Changes to the user's desktop beyond adding entries to the Start menu, such as adding icons to the desktop or quick launch bar.</span></span>
    -   <span data-ttu-id="e5b99-226">選用軟體，例如產品增強功能、訂閱和協力廠商產品。</span><span class="sxs-lookup"><span data-stu-id="e5b99-226">Optional software, such as product enhancements, subscriptions, and third-party products.</span></span>

    ![<span data-ttu-id="e5b99-227">[選擇您要的功能] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="e5b99-227">screen shot of choose features you want dialog box</span></span> ](images/exper-first-exper-image9.png)

    <span data-ttu-id="e5b99-228">在此範例中，使用者加入宣告產品增強功能、訂用帳戶和協力廠商產品。</span><span class="sxs-lookup"><span data-stu-id="e5b99-228">In this example, users opt in to product enhancements, subscriptions, and third-party products.</span></span>

-   <span data-ttu-id="e5b99-229">**如果強烈建議設定，請將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-229">**If a setting is strongly recommended, add "(recommended)" to the label.**</span></span> <span data-ttu-id="e5b99-230">若為選項按鈕和核取方塊，請務必將加入至控制項標籤，而不是附加的附注。</span><span class="sxs-lookup"><span data-stu-id="e5b99-230">For radio buttons and check boxes, be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="e5b99-231">**如果設定僅供 advanced 使用者使用，請將「 (advanced) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-231">**If a setting is intended only for advanced users, add "(advanced)" to the label.**</span></span> <span data-ttu-id="e5b99-232">若為選項按鈕和核取方塊，請務必將加入至控制項標籤，而不是附加的附注。</span><span class="sxs-lookup"><span data-stu-id="e5b99-232">For radio buttons and check boxes, be sure to add to the control label, not the supplemental notes.</span></span>

### <a name="tasks"></a><span data-ttu-id="e5b99-233">工作</span><span class="sxs-lookup"><span data-stu-id="e5b99-233">Tasks</span></span>

-   <span data-ttu-id="e5b99-234">**協助使用者有效率地傳遞等待時間。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-234">**Help users pass waiting time productively.**</span></span>
    -   <span data-ttu-id="e5b99-235">如果等候時間通常介於一到兩分鐘之間，請考慮在使用者等待時提供有用的資訊，例如，在安裝過程中的新功能。</span><span class="sxs-lookup"><span data-stu-id="e5b99-235">If the waiting time is typically between one and two minutes, consider providing helpful information while users are waiting, such as a presentation of what is new during setup.</span></span>
    -   <span data-ttu-id="e5b99-236">如果等候時間通常超過兩分鐘，讓使用者可以輕鬆地執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="e5b99-236">If the waiting time is typically longer than two minutes, make it easy for users to perform other tasks.</span></span> <span data-ttu-id="e5b99-237">顯示預估的等候時間，建議使用者在一段時間內執行其他動作，並大幅變更畫面來使工作完成變得很明顯。</span><span class="sxs-lookup"><span data-stu-id="e5b99-237">Display the estimated wait time, recommend that users do something else in the meantime, and make task completion obvious by changing the screen significantly.</span></span>
-   <span data-ttu-id="e5b99-238">**在第一次體驗期間重新考慮呈現教學課程。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-238">**Reconsider presenting tutorials during the first experience.**</span></span> <span data-ttu-id="e5b99-239">最有可能的使用者想要立即使用您的程式，並對稍後的教學課程有興趣。</span><span class="sxs-lookup"><span data-stu-id="e5b99-239">Most likely users want to use your program right away and are interested in tutorials at a later point.</span></span>
-   <span data-ttu-id="e5b99-240">**在第一次體驗中，請勿使用功能公告通知。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-240">**Don't use feature advertisement notifications in the first experience.**</span></span> <span data-ttu-id="e5b99-241">您可以將功能設計成更容易在需要的內容中探索，或不使用任何特殊功能，讓使用者自行探索功能，而不是使用 [功能公告通知](mess-notif.md)。</span><span class="sxs-lookup"><span data-stu-id="e5b99-241">Instead of using a [feature advertisement notification](mess-notif.md), design the feature to be easier to discover in contexts where it is needed, or don't do anything special and let users discover the feature on their own.</span></span>
-   <span data-ttu-id="e5b99-242">**請勿在初始 Windows 體驗期間使用任何通知。**</span><span class="sxs-lookup"><span data-stu-id="e5b99-242">**Don't use any notifications during the initial Windows experience.**</span></span> <span data-ttu-id="e5b99-243">為了改善它的第一個經驗，Windows 7 會隱藏在前幾小時的使用量中顯示的所有通知。</span><span class="sxs-lookup"><span data-stu-id="e5b99-243">To improve its first experience, Windows 7 suppresses all notifications displayed during the first few hours of usage.</span></span> <span data-ttu-id="e5b99-244">設計您的程式，假設使用者不會看到任何這類通知。</span><span class="sxs-lookup"><span data-stu-id="e5b99-244">Design your program assuming users won't see any such notifications.</span></span>

 

