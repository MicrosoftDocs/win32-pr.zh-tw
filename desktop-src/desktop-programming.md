---
description: 在本節中開始學習建立絕佳桌面應用程式的基本概念。
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: 開始使用
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f791589d73447798a7721c52164a2002b48a792959c698b835039293ce6004d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755008"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>開始使用使用 WIN32 API 的桌面 Windows 應用程式

Win32 API (也稱為 Windows API) 是適用於原生 C/C++ Windows 應用程式的原創平台，而這些應用程式需要直接存取 Windows 和硬體。 它提供頂級的開發體驗，而不需依賴 managed 執行時間環境，例如適用于 Windows 10) 之 UWP 應用程式的 .net 和 WinRT (。 這讓 Win32 API 成為應用程式的首選平台，因為這些應用程式需要最高階效能及直接存取系統硬體。

> [!NOTE]
> 本檔涵蓋如何使用 WIN32 API 建立桌面 Windows 應用程式。 WIN32 API 是數個應用程式平臺的其中一個，您可以用來建立桌面 Windows 應用程式。 如需其他應用程式平臺的詳細資訊，請參閱 [選擇您的平臺](/windows/apps/desktop/choose-your-platform)。

## <a name="get-set-up"></a>開始設定

遵循這些指示，開始建立使用 WIN32 API 之 Windows 10 的桌面應用程式。

1. 下載或更新 Visual Studio 2019。 如果您還沒有 Visual Studio 2019，則可以安裝免費的 Microsoft Visual Studio Community 2019。 當您安裝 Visual Studio 時，請務必選取 [**使用 c + + 的桌面開發**] 選項。 如需下載連結，請參閱我們的 [下載](https://developer.microsoft.com/windows/downloads) 頁面。

    > [!NOTE]
    > 當您安裝 Visual Studio 時，您可以選擇性地選取 [ **.net 桌面開發**] 和 [**通用 Windows 平臺開發**] 選項，以存取其他專案類型和應用程式平臺，以建立桌面 Windows 應用程式。

2. 如果您想要將傳統型應用程式建立成 [MSIX 套件](/windows/msix/desktop/desktop-to-uwp-root) ，並在開發電腦上測試或偵測已封裝的應用程式，您必須 [在電腦上啟用開發人員模式](/windows/uwp/get-started/enable-your-device-for-development)。

> [!NOTE]
> 針對您可以用來設定開發電腦並安裝其他功能或封裝的腳本，請參閱[此 GitHub 專案](https://github.com/Microsoft/windows-dev-box-setup-scripts)。

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>瞭解如何使用 WIN32 API 建立桌面應用程式

如果您不熟悉如何使用 WIN32 API 來建立傳統型應用程式，下列教學課程和文章將協助您入門。

| 主題        | 描述      |
|---------------|-----------------|
| [建立您的第一個 c + + Win32 應用程式](LearnWin32/learn-to-program-for-windows.md)    | 本教學課程會教您如何使用 Win32 和 COM api 在 c + + 中撰寫 Windows 程式。  |
| [使用 DirectX 建立您的第一個應用程式](direct3dgetstarted/building-your-first-directx-app.md) | 本基本教學課程可讓您開始進行 DirectX 應用程式開發。            |
| [64 位元 Windows 程式設計手冊](WinProg64/programming-guide-for-64-bit-windows.md)    | 描述 Windows 作業系統64位版本的程式設計。 |
| [使用 Windows 標頭](WinProg/using-the-windows-headers.md)     | 提供 Windows 標頭檔中使用的一些慣例總覽。 |

您也可以流覽 [桌面應用程式範例](https://github.com/Microsoft/Windows-classic-samples)。

## <a name="modernize-your-desktop-apps-for-windows-10"></a>將您的桌面應用程式現代化以進行 Windows 10

如果您有現有的桌面 Win32 應用程式，通用 Windows 平臺 (UWP) 中有許多功能，可讓您用來在 Windows 10 上提供最佳的可能體驗。 例如，從1903版 Windows 10 開始，您可以使用稱為 XAML 孤島的功能，在桌面 Win32 應用程式中裝載 UWP XAML 控制項。

這些 UWP 的大部分功能都是以模組化元件的形式提供，您可以在桌面應用程式中依自己的步調採用，而不需要重寫整個應用程式。 您可以選擇要採用 Windows 10 和 UWP 的哪些部分，以增強現有的桌面應用程式。

如需詳細資訊，請參閱[讓您的傳統型應用程式現代化](/windows/apps/desktop/modernize)。

## <a name="cwinrt"></a>C++/WinRT

（選擇性）您可以將開發電腦設定為使用 [c + +/WinRT](/windows/uwp/cpp-and-winrt-apis/)。 c + +/WinRT 是一種完全標準的新式 c + + 17 語言投射，可讓您輕鬆地從 c + + Win32 desktop 應用程式使用 Windows 執行階段 api Windows 執行階段 (WinRT) api。 C + +/WinRT 會實作為以標頭檔為基礎的程式庫。

設定專案使其適用於 C++/WinRT：

* 針對新專案，您可以安裝 [C++/WinRT Visual Studio 延伸模組 (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264)，並使用該延伸模組隨附的其中一個 C++/WinRT 專案範本。
* 針對現有的 Windows 桌面應用程式專案，您可以安裝[Microsoft Windows。](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/)在專案中 CppWinRT NuGet 套件。

如需這些選項的詳細資訊，請參閱[本文章](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package)。

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Windows 10 中的 Win32 Api 的新功能

若要瞭解 Windows 10 中引進的新 Win32 api，請參閱[新功能](whats-new.md)。

## <a name="get-started-with-win32-features-and-technologies"></a>Win32 功能與技術入門

Windows 10 中的許多功能和技術都有 Win32 api，包括核心使用者介面和視窗型 api、音訊和圖形以及網路功能。 如需有關使用這些 Api 的指引和程式碼範例， [請參閱我們的功能和技術索引](desktop-app-technologies.md)。

## <a name="related-topics"></a>相關主題

* [開發桌面應用程式](/windows/apps/desktop)
* [WindowsAPI 參考](/windows/desktop/api/)
* [Windows API 索引](/windows/desktop/apiindex/api-index-portal)
* [Windows執行時間 c + + 參考](/windows/desktop/winrt/reference)
