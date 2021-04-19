---
description: 瞭解國際化
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: 瞭解國際化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979298"
---
# <a name="understanding-internationalization"></a><span data-ttu-id="fca4a-103">瞭解國際化</span><span class="sxs-lookup"><span data-stu-id="fca4a-103">Understanding Internationalization</span></span>

<span data-ttu-id="fca4a-104">開發國際化軟體產品不僅需要正確的程式碼的生產環境，還需要能讓產品支援許多地區設定的設計。</span><span class="sxs-lookup"><span data-stu-id="fca4a-104">Developing internationalized software products requires not only the production of correct code, but also a design that permits the product to support many locales.</span></span> <span data-ttu-id="fca4a-105">開發人員及其管理員應該留意到建立全球化應用程式所需的工作量和詳細資料，無論這些應用程式是以單一二進位檔的形式提供給許多不同的市場，或是每個特定地區設定的多個二進位檔都能使用。</span><span class="sxs-lookup"><span data-stu-id="fca4a-105">Developers and their managers should be aware of the level of effort and attention to detail required to create world-ready applications, whether they deliver them as single binaries ready for use in many different markets, or as multiple binaries that are each specific to one locale.</span></span> <span data-ttu-id="fca4a-106">如果您是開發人員，請確定您的管理瞭解國際化牽涉到的不只是程式碼開發。</span><span class="sxs-lookup"><span data-stu-id="fca4a-106">As a developer, make sure your management understands that internationalization involves more than just code development.</span></span> <span data-ttu-id="fca4a-107">在產品週期開始時為國際化設計，可節省您的時間、金錢和投入時間。</span><span class="sxs-lookup"><span data-stu-id="fca4a-107">Designing for internationalization at the beginning of your product cycle saves you time, money, and effort.</span></span>

<span data-ttu-id="fca4a-108">**國際化** 是為了適應世界各地的地區設定而建立的軟體。</span><span class="sxs-lookup"><span data-stu-id="fca4a-108">**Internationalization** is the creation of software that adapts to locales around the world.</span></span> <span data-ttu-id="fca4a-109">**地區** 設定是一組與語言相關的使用者喜好設定。</span><span class="sxs-lookup"><span data-stu-id="fca4a-109">A **locale** is a collection of language-related user preferences.</span></span> <span data-ttu-id="fca4a-110">地區設定是由語言和地理區域配對所指定。</span><span class="sxs-lookup"><span data-stu-id="fca4a-110">A locale is specified by the pairing of a language and a geographical region.</span></span> <span data-ttu-id="fca4a-111">例如，英文 (美國) 和英文 (英國) 有兩種不同的地區設定，也就是英文 (加拿大) 和法文 (加拿大) 。</span><span class="sxs-lookup"><span data-stu-id="fca4a-111">For example, English (United States) and English (United Kingdom) are two different locales, as are English (Canada) and French (Canada).</span></span>

<span data-ttu-id="fca4a-112">國際化軟體有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="fca4a-112">Internationalized software has these attributes:</span></span>

-   <span data-ttu-id="fca4a-113">**全球就緒** 程度涵蓋了設計和實行，可將地區設定無關的程式碼與地區設定相關的資源分開，並包含兩個主要區域：</span><span class="sxs-lookup"><span data-stu-id="fca4a-113">**World-readiness** covers design and implementation that separate locale-independent code from locale-dependent resources, and comprises two major areas:</span></span>
    -   <span data-ttu-id="fca4a-114">**全球化** 是使用獨立于語言或地區設定的功能和程式碼設計來開發程式核心的程式。</span><span class="sxs-lookup"><span data-stu-id="fca4a-114">**Globalization** is the process of developing a program core with features and code design that are independent of language or locale.</span></span> <span data-ttu-id="fca4a-115">相反地，此設計支援 Unicode 支援之語言腳本的輸入、顯示和輸出，以及與特定地區設定相關的資料。</span><span class="sxs-lookup"><span data-stu-id="fca4a-115">Instead, the design supports the input, display, and output of Unicode-supported language scripts, as well as data related to specific locales.</span></span>
    -   <span data-ttu-id="fca4a-116">可 **當地語系化** 性是軟體程式碼基底和資源的設計，可將程式當地語系化（如下所述）至不同的語言版本，而不會變更原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="fca4a-116">**Localizability** is the design of the software code base and resources such that a program can be localized, as defined below, into different language editions without any changes to the source code.</span></span> <span data-ttu-id="fca4a-117">例如，程式碼中的字串緩衝區和 UI 中的文字方塊，必須夠大，才能容納較長的文字字串，例如德文或荷蘭文等語言。</span><span class="sxs-lookup"><span data-stu-id="fca4a-117">For example, string buffers in the code, and text boxes in the UI, must be large enough to accommodate longer text strings in languages such as German or Dutch.</span></span>
-   <span data-ttu-id="fca4a-118">**當地語系化** 這牽涉到轉譯和自訂特定市場的產品，而且主要是建立資源檔，而不是撰寫原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="fca4a-118">**Localization** This involves translating and customizing a product for a specific market, and it is mainly about creating resource files rather than writing source code.</span></span>

<span data-ttu-id="fca4a-119">例如，使用「Microsoft WIN32 API」所提供的「國家語言支援 (NLS) ，是一種軟體發展程式，可支援世界級的準備工作，而修改 UI 元素、翻譯文字，以及將術語標準化，通常是由身為語言專家的人員（例如 translator）所執行的當地語系化步驟。</span><span class="sxs-lookup"><span data-stu-id="fca4a-119">For example, using the National Language Support (NLS) supplied by the Microsoft Win32 API is a software development process that supports world-readiness, whereas modifying the UI elements, translating text, and standardizing terminology are localization steps usually performed by someone who is a language specialist, such as a translator.</span></span> <span data-ttu-id="fca4a-120">即使您的程式碼開發強調世界的就緒程度，您還是需要瞭解當地語系化，因為您的設計決策會影響翻譯人員的工作。</span><span class="sxs-lookup"><span data-stu-id="fca4a-120">Even when your code development emphasizes world-readiness, you need to understand localization because your design decisions affect the work of the translator.</span></span>

 

 



