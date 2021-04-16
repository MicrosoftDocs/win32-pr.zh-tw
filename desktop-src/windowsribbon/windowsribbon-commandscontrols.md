---
title: 瞭解命令和控制項
description: 將邏輯與展示分開的設計原理，就是激勵 Windows 功能區架構 \ 郵件的命令呈現系統的設計原理，這是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Windows 功能區，命令總覽
- 功能區，命令總覽
- Windows 功能區，控制項總覽
- 功能區、控制項總覽
- Windows 功能區的命令系統
- Windows 功能區的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571519"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="1637f-109">瞭解命令和控制項</span><span class="sxs-lookup"><span data-stu-id="1637f-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="1637f-110">將邏輯與展示分開的設計原理，就是激勵 Windows 功能區架構的命令呈現系統的設計原理，也就是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。</span><span class="sxs-lookup"><span data-stu-id="1637f-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="1637f-111">簡介</span><span class="sxs-lookup"><span data-stu-id="1637f-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="1637f-112">Windows 功能區命令系統</span><span class="sxs-lookup"><span data-stu-id="1637f-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="1637f-113">控制項</span><span class="sxs-lookup"><span data-stu-id="1637f-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="1637f-114">命令</span><span class="sxs-lookup"><span data-stu-id="1637f-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="1637f-115">作用中的命令體驗</span><span class="sxs-lookup"><span data-stu-id="1637f-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="1637f-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1637f-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="1637f-117">簡介</span><span class="sxs-lookup"><span data-stu-id="1637f-117">Introduction</span></span>

<span data-ttu-id="1637f-118">本文討論功能區架構命令系統的設計。</span><span class="sxs-lookup"><span data-stu-id="1637f-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="1637f-119">它描述命令和控制項的概念，並探索它們如何一起運作，以提供豐富的命令體驗，並提供主機新的 UI 功能。</span><span class="sxs-lookup"><span data-stu-id="1637f-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="1637f-120">Windows 功能區命令系統</span><span class="sxs-lookup"><span data-stu-id="1637f-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="1637f-121">在功能區架構中，命令和控制項都是獨立的實體。</span><span class="sxs-lookup"><span data-stu-id="1637f-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="1637f-122">命令是一個不含標記法條件約束的抽象結構，表示特定工作或功能類別。</span><span class="sxs-lookup"><span data-stu-id="1637f-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="1637f-123">另一方面，控制項是透過功能區 UI 公開命令功能的實體物件。</span><span class="sxs-lookup"><span data-stu-id="1637f-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="1637f-124">這項區別能讓您定義無 UI 詳細資料的命令，並能夠在動作意圖上執行，而不需要管理叫用動作的方式。</span><span class="sxs-lookup"><span data-stu-id="1637f-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="1637f-125">控制項</span><span class="sxs-lookup"><span data-stu-id="1637f-125">Controls</span></span>

<span data-ttu-id="1637f-126">控制項是命令呈現所需的 UI 物件。</span><span class="sxs-lookup"><span data-stu-id="1637f-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="1637f-127">架構會根據使用者互動以及一組固有的屬性和行為，在執行時間呈現和管理它們。</span><span class="sxs-lookup"><span data-stu-id="1637f-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="1637f-128">也稱為彈性配置，架構管理的 UI 彈性是功能區的最大優點之一。</span><span class="sxs-lookup"><span data-stu-id="1637f-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="1637f-129">功能區控制項可透過架構相依或開發人員定義的版面配置範本，自動自行重新設定，而這些範本可以回應各種執行時間需求，而不需要撰寫任何一行簡報程式碼。</span><span class="sxs-lookup"><span data-stu-id="1637f-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="1637f-130">如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="1637f-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="1637f-131">除了調適型配置的優點之外，許多複雜的功能區控制項都能為特定的 UI 問題空間提供獨立的解決方案。</span><span class="sxs-lookup"><span data-stu-id="1637f-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="1637f-132">藉由提供精密的互動模型，功能區控制項（例如 FontControl 或 ColorPicker）可讓您透過實際字型或色彩屬性的屬性包，以更抽象的詞彙來運算元據，而不是透過標準 Windows 控制項的各種子控制項、列舉和索引值。</span><span class="sxs-lookup"><span data-stu-id="1637f-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="1637f-133">命令</span><span class="sxs-lookup"><span data-stu-id="1637f-133">Commands</span></span>

<span data-ttu-id="1637f-134">鬆散結合功能區控制項來公開其功能，命令執行是主應用程式的網域，並採用事件接聽程式、命令處理常式和各種命令屬性的形式。</span><span class="sxs-lookup"><span data-stu-id="1637f-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="1637f-135">命令會在具有唯一識別碼的功能區標記中宣告，或在編譯時指派標記編譯器產生的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1637f-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="1637f-136">命令會透過命令名稱與控制項相關聯，但不同于控制項，其實際功能是在程式碼中定義，而這些程式碼會透過命令識別碼系結至特定的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="1637f-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="1637f-137">在編譯時，此識別碼會儲存在識別碼定義標頭檔中，該檔案會在功能區主應用程式中公開命令至其對應的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="1637f-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="1637f-138">每個命令都有一種基礎命令類型，在 [**UI \_ COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) 列舉中有詳細的述。</span><span class="sxs-lookup"><span data-stu-id="1637f-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="1637f-139">作用中的命令體驗</span><span class="sxs-lookup"><span data-stu-id="1637f-139">The Command Experience In Action</span></span>

<span data-ttu-id="1637f-140">功能區快速存取工具列會示範此命令模型的功能 (QAT) 。</span><span class="sxs-lookup"><span data-stu-id="1637f-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="1637f-141">QAT 可讓使用者輕鬆地針對功能區 UI 中的任何控制項定義自己的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1637f-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="1637f-142">當使用者在功能區控制項上按一下滑鼠右鍵，並從內容功能表選取 [ **加入至快速存取] 工具列** 時，會在執行時間將快捷方式動態加入至 QAT。</span><span class="sxs-lookup"><span data-stu-id="1637f-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="1637f-143">下圖顯示從命令的 [ **貼** 上] 和 [ **貼** 上] 命令（以 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項表示）在 Windows 7 繪圖的功能區中。</span><span class="sxs-lookup"><span data-stu-id="1637f-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![microsoft 油漆功能區中 [貼上] splitbutton 的圖片。](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="1637f-145">下圖顯示來自命令的相同 **貼** 上和 **貼** 上，在 Windows 7 的功能區 QAT 中仍以 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項表示。</span><span class="sxs-lookup"><span data-stu-id="1637f-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![microsoft 油漆 qat 中 [貼上] splitbutton 的圖片。](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="1637f-147">當控制項由 QAT 主控時，控制項的新實例會維護原始控制項的所有功能，而不需要其他事件接聽程式和命令處理常式來支援它。</span><span class="sxs-lookup"><span data-stu-id="1637f-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="1637f-148">這兩個控制項都透過共用命令識別碼系結至相同的功能區命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="1637f-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="1637f-149">如此一來，無論叫用哪一個控制項，架構都會將兩者視為一個。</span><span class="sxs-lookup"><span data-stu-id="1637f-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="1637f-150">在設計階段將命令合併到 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 時，也會實現相同的優點。</span><span class="sxs-lookup"><span data-stu-id="1637f-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="1637f-151">在此情況下，不論 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項是否出現在功能區、QAT 或 **CoNtextPopup** 中，都可以使用貼入命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="1637f-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1637f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="1637f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1637f-153">Windows 功能區架構簡介</span><span class="sxs-lookup"><span data-stu-id="1637f-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="1637f-154">建立功能區應用程式</span><span class="sxs-lookup"><span data-stu-id="1637f-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="1637f-155">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="1637f-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 