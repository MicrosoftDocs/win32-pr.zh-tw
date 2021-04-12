---
title: 'Windows 控制項的新功能 () '
description: 本主題說明 Windows 8 與舊版 Windows 之間的主題和視覺化樣式的支援差異。
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464044"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="d7e41-103">Windows 控制項的新功能 () </span><span class="sxs-lookup"><span data-stu-id="d7e41-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="d7e41-104">本主題說明 Windows 8 與舊版 Windows 之間的主題和視覺化樣式的支援差異。</span><span class="sxs-lookup"><span data-stu-id="d7e41-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="d7e41-105">至 Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7e41-105">Through Windows 7</span></span>

<span data-ttu-id="d7e41-106">在 Windows 7 中，視覺效果樣式預設為開啟，但使用者可以選取 [Windows 傳統主題] 或關閉 [主題] 服務，將其關閉。</span><span class="sxs-lookup"><span data-stu-id="d7e41-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="d7e41-107">當視覺化樣式關閉時，所有 UI 都會取得傳統外觀，且大部分的視覺效果樣式 Api 都無法使用。</span><span class="sxs-lookup"><span data-stu-id="d7e41-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="d7e41-108">已透過 Windows 7 保留視覺化樣式的模式，以支援各種高對比主題，以及 Windows 傳統主題。</span><span class="sxs-lookup"><span data-stu-id="d7e41-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="d7e41-109">如果您想要在相同的應用程式中同時支援視覺效果樣式和高對比主題，通常需要維護兩個不同的程式碼路徑來呈現控制項。</span><span class="sxs-lookup"><span data-stu-id="d7e41-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="d7e41-110">Windows 8 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d7e41-110">Windows 8 and Later</span></span>

<span data-ttu-id="d7e41-111">在 Windows 8 中，視覺效果樣式無法 **透過 [** **電腦設定** ] 的 [個人化] 頁面或關閉主題服務來關閉。</span><span class="sxs-lookup"><span data-stu-id="d7e41-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="d7e41-112">Windows 傳統模式已不存在，而且已修改高對比模式來使用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="d7e41-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="d7e41-113">因為這些變更，所以僅以 Windows 8 為目標的應用程式不再需要兩個不同的程式碼路徑來支援視覺效果樣式和高對比主題。</span><span class="sxs-lookup"><span data-stu-id="d7e41-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="d7e41-114">Windows 8 中的視覺化樣式包含 Windows 傳統主題模式的回溯相容性支援。</span><span class="sxs-lookup"><span data-stu-id="d7e41-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="d7e41-115">任何適用于舊版的 UI 轉譯程式碼將繼續在 Windows 8 上運作，而不需要修改。</span><span class="sxs-lookup"><span data-stu-id="d7e41-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="d7e41-116">在 Windows 8 中，如果您想要讓應用程式支援以視覺化樣式為基礎的高對比主題，您必須在應用程式資訊清單的 [相容性] 區段中包含 Windows 8 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7e41-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="d7e41-117">否則，系統會假設應用程式是針對先前的版本所設計，並藉由模擬 Windows 傳統高對比主題來呈現工作區。</span><span class="sxs-lookup"><span data-stu-id="d7e41-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="d7e41-118">如需詳細資訊，請參閱 [支援高對比主題](supporting-high-contrast-themes.md)。</span><span class="sxs-lookup"><span data-stu-id="d7e41-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="d7e41-119">如同舊版，Windows 8 支援第5版和第6版的通用控制項，預設值為5。</span><span class="sxs-lookup"><span data-stu-id="d7e41-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="d7e41-120">因為只有第6版支援視覺化樣式，所以如果您想要將視覺化樣式套用至應用程式工作區中的通用控制項，則必須在應用程式資訊清單中指定第6版。</span><span class="sxs-lookup"><span data-stu-id="d7e41-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="d7e41-121">如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d7e41-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7e41-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7e41-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e41-123">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="d7e41-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="d7e41-124">支援高對比主題</span><span class="sxs-lookup"><span data-stu-id="d7e41-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="d7e41-125">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="d7e41-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="d7e41-126">視覺化樣式總覽</span><span class="sxs-lookup"><span data-stu-id="d7e41-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




