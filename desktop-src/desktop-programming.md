---
description: 在本節中開始學習建立絕佳桌面應用程式的基本概念。
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: 開始使用
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984152"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a><span data-ttu-id="3c456-103">開始使用使用 WIN32 API 的桌面 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="3c456-103">Get started with desktop Windows apps that use the Win32 API</span></span>

<span data-ttu-id="3c456-104">Win32 API (也稱為 Windows API) 是適用於原生 C/C++ Windows 應用程式的原創平台，而這些應用程式需要直接存取 Windows 和硬體。</span><span class="sxs-lookup"><span data-stu-id="3c456-104">The Win32 API (also called the Windows API) is the original platform for native C/C++ Windows applications that require direct access to Windows and hardware.</span></span> <span data-ttu-id="3c456-105">它提供頂級的開發體驗，而不需依賴 managed 執行時間環境，例如適用于 Windows 10) 之 UWP 應用程式的 .NET 和 WinRT (。</span><span class="sxs-lookup"><span data-stu-id="3c456-105">It provides a first-class development experience without depending on a managed runtime environment like .NET and WinRT (for UWP apps for Windows 10).</span></span> <span data-ttu-id="3c456-106">這讓 Win32 API 成為應用程式的首選平台，因為這些應用程式需要最高階效能及直接存取系統硬體。</span><span class="sxs-lookup"><span data-stu-id="3c456-106">This makes the Win32 API the platform of choice for applications that need the highest level of performance and direct access to system hardware.</span></span>

> [!NOTE]
> <span data-ttu-id="3c456-107">本檔涵蓋如何使用 WIN32 API 建立桌面 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-107">This documentation covers how to create desktop Windows apps with the Win32 API.</span></span> <span data-ttu-id="3c456-108">WIN32 API 是數個應用程式平臺的其中一個，您可以用來建立桌面 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-108">The Win32 API is one of several app platforms you can use to build desktop Windows apps.</span></span> <span data-ttu-id="3c456-109">如需其他應用程式平臺的詳細資訊，請參閱 [選擇您的平臺](/windows/apps/desktop/choose-your-platform)。</span><span class="sxs-lookup"><span data-stu-id="3c456-109">For more info about other app platforms, see [Choose your platform](/windows/apps/desktop/choose-your-platform).</span></span>

## <a name="get-set-up"></a><span data-ttu-id="3c456-110">開始設定</span><span class="sxs-lookup"><span data-stu-id="3c456-110">Get set up</span></span>

<span data-ttu-id="3c456-111">遵循這些指示，開始建立使用 WIN32 API 之 Windows 10 的桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-111">Follow these instructions and start creating desktop apps for Windows 10 that use the Win32 API.</span></span>

1. <span data-ttu-id="3c456-112">下載或更新 Visual Studio 2019。</span><span class="sxs-lookup"><span data-stu-id="3c456-112">Download or update Visual Studio 2019.</span></span> <span data-ttu-id="3c456-113">如果您還沒有 Visual Studio 2019，則可以安裝免費的 Microsoft Visual Studio Community 2019。</span><span class="sxs-lookup"><span data-stu-id="3c456-113">If you don't already have Visual Studio 2019, you can install the free Microsoft Visual Studio Community 2019.</span></span> <span data-ttu-id="3c456-114">當您安裝 Visual Studio 時，請務必選取 [ **使用 c + + 的桌面開發** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="3c456-114">When you install Visual Studio, make sure to select the **Desktop development with C++** option.</span></span> <span data-ttu-id="3c456-115">如需下載連結，請參閱我們的 [下載](https://developer.microsoft.com/windows/downloads) 頁面。</span><span class="sxs-lookup"><span data-stu-id="3c456-115">For download links, see our [Downloads](https://developer.microsoft.com/windows/downloads) page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3c456-116">當您安裝 Visual Studio 時，您可以選擇性地選取 [ **.net 桌面開發** ] 和 [ **通用 Windows 平臺開發** ] 選項，以存取其他專案類型和應用程式平臺來建立桌面 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-116">When you install Visual Studio, you can optionally select the **.NET desktop development** and **Universal Windows Platform development** options for access to other project types and app platforms for building desktop Windows apps.</span></span>

2. <span data-ttu-id="3c456-117">如果您想要將傳統型應用程式建立成 [MSIX 套件](/windows/msix/desktop/desktop-to-uwp-root) ，並在開發電腦上測試或偵測已封裝的應用程式，您必須 [在電腦上啟用開發人員模式](/windows/uwp/get-started/enable-your-device-for-development)。</span><span class="sxs-lookup"><span data-stu-id="3c456-117">If you want to build your desktop app into an [MSIX package](/windows/msix/desktop/desktop-to-uwp-root) and test or debug the packaged app on your development computer, you'll need to [enable Developer Mode on your computer](/windows/uwp/get-started/enable-your-device-for-development).</span></span>

> [!NOTE]
> <span data-ttu-id="3c456-118">針對您可以用來設定開發電腦並安裝其他功能或套件的腳本，請參閱 [此 GitHub 專案](https://github.com/Microsoft/windows-dev-box-setup-scripts)。</span><span class="sxs-lookup"><span data-stu-id="3c456-118">For scripts you can use to set up your development computer and install other features or packages, check out [this GitHub project](https://github.com/Microsoft/windows-dev-box-setup-scripts).</span></span>

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a><span data-ttu-id="3c456-119">瞭解如何使用 WIN32 API 建立桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="3c456-119">Learn how to create desktop apps using the Win32 API</span></span>

<span data-ttu-id="3c456-120">如果您不熟悉如何使用 WIN32 API 來建立傳統型應用程式，下列教學課程和文章將協助您入門。</span><span class="sxs-lookup"><span data-stu-id="3c456-120">If you're new to building desktop apps using the Win32 API, the following tutorials and articles will help get you started.</span></span>

| <span data-ttu-id="3c456-121">主題</span><span class="sxs-lookup"><span data-stu-id="3c456-121">Topic</span></span>        | <span data-ttu-id="3c456-122">描述</span><span class="sxs-lookup"><span data-stu-id="3c456-122">Description</span></span>      |
|---------------|-----------------|
| [<span data-ttu-id="3c456-123">建立您的第一個 c + + Win32 應用程式</span><span class="sxs-lookup"><span data-stu-id="3c456-123">Create your first C++ Win32 app</span></span>](LearnWin32/learn-to-program-for-windows.md)    | <span data-ttu-id="3c456-124">本教學課程會教您如何使用 Win32 和 COM Api，以 c + + 撰寫 Windows 程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-124">This tutorial teaches you how to write a Windows program in C++ using Win32 and COM APIs.</span></span>  |
| [<span data-ttu-id="3c456-125">使用 DirectX 建立您的第一個應用程式</span><span class="sxs-lookup"><span data-stu-id="3c456-125">Create your first app using DirectX</span></span>](direct3dgetstarted/building-your-first-directx-app.md) | <span data-ttu-id="3c456-126">本基本教學課程可讓您開始進行 DirectX 應用程式開發。</span><span class="sxs-lookup"><span data-stu-id="3c456-126">This basic tutorial will get you started with DirectX app development.</span></span>            |
| [<span data-ttu-id="3c456-127">64 位元 Windows 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="3c456-127">Programming Guide for 64-bit Windows</span></span>](WinProg64/programming-guide-for-64-bit-windows.md)    | <span data-ttu-id="3c456-128">描述適用于64位版本之 Windows 作業系統的程式設計。</span><span class="sxs-lookup"><span data-stu-id="3c456-128">Describes programming for 64-bit versions of the Windows operating system.</span></span> |
| [<span data-ttu-id="3c456-129">使用 Windows 標頭</span><span class="sxs-lookup"><span data-stu-id="3c456-129">Using the Windows Headers</span></span>](WinProg/using-the-windows-headers.md)     | <span data-ttu-id="3c456-130">概要說明 Windows 標頭檔中使用的一些慣例。</span><span class="sxs-lookup"><span data-stu-id="3c456-130">Provides an overview of some of the conventions used in the Windows header files.</span></span> |

<span data-ttu-id="3c456-131">您也可以流覽 [桌面應用程式範例](https://github.com/Microsoft/Windows-classic-samples)。</span><span class="sxs-lookup"><span data-stu-id="3c456-131">You can also browse the [desktop app samples](https://github.com/Microsoft/Windows-classic-samples).</span></span>

## <a name="modernize-your-desktop-apps-for-windows-10"></a><span data-ttu-id="3c456-132">將您的桌面應用程式現代化以進行 Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c456-132">Modernize your desktop apps for Windows 10</span></span>

<span data-ttu-id="3c456-133">如果您有現有的桌面 Win32 應用程式，通用 Windows 平臺 (UWP) 中有許多功能，可讓您用來在 Windows 10 上提供最佳的可能體驗。</span><span class="sxs-lookup"><span data-stu-id="3c456-133">If you have an existing desktop Win32 app, there are many features in the Universal Windows Platform (UWP) that you can use to deliver the best possible experience on Windows 10.</span></span> <span data-ttu-id="3c456-134">例如，從1903版 Windows 10 開始，您可以使用稱為 XAML 孤島的功能，在桌面 Win32 應用程式中裝載 UWP XAML 控制項。</span><span class="sxs-lookup"><span data-stu-id="3c456-134">For example, starting in Windows 10, version 1903, you can host UWP XAML controls in your desktop Win32 app using a feature called XAML Islands.</span></span>

<span data-ttu-id="3c456-135">這些 UWP 的大部分功能都是以模組化元件的形式提供，您可以在桌面應用程式中依自己的步調採用，而不需要重寫整個應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-135">Most of these UWP features are available as modular components that you can adopt in your desktop app at your own pace without having to rewrite your entire application.</span></span> <span data-ttu-id="3c456-136">您可以選擇要採用 Windows 10 和 UWP 的哪些部分，以增強現有的桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c456-136">You can enhance your existing desktop app by choosing which parts of Windows 10 and UWP to adopt.</span></span>

<span data-ttu-id="3c456-137">如需詳細資訊，請參閱[讓您的傳統型應用程式現代化](/windows/apps/desktop/modernize)。</span><span class="sxs-lookup"><span data-stu-id="3c456-137">For more information, see [Modernize your desktop apps](/windows/apps/desktop/modernize).</span></span>

## <a name="cwinrt"></a><span data-ttu-id="3c456-138">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3c456-138">C++/WinRT</span></span>

<span data-ttu-id="3c456-139">（選擇性）您可以將開發電腦設定為使用 [c + +/WinRT](/windows/uwp/cpp-and-winrt-apis/)。</span><span class="sxs-lookup"><span data-stu-id="3c456-139">Optionally, you can configure your development computer to use [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/).</span></span> <span data-ttu-id="3c456-140">C + +/WinRT 是一種完全標準的新式 c + + 17 語言投射，可讓您輕鬆地從 c + + Win32 desktop 應用程式使用 Windows 執行階段 Api Windows 執行階段 (WinRT) Api。</span><span class="sxs-lookup"><span data-stu-id="3c456-140">C++/WinRT is an entirely standard modern C++17 language projection enables you to easily consume Windows Runtime APIs Windows Runtime (WinRT) APIs from your C++ Win32 desktop application.</span></span> <span data-ttu-id="3c456-141">C + +/WinRT 會實作為以標頭檔為基礎的程式庫。</span><span class="sxs-lookup"><span data-stu-id="3c456-141">C++/WinRT is implemented as a header-file-based library.</span></span>

<span data-ttu-id="3c456-142">設定專案使其適用於 C++/WinRT：</span><span class="sxs-lookup"><span data-stu-id="3c456-142">To configure your project for C++/WinRT:</span></span>

* <span data-ttu-id="3c456-143">針對新專案，您可以安裝 [C++/WinRT Visual Studio 延伸模組 (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264)，並使用該延伸模組隨附的其中一個 C++/WinRT 專案範本。</span><span class="sxs-lookup"><span data-stu-id="3c456-143">For new projects, you can install the [C++/WinRT Visual Studio Extension (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) and use one of the C++/WinRT project templates included in that extension.</span></span>
* <span data-ttu-id="3c456-144">針對現有的 Windows 桌面應用程式專案，您可以在專案中安裝 [CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) NuGet 套件。</span><span class="sxs-lookup"><span data-stu-id="3c456-144">For existing Windows desktop application projects, you can install the [Microsoft.Windows.CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) NuGet package in the project.</span></span>

<span data-ttu-id="3c456-145">如需這些選項的詳細資訊，請參閱[本文章](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package)。</span><span class="sxs-lookup"><span data-stu-id="3c456-145">For more details about these options, see [this article](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).</span></span>

## <a name="whats-new-for-win32-apis-in-windows-10"></a><span data-ttu-id="3c456-146">Windows 10 中的 Win32 Api 的新功能</span><span class="sxs-lookup"><span data-stu-id="3c456-146">What's new for Win32 APIs in Windows 10</span></span>

<span data-ttu-id="3c456-147">若要瞭解 Windows 10 中引進的新 Win32 Api，請參閱 [新功能](whats-new.md)。</span><span class="sxs-lookup"><span data-stu-id="3c456-147">To learn about new Win32 APIs that have been introduced in Windows 10, see [what's new](whats-new.md).</span></span>

## <a name="get-started-with-win32-features-and-technologies"></a><span data-ttu-id="3c456-148">Win32 功能與技術入門</span><span class="sxs-lookup"><span data-stu-id="3c456-148">Get started with Win32 features and technologies</span></span>

<span data-ttu-id="3c456-149">Windows 10 中的許多功能和技術都有 Win32 Api，包括核心使用者介面和視窗型 Api、音訊和圖形以及網路功能。</span><span class="sxs-lookup"><span data-stu-id="3c456-149">Win32 APIs exist for many features and technologies in Windows 10, including core user interface and windowing APIs, audio and graphics, and networking.</span></span> <span data-ttu-id="3c456-150">如需有關使用這些 Api 的指引和程式碼範例， [請參閱我們的功能和技術索引](desktop-app-technologies.md)。</span><span class="sxs-lookup"><span data-stu-id="3c456-150">For guidance and code samples about using these APIs, [see our features and technologies index](desktop-app-technologies.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c456-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c456-151">Related topics</span></span>

* [<span data-ttu-id="3c456-152">開發桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="3c456-152">Develop desktop apps</span></span>](/windows/apps/desktop)
* [<span data-ttu-id="3c456-153">Windows API 參考</span><span class="sxs-lookup"><span data-stu-id="3c456-153">Windows API reference</span></span>](/windows/desktop/api/)
* [<span data-ttu-id="3c456-154">Windows API 索引</span><span class="sxs-lookup"><span data-stu-id="3c456-154">Windows API index</span></span>](/windows/desktop/apiindex/api-index-portal)
* [<span data-ttu-id="3c456-155">Windows 執行階段 c + + 參考</span><span class="sxs-lookup"><span data-stu-id="3c456-155">Windows Runtime C++ reference</span></span>](/windows/desktop/winrt/reference)
