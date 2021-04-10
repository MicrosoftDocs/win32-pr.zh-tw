---
description: 說明的 MUI 基本概念
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: 說明的 MUI 基本概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dbeedb246944bef6c23c739eafddff86423b35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943676"
---
# <a name="mui-fundamental-concepts-explained"></a><span data-ttu-id="031fb-103">說明的 MUI 基本概念</span><span class="sxs-lookup"><span data-stu-id="031fb-103">MUI Fundamental Concepts Explained</span></span>

-   [<span data-ttu-id="031fb-104">MUI 的先決條件</span><span class="sxs-lookup"><span data-stu-id="031fb-104">Prerequisite for MUI</span></span>](#prerequisite-for-mui)
-   [<span data-ttu-id="031fb-105">分隔原始程式碼與特定語言的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-105">Separation of source code from language specific resources</span></span>](#separation-of-source-code-from-language-specific-resources)
    -   [<span data-ttu-id="031fb-106">早期的程式碼和資源會一起運作</span><span class="sxs-lookup"><span data-stu-id="031fb-106">The early days: code and resources live together</span></span>](#the-early-days-code-and-resources-live-together)
    -   [<span data-ttu-id="031fb-107">以邏輯方式分隔程式碼和可當地語系化的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-107">Logically separating code and localizable resources</span></span>](#logically-separating-code-and-localizable-resources)
    -   [<span data-ttu-id="031fb-108">實際分隔程式碼和資源</span><span class="sxs-lookup"><span data-stu-id="031fb-108">Physically separating code and resources</span></span>](#physically-separating-code-and-resources)
-   [<span data-ttu-id="031fb-109">以動態方式載入特定語言的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-109">Dynamically loading language-specific resources</span></span>](#dynamically-loading-language-specific-resources)
-   [<span data-ttu-id="031fb-110">建立 MUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="031fb-110">Building MUI applications</span></span>](#building-mui-applications)

## <a name="prerequisite-for-mui"></a><span data-ttu-id="031fb-111">MUI 的先決條件</span><span class="sxs-lookup"><span data-stu-id="031fb-111">Prerequisite for MUI</span></span>

<span data-ttu-id="031fb-112">建立適用于 Windows Vista 和以上的 MUI 相容應用程式的基本必要條件是根據 Windows [全球化指導方針](https://msdn.microsoft.com/goglobal/bb688110.aspx)來設計應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-112">The basic prerequisite for building a MUI-compliant application for Windows Vista and beyond is to design the application in accordance with Windows [globalization guidelines](https://msdn.microsoft.com/goglobal/bb688110.aspx).</span></span>

## <a name="separation-of-source-code-from-language-specific-resources"></a><span data-ttu-id="031fb-113">分隔原始程式碼與特定語言的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-113">Separation of source code from language specific resources</span></span>

<span data-ttu-id="031fb-114">MUI 技術的其中一個基本部署是將應用程式原始程式碼與特定語言的資源分開，以便更有效率地在應用程式中啟用多語言案例。</span><span class="sxs-lookup"><span data-stu-id="031fb-114">One of the fundamental premises of MUI technology is the separation of application source code from language-specific resources, to enable multi-lingual scenarios in applications more efficiently.</span></span> <span data-ttu-id="031fb-115">程式碼和資源的分隔是透過不同的機制，以及一段時間內的不同角度來達成，如下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="031fb-115">The separation of code and resources has been achieved via different mechanisms and to different degrees over time, as outlined in the following sections.</span></span> <span data-ttu-id="031fb-116">每個方法都提供了不同程度的彈性來建立、部署及服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-116">Each method provided varying degrees of flexibility in building, deploying, and servicing the application.</span></span>

<span data-ttu-id="031fb-117">適用于 MUI 規範之應用程式的建議解決方案是此處所述的最後一種方法，也就是應用程式原始程式碼和資源的實體分隔，其資源本身會進一步細分為每個支援的語言，以獲得最大的建立、部署和服務彈性。</span><span class="sxs-lookup"><span data-stu-id="031fb-117">The recommended solution for MUI-compliant applications is the last method outlined here, namely the physical separation of application source code and resources, with the resources themselves further broken down into one file per supported language for maximum flexibility in building, deploying, and servicing.</span></span>

### <a name="the-early-days-code-and-resources-live-together"></a><span data-ttu-id="031fb-118">早期的程式碼和資源會一起運作</span><span class="sxs-lookup"><span data-stu-id="031fb-118">The early days: code and resources live together</span></span>

<span data-ttu-id="031fb-119">一開始，當地語系化的應用程式是透過編輯原始程式碼和變更資源來建立， (通常是程式碼中) 的字串，然後重新編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-119">Initially, localized applications were created by editing the source code and changing the resources (usually strings) in the code itself and recompiling the applications.</span></span> <span data-ttu-id="031fb-120">這表示若要產生當地語系化的版本，您必須複製原始原始程式碼、將文字 (資源轉譯為原始程式碼中的) 元素，然後重新編譯程式碼。</span><span class="sxs-lookup"><span data-stu-id="031fb-120">This meant that to produce a localized version, one had to copy the original source code, translate the text (resources) elements within the source code, and recompile the code.</span></span> <span data-ttu-id="031fb-121">下圖顯示需要當地語系化之文字的應用程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="031fb-121">The following image shows application code with text that needs to be localized.</span></span>

![顯示應用程式的概念圖表，其中包含內嵌文字資源的單位](images/mui-fundamental-concepts-explained-fig3.gif)

<span data-ttu-id="031fb-123">雖然這種方法可讓您建立當地語系化的應用程式，但它也有很大的缺點：</span><span class="sxs-lookup"><span data-stu-id="031fb-123">While this approach enables the creation of localized applications, it also has significant drawbacks:</span></span>

-   <span data-ttu-id="031fb-124">它需要多個版本的原始程式碼，至少一個用於來源語言，另一個適用于每個目的語言。</span><span class="sxs-lookup"><span data-stu-id="031fb-124">It requires multiple versions of the source code, at least one for the source language and one for each of the target languages.</span></span> <span data-ttu-id="031fb-125">這會造成將應用程式的不同語言版本同步處理的重大問題。</span><span class="sxs-lookup"><span data-stu-id="031fb-125">This creates significant issues synchronizing the different language releases of the application.</span></span> <span data-ttu-id="031fb-126">尤其是，在程式碼中需要修正瑕疵時，每個程式碼的每個複本都需要修正瑕疵 (每一個語言) 。</span><span class="sxs-lookup"><span data-stu-id="031fb-126">In particular, when a defect needs to be fixed in the code, the defect needs to be fixed in every copy of the source code (one per language).</span></span>
-   <span data-ttu-id="031fb-127">它也很容易發生錯誤，因為它需要當地語系化人員（非開發人員）在原始程式碼中進行修改，因此在程式碼完整性方面創造相當大的風險。</span><span class="sxs-lookup"><span data-stu-id="031fb-127">It is also extremely error-prone as it required localizers—who are not developers—to make modifications in source code, thus creating a considerable risk in terms of code integrity.</span></span>

<span data-ttu-id="031fb-128">這些缺點的組合使得這項功能極為沒有效率，並且需要更好的模型。</span><span class="sxs-lookup"><span data-stu-id="031fb-128">The combination of these drawbacks makes this an extremely inefficient proposition, and a better model was needed.</span></span>

### <a name="logically-separating-code-and-localizable-resources"></a><span data-ttu-id="031fb-129">以邏輯方式分隔程式碼和可當地語系化的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-129">Logically separating code and localizable resources</span></span>

<span data-ttu-id="031fb-130">上述模型的重大改進，是應用程式程式碼和可當地語系化資源的邏輯分隔。</span><span class="sxs-lookup"><span data-stu-id="031fb-130">A significant improvement over the preceding model is the logical separation of code and localizable resources for an application.</span></span> <span data-ttu-id="031fb-131">這會將程式碼與資源隔離，並確保當資源受到當地語系化的變更時，程式碼保持不變。</span><span class="sxs-lookup"><span data-stu-id="031fb-131">This isolates the code from the resources and ensures that code remains untouched when resources are being changed by localization.</span></span> <span data-ttu-id="031fb-132">從執行的觀點來看，字串和其他使用者介面專案會儲存在資源檔中，這種方式相當容易轉譯，而且會以邏輯方式與程式碼區段分開。</span><span class="sxs-lookup"><span data-stu-id="031fb-132">From an implementation standpoint, strings and other user interface elements are stored in resource files, which are relatively easy to translate and are logically separated from the code sections.</span></span>

<span data-ttu-id="031fb-133">在理想的情況下，新增任何特定語言的支援可以像將可當地語系化的資源轉譯成這種新的語言，並使用這些轉譯的資源來建立新的當地語系化版本的應用程式一樣簡單，而不需要修改任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="031fb-133">Ideally, adding support for any given language can be as simple as translating the localizable resources into this new language and using these translated resources to create a new localized version of the application—without requiring any code modification.</span></span> <span data-ttu-id="031fb-134">下圖說明如何在應用程式中以邏輯方式分隔程式碼和可當地語系化的資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-134">The following image illustrates how code and localizable resources should be logically separated within an application.</span></span>

![顯示應用程式的概念圖表，其中包含與程式碼分開的可當地語系化資源](images/mui-fundamental-concepts-explained-fig4.gif)

<span data-ttu-id="031fb-136">此模型可讓您更輕鬆地建立當地語系化的應用程式版本，並大幅改善了先前的模型。</span><span class="sxs-lookup"><span data-stu-id="031fb-136">This model enables an easier creation of localized versions of an application and is a significant improvement over the previous model.</span></span> <span data-ttu-id="031fb-137">此模型是透過使用資源管理工具來實行，多年以來都有很多的經驗，現在許多應用程式也經常使用。</span><span class="sxs-lookup"><span data-stu-id="031fb-137">This model, implemented through the use of resource management tools, has been very successful over the years and is still commonly used by many applications today.</span></span> <span data-ttu-id="031fb-138">不過，它的確有很大的缺點：</span><span class="sxs-lookup"><span data-stu-id="031fb-138">However, it does have significant drawbacks:</span></span>

-   <span data-ttu-id="031fb-139">在邏輯上分隔的情況下，程式碼和當地語系化的資源仍會實際聯結在一個可執行檔中。</span><span class="sxs-lookup"><span data-stu-id="031fb-139">While logically separated, code and localized resources are still physically joined in one executable file.</span></span> <span data-ttu-id="031fb-140">尤其是，因為相同的程式碼缺失 (在所有語言版本中都相同，所以仍有問題，) 需要每種語言的修補程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-140">In particular, serviceability is still problematic as the same code defect (identical in all language versions) requires a patch per language.</span></span> <span data-ttu-id="031fb-141">因此，如果某個應用程式是以20種語言傳送應用程式，則必須發出20次的服務修補程式 (每個語言) 一次，即使程式碼只是固定的一次也是一樣。</span><span class="sxs-lookup"><span data-stu-id="031fb-141">Therefore, if one is shipping the application in 20 languages, a service patch needs to be issued 20 times (one for each language), even though the code is only fixed once.</span></span>
-   <span data-ttu-id="031fb-142">此模型不會適當地支援散發和使用多語言應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-142">Distribution and use of multi-lingual applications are not adequately supported by this model.</span></span> <span data-ttu-id="031fb-143">這可能是 OEM 和企業案例中的重大問題。</span><span class="sxs-lookup"><span data-stu-id="031fb-143">This can be a significant problem in OEM and enterprise scenarios.</span></span> <span data-ttu-id="031fb-144">比方說，如果在兩個使用不同語言的使用者之間共用電腦，則必須使用此模型來安裝應用程式兩次，然後必須啟用某些機制，才能在兩個安裝之間替代。</span><span class="sxs-lookup"><span data-stu-id="031fb-144">For instance, if a computer is to be shared between two users using different languages, applications will need to be installed twice with this model, and then some mechanism will need to be enabled to alternate between the two installations.</span></span> <span data-ttu-id="031fb-145">這假設沒有其他相依性可防止這種情況執行。</span><span class="sxs-lookup"><span data-stu-id="031fb-145">This assumes that there are no additional dependencies that prevent even this scenario from being implemented.</span></span> <span data-ttu-id="031fb-146">下圖顯示需要兩個修補程式的單一程式碼缺失範例。</span><span class="sxs-lookup"><span data-stu-id="031fb-146">The following image shows an example of a single code defect that requires two patches.</span></span>

![顯示兩個具有相同程式碼瑕疵之當地語系化應用程式的概念圖表](images/mui-fundamental-concepts-explained-fig5.gif)

<span data-ttu-id="031fb-148">很明顯地，雖然此模型在某些情況下可正常運作，但對於多語言應用程式及其部署的限制可能會有很大的問題。</span><span class="sxs-lookup"><span data-stu-id="031fb-148">It is clear that while this model works well in some scenarios, its limitations for multi-lingual applications and their deployments can be very problematic.</span></span>

<span data-ttu-id="031fb-149">此模型的變化可緩和某些多語言應用程式問題，這是可當地語系化的資源包含一組不同語言資源的模型。</span><span class="sxs-lookup"><span data-stu-id="031fb-149">A variation of this model that alleviates some of the multi-lingual applications issues is the model where the localizable resources contain a set of different language resources.</span></span> <span data-ttu-id="031fb-150">此模型在相同的應用程式中有通用的程式碼基底和數種不同語言的資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-150">This model has a common code base and several resources for different languages in the same application.</span></span> <span data-ttu-id="031fb-151">例如，應用程式可以在同一個套件中隨附英文、德文、法文、西班牙文、荷蘭文和義大利文。</span><span class="sxs-lookup"><span data-stu-id="031fb-151">For example, an application can ship with English, German, French, Spanish, Dutch, and Italian in the same package.</span></span> <span data-ttu-id="031fb-152">下圖顯示包含多個語言資源的應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-152">The following image shows an application that contains multiple language resources.</span></span>

![顯示應用程式與兩個地區設定專屬資源不同的程式碼的概念圖表](images/mui-fundamental-concepts-explained-fig6.gif)

<span data-ttu-id="031fb-154">這種模型可讓您在程式碼缺失需要修正時更輕鬆地為應用程式提供服務（這是一項改善的功能），但在支援其他語言時，不會改善先前的模型。</span><span class="sxs-lookup"><span data-stu-id="031fb-154">This model makes it easier to service the application when a code defect needs to be fixed—which is an improvement—but does not improve over previous models when it comes to supporting additional languages.</span></span> <span data-ttu-id="031fb-155">在此情況下，您仍然需要釋出新版本的應用程式 (而且該版本可能會很複雜，因為必須確保所有語言資源都在相同的散發) 內進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="031fb-155">In this case, one still needs to release a new version of the application (and that release is potentially complicated by the need to ensure that all language resources are synchronized within the same distribution).</span></span>

### <a name="physically-separating-code-and-resources"></a><span data-ttu-id="031fb-156">實際分隔程式碼和資源</span><span class="sxs-lookup"><span data-stu-id="031fb-156">Physically separating code and resources</span></span>

<span data-ttu-id="031fb-157">下一個進化步驟是實際分隔程式碼和資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-157">The next evolutionary step is to physically separate code and resources.</span></span> <span data-ttu-id="031fb-158">在此模型中，資源會從程式碼抽象化，並實際分隔不同的實檔案。</span><span class="sxs-lookup"><span data-stu-id="031fb-158">In this model, the resources are abstracted from the code and physically separated in different implementation files.</span></span> <span data-ttu-id="031fb-159">特別是，這表示程式碼可能會變成與語言無關的真正語言;應用程式的所有當地語系化版本實際上都會隨附相同的實體程式碼。</span><span class="sxs-lookup"><span data-stu-id="031fb-159">In particular, this means that the code can become truly language independent; the same physical code is actually shipped for all localized versions of an application.</span></span> <span data-ttu-id="031fb-160">下圖說明程式碼和可當地語系化的資源必須實體分隔。</span><span class="sxs-lookup"><span data-stu-id="031fb-160">The following image illustrates that code and localizable resources must be physically separated.</span></span>

![顯示應用程式與可當地語系化資源分開的概念圖表](images/mui-fundamental-concepts-explained-fig7.gif)

<span data-ttu-id="031fb-162">這種方法有幾個優點，而不是先前的方法：</span><span class="sxs-lookup"><span data-stu-id="031fb-162">This approach has several advantages over the previous approaches:</span></span>

-   <span data-ttu-id="031fb-163">多語言解決方案的部署大幅簡化。</span><span class="sxs-lookup"><span data-stu-id="031fb-163">Deployment of multi-lingual solutions is greatly simplified.</span></span> <span data-ttu-id="031fb-164">新增任何指定語言的支援只需要為此特定語言傳送和安裝一組新的語言資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-164">Adding support for any given language requires only shipping and installing a new set of language resources for this particular language.</span></span> <span data-ttu-id="031fb-165">當語言資源並非全部都能同時使用時，這一點特別重要。</span><span class="sxs-lookup"><span data-stu-id="031fb-165">This is particularly important when language resources are not all simultaneously available.</span></span> <span data-ttu-id="031fb-166">使用此模型，您可以使用一組核心語言來部署應用程式，並在一段時間後增加支援的語言數目，而不需要修改或重新部署實際的程式碼。</span><span class="sxs-lookup"><span data-stu-id="031fb-166">With this model, one can deploy an application in a set of core languages and increase the number of supported languages over time without having to modify or redeploy the actual code.</span></span> <span data-ttu-id="031fb-167">這項優點更進一步延伸，可讓您藉由確保在此慣用語言中找不到的資源「切換回」至使用者也瞭解的另一種語言，以提供指定語言的部分當地語系化應用程式和系統元件。</span><span class="sxs-lookup"><span data-stu-id="031fb-167">This advantage is further extended by a fallback mechanism that allows for partial localization of applications and system components in a given language by ensuring that resources that are not found in this preferred language "fall back" to another language that the users also understand.</span></span> <span data-ttu-id="031fb-168">整體來說，此模型有助於減輕全球公司在部署多個語言的應用程式時所面臨的沉重負擔，因為這可讓您以更有效率的方式來部署單一映射。</span><span class="sxs-lookup"><span data-stu-id="031fb-168">Overall, this model helps alleviate the considerable burden that global companies face in deploying applications in multiple languages as it enables single image deployment in a much more effective way.</span></span>
-   <span data-ttu-id="031fb-169">改良功能已獲得改善。</span><span class="sxs-lookup"><span data-stu-id="031fb-169">Serviceability is improved.</span></span> <span data-ttu-id="031fb-170">由於程式碼完全與當地語系化無關，因此只需要修正並部署程式碼缺失。</span><span class="sxs-lookup"><span data-stu-id="031fb-170">A code defect only needs to be fixed and deployed once, as the code is completely localization-independent.</span></span> <span data-ttu-id="031fb-171">在此模型中，如果變更與 UI 無關，就會發出程式碼缺失的更正，比先前的任何模型更簡單且符合成本效益。</span><span class="sxs-lookup"><span data-stu-id="031fb-171">With this model, issuing a correction for a code defect, provided the change is not UI-related, is much simpler and cost effective than in any of the previous models.</span></span>

## <a name="dynamically-loading-language-specific-resources"></a><span data-ttu-id="031fb-172">以動態方式載入特定語言的資源</span><span class="sxs-lookup"><span data-stu-id="031fb-172">Dynamically loading language-specific resources</span></span>

<span data-ttu-id="031fb-173">[從特定語言的資源中實際分隔原始程式碼](#physically-separating-code-and-resources)，以及為應用程式建立非語言相關核心二進位檔的 MUI 基本概念，基本上會設定採用遭利用的架構，以根據使用者和系統語言設定來執行特定語言資源的動態載入。</span><span class="sxs-lookup"><span data-stu-id="031fb-173">The MUI fundamental concepts of [physically separating source code from language-specific resources](#physically-separating-code-and-resources), and building a language-neutral core binary for an application, essentially set up an architecture that is conducive to implementing the dynamic loading of language-specific resources based on user and system language settings.</span></span>

<span data-ttu-id="031fb-174">內建在非語言相關核心二進位檔中的應用程式原始程式碼，可以利用 Windows 平臺中的 MUI Api，針對指定的內容，對適當的顯示使用者介面語言進行抽象化。</span><span class="sxs-lookup"><span data-stu-id="031fb-174">Application source code bundled into the language-neutral core binary can utilize MUI APIs in the Windows platform to abstract the selection of the appropriate display user interface language for a given context.</span></span> <span data-ttu-id="031fb-175">MUI 支援這種方式：</span><span class="sxs-lookup"><span data-stu-id="031fb-175">MUI supports this by:</span></span>

-   <span data-ttu-id="031fb-176">根據系統、使用者、應用層級、使用者層級和系統層級設定，來建立顯示使用者介面語言的優先順序清單。</span><span class="sxs-lookup"><span data-stu-id="031fb-176">Constructing a prioritized list of display user interface languages based on system, user, and application-level, user-level, and system-level settings.</span></span>
-   <span data-ttu-id="031fb-177">根據當地語系化資源的可用性，執行可根據已設定優先順序的語言清單選擇適當候選項的回溯機制。</span><span class="sxs-lookup"><span data-stu-id="031fb-177">Implementing a fallback mechanism that chooses an appropriate candidate from this prioritized list of languages, based on the availability of localized resources.</span></span>

<span data-ttu-id="031fb-178">使用優先回復動態載入使用者介面資源的優點如下：</span><span class="sxs-lookup"><span data-stu-id="031fb-178">The benefits of dynamically loading user-interface resources with prioritized fallback are:</span></span>

-   <span data-ttu-id="031fb-179">它可讓您以指定的語言進行應用程式和系統元件的部分當地語系化，因為在此慣用語言中找不到的資源會自動切換回優先順序清單上的下一個語言。</span><span class="sxs-lookup"><span data-stu-id="031fb-179">It allows for partial localization of applications and system components in a given language, as resources that are not found in this preferred language will automatically fall back to the next language on the prioritized list.</span></span>
-   <span data-ttu-id="031fb-180">它可讓您從一種語言動態切換到另一種語言。</span><span class="sxs-lookup"><span data-stu-id="031fb-180">It enables scenarios such as switching dynamically from one language to another.</span></span>
-   <span data-ttu-id="031fb-181">它可讓您建立區域或全球單一部署映射，其中涵蓋一組適用于 Oem 和企業的語言。</span><span class="sxs-lookup"><span data-stu-id="031fb-181">It allows creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="building-mui-applications"></a><span data-ttu-id="031fb-182">建立 MUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="031fb-182">Building MUI applications</span></span>

<span data-ttu-id="031fb-183">上述各節概述將原始程式碼與特定語言的資源分開的選項，以及能夠利用核心 Windows 平臺 Api 動態載入當地語系化資源的結果優點。</span><span class="sxs-lookup"><span data-stu-id="031fb-183">The previous sections outlined the options for separating source code from language-specific resources, and the resultant benefit in being able to utilize core Windows platform APIs to dynamically load localized resources.</span></span> <span data-ttu-id="031fb-184">雖然這些都是指導方針，但也應該指出，沒有任何特定的規範方法可開發 Windows 平臺的 MUI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="031fb-184">While these are guidelines, it should also be pointed out that there is no specific prescriptive way to develop a MUI application for the Windows platform.</span></span>

<span data-ttu-id="031fb-185">應用程式開發人員可以完整選擇如何處理各種使用者介面語言設定、資源建立選項和資源載入方法。</span><span class="sxs-lookup"><span data-stu-id="031fb-185">Application developers have full choice in how they handle various user-interface language settings, resource creation options, and resource loading methods.</span></span> <span data-ttu-id="031fb-186">開發人員可以評估這份檔中所提供的指導方針，並選擇符合其需求和開發環境的組合。</span><span class="sxs-lookup"><span data-stu-id="031fb-186">Developers can evaluate the guidelines provided in this document and choose a combination that fits their requirements and development environment.</span></span>

<span data-ttu-id="031fb-187">下表摘要說明要為 Windows 平臺建立 MUI 應用程式的應用程式開發人員可使用的各種設計選項。</span><span class="sxs-lookup"><span data-stu-id="031fb-187">The following table summarizes the different design options available to application developers who are looking to create a MUI application for the Windows platform.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="031fb-188">使用者介面語言設定</span><span class="sxs-lookup"><span data-stu-id="031fb-188">User interface language settings</span></span></th>
<th><span data-ttu-id="031fb-189">資源建立</span><span class="sxs-lookup"><span data-stu-id="031fb-189">Resource creation</span></span></th>
<th><span data-ttu-id="031fb-190">資源載入</span><span class="sxs-lookup"><span data-stu-id="031fb-190">Resource loading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="031fb-191">遵循作業系統 $ {REMOVE} $ 中的 UI 語言設定</span><span class="sxs-lookup"><span data-stu-id="031fb-191">Follow UI language settings in the operating system${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="031fb-192">分割資源二進位檔中的單一語言 (MUI 資源技術) </span><span class="sxs-lookup"><span data-stu-id="031fb-192">Single language in a split resource binary (MUI Resource Technology)</span></span><br/> <span data-ttu-id="031fb-193">-或-</span><span class="sxs-lookup"><span data-stu-id="031fb-193">-or-</span></span><br/> <span data-ttu-id="031fb-194">非分割資源二進位檔中的多個語言</span><span class="sxs-lookup"><span data-stu-id="031fb-194">Multiple languages in a non-split resource binary</span></span><br/></td>
<td><span data-ttu-id="031fb-195">應用程式會呼叫標準資源載入功能。</span><span class="sxs-lookup"><span data-stu-id="031fb-195">Application calls standard resource loading functions.</span></span> <span data-ttu-id="031fb-196">系統會以符合作業系統設定的語言傳回資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-196">Resources are returned in the languages matching the operating system settings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="031fb-197">應用程式特定的資源機制</span><span class="sxs-lookup"><span data-stu-id="031fb-197">Application-specific resource mechanism</span></span><br/></td>
<td><span data-ttu-id="031fb-198">應用程式會呼叫 MUI API，從作業系統取出執行緒慣用的 UI 語言或處理常式慣用的 UI 語言，並使用這些設定來載入本身的資源。</span><span class="sxs-lookup"><span data-stu-id="031fb-198">Application calls MUI API to retrieve the thread-preferred UI languages or process-preferred UI languages from the operating system and use these settings to load its own resources.</span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="031fb-199">應用程式特定的 UI 語言設定 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="031fb-199">Application-specific UI language settings${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="031fb-200">分割資源二進位檔中的單一語言</span><span class="sxs-lookup"><span data-stu-id="031fb-200">Single language in a split resource binary</span></span><br/> <span data-ttu-id="031fb-201">-或-</span><span class="sxs-lookup"><span data-stu-id="031fb-201">-or-</span></span><br/> <span data-ttu-id="031fb-202">非分割資源二進位檔中的多個語言</span><span class="sxs-lookup"><span data-stu-id="031fb-202">Multiple languages in a non-split resource binary</span></span><br/></td>
<td><span data-ttu-id="031fb-203">應用程式會呼叫 MUI API 來設定應用程式特定的 UI 語言或處理常式慣用的 UI 語言，然後呼叫標準資源載入功能。</span><span class="sxs-lookup"><span data-stu-id="031fb-203">Application calls MUI API to set application-specific UI languages or process-preferred UI languages and then calls standard resource loading functions.</span></span> <span data-ttu-id="031fb-204">資源會以應用程式或系統語言所設定的語言傳回。</span><span class="sxs-lookup"><span data-stu-id="031fb-204">Resources are returned in the languages set by the application or system languages.</span></span><br/> <span data-ttu-id="031fb-205">-或-</span><span class="sxs-lookup"><span data-stu-id="031fb-205">-or-</span></span><br/> <span data-ttu-id="031fb-206">應用程式會探查特定語言的資源，並從抓取的二進位資料處理自己的資源解壓縮。</span><span class="sxs-lookup"><span data-stu-id="031fb-206">Application probes resources in a specific language and handles its own resource extraction from the retrieved binary data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="031fb-207">應用程式特定的資源機制</span><span class="sxs-lookup"><span data-stu-id="031fb-207">Application-specific resource mechanism</span></span><br/></td>
<td><span data-ttu-id="031fb-208">應用程式會管理本身的資源載入。</span><span class="sxs-lookup"><span data-stu-id="031fb-208">Application manages its own resource loading.</span></span><br/></td>

</tr>
</tbody>
</table>



 

 

 




