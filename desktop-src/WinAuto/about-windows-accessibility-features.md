---
title: Windows 協助工具功能
description: Windows 協助工具支援 Windows 開發人員的兩種功能類別： Win32 Api 和使用者設定。
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023703"
---
# <a name="windows-accessibility-features"></a><span data-ttu-id="3e687-103">Windows 協助工具功能</span><span class="sxs-lookup"><span data-stu-id="3e687-103">Windows Accessibility features</span></span>

<span data-ttu-id="3e687-104">Windows 協助工具支援兩種功能，可協助 Windows 開發人員設計可存取的應用程式、輔助技術開發人員建立工具，例如螢幕閱讀程式和放大鏡，而軟體測試工程師會建立自動化腳本來測試 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3e687-104">Windows Accessibility supports two categories of features to help Windows developers design accessible applications, assistive technology developers build tools such as screen readers and magnifiers, and software test engineers create automated scripts for testing Windows applications.</span></span>

## <a name="settings"></a><span data-ttu-id="3e687-105">設定</span><span class="sxs-lookup"><span data-stu-id="3e687-105">Settings</span></span>

<span data-ttu-id="3e687-106">有兩種類型的設定可供使用者 (透過主控台) 中也會公開給開發人員的輕鬆存取中心：</span><span class="sxs-lookup"><span data-stu-id="3e687-106">There are two types of settings available to users (through the Ease of Access Center in Control Panel) that are also exposed to developers:</span></span>

- <span data-ttu-id="3e687-107">[協助工具參數](accessibility-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3e687-107">[Accessibility parameters](accessibility-parameters.md).</span></span> <span data-ttu-id="3e687-108">設定時，這些參數表示應用程式應該變更其預設行為。</span><span class="sxs-lookup"><span data-stu-id="3e687-108">When set, these parameters indicate that applications should change their default behavior.</span></span> <span data-ttu-id="3e687-109">應用程式可以檢查協助工具參數的狀態，以判斷使用者是否想要以應用程式特定的方式提供特殊行為。</span><span class="sxs-lookup"><span data-stu-id="3e687-109">Applications can check the state of an accessibility parameter to determine whether the user wants special behavior that can be provided in an application-specific manner.</span></span> <span data-ttu-id="3e687-110">例如，「聲音聲」參數表示通常使用音效來傳達重要資訊的應用程式，也應該以視覺化方式提供資訊。</span><span class="sxs-lookup"><span data-stu-id="3e687-110">For example, the ShowSounds parameter indicates that an application that typically uses sound to convey important information should also provide the information visually.</span></span>
- <span data-ttu-id="3e687-111">[內建的協助工具功能](built-in-accessibility-features.md)。</span><span class="sxs-lookup"><span data-stu-id="3e687-111">[Built-in accessibility features](built-in-accessibility-features.md).</span></span> <span data-ttu-id="3e687-112">這些功能已內建在系統中，或提供為系統的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3e687-112">These features are built into the system or provided as an extension to the system.</span></span> <span data-ttu-id="3e687-113">它們會影響使用者提供鍵盤和滑鼠輸入至電腦的方式。</span><span class="sxs-lookup"><span data-stu-id="3e687-113">They affect how the user provides keyboard and mouse input to the computer.</span></span> <span data-ttu-id="3e687-114">啟用時，不論正在執行哪些應用程式，都可以使用其功能。</span><span class="sxs-lookup"><span data-stu-id="3e687-114">When enabled, their functionality is available regardless of which applications are running.</span></span> <span data-ttu-id="3e687-115">例如，鍵盤篩選器可讓有行動的使用者更輕鬆地輸入按鍵組合（例如 CTRL + ALT + DEL）。</span><span class="sxs-lookup"><span data-stu-id="3e687-115">An example is a keyboard filter that makes it easier for users with movement impairments to type key combinations such as CTRL+ALT+DEL.</span></span>

<span data-ttu-id="3e687-116">每個協助工具參數和每個內建的協助工具功能都會對應到可使用 [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式進行設定或查詢的系統參數。</span><span class="sxs-lookup"><span data-stu-id="3e687-116">Each accessibility parameter and each built-in accessibility feature corresponds to a system parameter that can be set or queried with the [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

## <a name="win32-apis"></a><span data-ttu-id="3e687-117">Win32 API</span><span class="sxs-lookup"><span data-stu-id="3e687-117">Win32 APIs</span></span>

<span data-ttu-id="3e687-118">Win32 Api 提供協助工具和自動化功能，可協助開發人員建立應用程式和 UI 架構、輔助技術廠商建立工具、測試人員確保品質的執行，以及殘障人士使用他們的電腦和裝置。</span><span class="sxs-lookup"><span data-stu-id="3e687-118">The Win32 APIs provide accessibility and automation features to help developers build applications and UI frameworks, assistive technology vendors build tools, testers ensure quality implementations, and people with disabilities use their computers and devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e687-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e687-119">Related topics</span></span>

[<span data-ttu-id="3e687-120">輔助技術的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="3e687-120">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)