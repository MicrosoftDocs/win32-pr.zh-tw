---
title: 手寫和筆墨
description: 隨著市面上的 Tablet Pc 激增，平板電腦功能也成為主流運算的一部分。
ms.assetid: 22caf8b3-d519-418f-b662-180d270b7cfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10bec217a9568419b3b150c932fc236c7d735bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682951"
---
# <a name="handwriting-and-ink"></a><span data-ttu-id="52285-103">手寫和筆墨</span><span class="sxs-lookup"><span data-stu-id="52285-103">Handwriting and Ink</span></span>

<span data-ttu-id="52285-104">隨著市面上的 *Tablet pc* 激增， *平板* 電腦功能也成為主流運算的一部分。</span><span class="sxs-lookup"><span data-stu-id="52285-104">With the proliferation of *Tablet PCs* in the market, *Tablet* features are becoming part of mainstream computing.</span></span> <span data-ttu-id="52285-105">在 Windows 7 中，觸控和撰寫是一流的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="52285-105">In Windows 7, touch and writing are first-class user experiences.</span></span> <span data-ttu-id="52285-106">Windows 7 提供更高的精確度和速度，改善了畫筆體驗。</span><span class="sxs-lookup"><span data-stu-id="52285-106">Windows 7 improves the pen experience by providing greater accuracy and speed.</span></span> <span data-ttu-id="52285-107">手寫輸入已改善，並支援更多語言。</span><span class="sxs-lookup"><span data-stu-id="52285-107">Handwriting input is improved and more languages are supported.</span></span> <span data-ttu-id="52285-108">文字輸入面板提供預測文字，以提供更高速的輸入和修正。</span><span class="sxs-lookup"><span data-stu-id="52285-108">The Text Input Panel offers predictive text for greater speed of input and correction.</span></span> <span data-ttu-id="52285-109">透過個人化語言辨識中所有語言、自訂字典和突破的個人化，來改善手寫精確度。</span><span class="sxs-lookup"><span data-stu-id="52285-109">Handwriting accuracy is improved through personalization in all languages, custom dictionaries, and breakthroughs in East Asian language recognition.</span></span> <span data-ttu-id="52285-110">改良的互動模型可在可攜式電腦常見的小型高解析度畫面上，提供更好的閱讀體驗。</span><span class="sxs-lookup"><span data-stu-id="52285-110">The improved interaction model delivers a better reading experience on the small, high-resolution screens common in portable computers.</span></span> <span data-ttu-id="52285-111"> (參閱 [設計文字輸入面板的](../tablet/programming-the-text-input-panel.md)程式。 ) </span><span class="sxs-lookup"><span data-stu-id="52285-111">(See [Programming the Text Input Panel](../tablet/programming-the-text-input-panel.md).)</span></span>

![tablet pc 輸入面板](images/windows7-4.jpg)

<span data-ttu-id="52285-113">文字輸入面板具有簡單的文字校正功能</span><span class="sxs-lookup"><span data-stu-id="52285-113">The Text Input Panel features easy text correction</span></span>

## <a name="math-recognition"></a><span data-ttu-id="52285-114">數學辨識</span><span class="sxs-lookup"><span data-stu-id="52285-114">Math Recognition</span></span>

<span data-ttu-id="52285-115">新的數學辨識功能可讓使用者以手寫方式在應用程式中輸入數學，也就是輸入數學運算式的最自然、最有效率的方式。</span><span class="sxs-lookup"><span data-stu-id="52285-115">The new Math Recognition feature enables users to enter math into applications by means of handwriting—the most natural and efficient way of entering mathematical expressions.</span></span> <span data-ttu-id="52285-116">這項功能是由兩個 UI 元件所提供。</span><span class="sxs-lookup"><span data-stu-id="52285-116">The functionality is provided by two UI components.</span></span> <span data-ttu-id="52285-117">數學輸入面板是獨立的 Windows 配件，可搭配任何數學感知應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="52285-117">Math Input Panel is a stand-alone Windows accessory that works with any math-aware application.</span></span> <span data-ttu-id="52285-118">數學輸入控制項透過其 API 整合至應用程式。</span><span class="sxs-lookup"><span data-stu-id="52285-118">Math Input Control is integrated into applications through its API.</span></span>

<span data-ttu-id="52285-119">基礎 UI 元件是數學辨識器。</span><span class="sxs-lookup"><span data-stu-id="52285-119">Underlying the UI components is the Math Recognizer.</span></span> <span data-ttu-id="52285-120">此引擎會辨識手寫的數學運算式，並將結果轉譯為 *MathML* 格式，以便讓應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="52285-120">This engine recognizes handwritten mathematical expression and translates the result into *MathML* format for applications to use.</span></span> <span data-ttu-id="52285-121">修正經驗已經過改善，可協助使用者更快進行修正。</span><span class="sxs-lookup"><span data-stu-id="52285-121">The correction experience has been improved to help users make corrections faster.</span></span> <span data-ttu-id="52285-122"> (參閱程式 [設計數學輸入控制項](../tablet/programming-the-math-input-control.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="52285-122">(See [Programming the Math Input Control](../tablet/programming-the-math-input-control.md).)</span></span>

![數學輸入面板](images/windows7-5.jpg)

<span data-ttu-id="52285-124">數學辨識可讓使用者透過手寫方式在應用程式中輸入數學</span><span class="sxs-lookup"><span data-stu-id="52285-124">Math Recognition enables users to enter math into applications by means of handwriting</span></span>

## <a name="handwriting-with-personalized-custom-dictionary"></a><span data-ttu-id="52285-125">使用個人化自訂字典手寫</span><span class="sxs-lookup"><span data-stu-id="52285-125">Handwriting with Personalized Custom Dictionary</span></span>

<span data-ttu-id="52285-126">在許多案例中，良好的手寫精確度需要針對使用領域量身打造的字典。</span><span class="sxs-lookup"><span data-stu-id="52285-126">For many scenarios, good handwriting accuracy requires a dictionary tailored to the domain of use.</span></span> <span data-ttu-id="52285-127">Windows 7 引進了自訂字典，可針對特製化詞彙啟用更好的手寫辨識。</span><span class="sxs-lookup"><span data-stu-id="52285-127">Windows 7 introduces custom dictionaries, which enable better handwriting recognition for specialized vocabularies.</span></span> <span data-ttu-id="52285-128">撰寫垂直應用程式的開發人員（例如醫療處方記事本），現在可以將特定詞彙新增至其應用程式，例如藥物名稱。</span><span class="sxs-lookup"><span data-stu-id="52285-128">Developers who are writing vertical applications--for example, a medical prescription notepad--can now add specific terms to their application, such as drug names.</span></span> <span data-ttu-id="52285-129"> (請參閱 [Windows Touch 和 TABLET PC 開發人員的增強功能](https://www.microsoft.com/whdc/device/input/Touch_tab_enhance.mspx)。 ) </span><span class="sxs-lookup"><span data-stu-id="52285-129">(See [Developer Enhancements to Windows Touch and Tablet PC](https://www.microsoft.com/whdc/device/input/Touch_tab_enhance.mspx).)</span></span>

 

 