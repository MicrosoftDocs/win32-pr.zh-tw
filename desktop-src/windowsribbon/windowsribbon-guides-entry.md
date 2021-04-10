---
title: Windows 功能區架構開發人員指南
description: 本節所包含的主題將說明 Windows 功能區架構的特定層面。
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，開發人員指南
- 功能區，開發人員指南
- Windows 功能區的開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093115"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="c9627-108">Windows 功能區架構開發人員指南</span><span class="sxs-lookup"><span data-stu-id="c9627-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="c9627-109">本節所包含的主題將說明 Windows 功能區架構的特定層面。</span><span class="sxs-lookup"><span data-stu-id="c9627-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="c9627-110">基本概念</span><span class="sxs-lookup"><span data-stu-id="c9627-110">Basics</span></span>

[<span data-ttu-id="c9627-111">建立功能區應用程式</span><span class="sxs-lookup"><span data-stu-id="c9627-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="c9627-112">若要讓 Windows 功能區架構使用功能區標記檔案，必須將標記檔案編譯成二進位格式的資源檔。</span><span class="sxs-lookup"><span data-stu-id="c9627-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="c9627-113">Microsoft Windows 軟體開發套件 (SDK)  (7.0 或更新版本的 (UICC) 包含專用的功能區標記編譯器，) 此用途。</span><span class="sxs-lookup"><span data-stu-id="c9627-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="c9627-114">除了編譯功能區標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。</span><span class="sxs-lookup"><span data-stu-id="c9627-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="c9627-115">遷移至 Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="c9627-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="c9627-116">依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至功能區架構命令系統 (UI) 的豐富、動態和內容驅動使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c9627-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="c9627-117">這是將應用程式現代化和讓起死回生的簡單且有效的方式，同時也改善了其功能的協助工具、可用性及可探索性。</span><span class="sxs-lookup"><span data-stu-id="c9627-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="c9627-118">瞭解命令和控制項</span><span class="sxs-lookup"><span data-stu-id="c9627-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="c9627-119">將邏輯與展示分開的設計原理，就是激勵功能區架構的命令呈現系統的設計原理，也就是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。</span><span class="sxs-lookup"><span data-stu-id="c9627-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="c9627-120">使用者介面</span><span class="sxs-lookup"><span data-stu-id="c9627-120">User Interface</span></span>

[<span data-ttu-id="c9627-121">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="c9627-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="c9627-122">功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面中廣泛地支援影像資源， (UI) 。</span><span class="sxs-lookup"><span data-stu-id="c9627-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="c9627-123">所有影像資源都是在 [功能區標記](windowsribbon-schema.md) 中宣告，或從功能區主機應用程式進行查詢。</span><span class="sxs-lookup"><span data-stu-id="c9627-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="c9627-124">針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。</span><span class="sxs-lookup"><span data-stu-id="c9627-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="c9627-125">針對 Windows 7 及更早版本，映射資源必須符合 Windows 中所使用的標準 BMP 圖形格式。</span><span class="sxs-lookup"><span data-stu-id="c9627-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="c9627-126">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="c9627-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="c9627-127">功能區命令列中裝載的控制項受限於功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合， (在功能區標記中宣告的架構定義和自訂) 。</span><span class="sxs-lookup"><span data-stu-id="c9627-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="c9627-128">這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。</span><span class="sxs-lookup"><span data-stu-id="c9627-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="c9627-129">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="c9627-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="c9627-130">功能區架構可為開發人員提供健全且一致的模型，以管理各種集合型控制項的動態內容。</span><span class="sxs-lookup"><span data-stu-id="c9627-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="c9627-131">藉由 (UI) 來調整並重新設定功能區使用者介面，這些動態控制項可讓架構在主應用程式和功能區本身中回應使用者互動，並提供彈性來處理各種執行時間環境。</span><span class="sxs-lookup"><span data-stu-id="c9627-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="c9627-132">顯示內容索引標籤</span><span class="sxs-lookup"><span data-stu-id="c9627-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="c9627-133">在功能區架構應用程式中，[內容] 索引標籤是一個隱藏的索引標籤控制項，會在應用程式工作區中的物件（例如影像）已選取或反白顯示時，顯示在索引標籤[列上。](windowsribbon-controls-tab.md)</span><span class="sxs-lookup"><span data-stu-id="c9627-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="c9627-134">使用應用程式模式重新設定功能區</span><span class="sxs-lookup"><span data-stu-id="c9627-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="c9627-135">功能區架構支援動態重新設定和公開功能區使用者介面的核心元素， (UI) 在執行時間，根據應用程式的狀態 (也稱為內容) 。</span><span class="sxs-lookup"><span data-stu-id="c9627-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="c9627-136">宣告並與標記中的特定元素相關聯時，應用程式支援的各種狀態稱為應用程式模式。</span><span class="sxs-lookup"><span data-stu-id="c9627-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="c9627-137">自訂功能區色彩</span><span class="sxs-lookup"><span data-stu-id="c9627-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="c9627-138">功能區架構會公開一組色彩屬性，可讓應用程式在執行時間 (UI) 元素自訂各種功能區使用者介面的外觀。</span><span class="sxs-lookup"><span data-stu-id="c9627-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="c9627-139">顯示功能區</span><span class="sxs-lookup"><span data-stu-id="c9627-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="c9627-140">功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區使用者介面 (UI) 的方式。</span><span class="sxs-lookup"><span data-stu-id="c9627-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="c9627-141">管理性</span><span class="sxs-lookup"><span data-stu-id="c9627-141">Management</span></span>

[<span data-ttu-id="c9627-142">保存功能區狀態</span><span class="sxs-lookup"><span data-stu-id="c9627-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="c9627-143">Windows Ribon framework (功能區) 可讓您在應用程式會話之間保留各種使用者設定和喜好設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9627-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="c9627-144">接聽功能區事件</span><span class="sxs-lookup"><span data-stu-id="c9627-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="c9627-145">功能區架構使用 [Windows 的事件追蹤 (ETW) ](../etw/event-tracing-portal.md) 基礎結構，讓開發人員瞭解使用者如何與應用程式的功能區互動。</span><span class="sxs-lookup"><span data-stu-id="c9627-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="c9627-146">標記編譯器</span><span class="sxs-lookup"><span data-stu-id="c9627-146">Markup Compiler</span></span>

[<span data-ttu-id="c9627-147">編譯功能區標記</span><span class="sxs-lookup"><span data-stu-id="c9627-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="c9627-148">若要讓功能區架構使用 [功能區標記](windowsribbon-schema.md) 檔案，必須將標記檔案編譯成二進位格式資源檔。</span><span class="sxs-lookup"><span data-stu-id="c9627-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="c9627-149">針對此用途，Microsoft Windows 軟體開發套件 (SDK)  (7.0 或更新版本) 中包含了專用標記編譯器（ (UICC) 的 UI 命令編譯器）。</span><span class="sxs-lookup"><span data-stu-id="c9627-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="c9627-150">除了編譯標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。</span><span class="sxs-lookup"><span data-stu-id="c9627-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="c9627-151">瞭解標記編譯器訊息</span><span class="sxs-lookup"><span data-stu-id="c9627-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="c9627-152">Windows 功能區架構 (功能區) 標記編譯器、UI 命令編譯器 (UICC.exe) ，會針對功能區架構和功能區架構所定義的一組額外規則驗證功能區標記。</span><span class="sxs-lookup"><span data-stu-id="c9627-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 