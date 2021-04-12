---
title: 建立功能區應用程式
description: Windows 功能區架構是由兩個不同但相依的開發平臺所組成，以 Extensible Application Markup Language (XAML) 來宣告控制項和其視覺化配置，以及 c + + 元件物件模型 (COM) 型介面集，以定義命令功能和應用程式攔截。 在功能區架構架構中的這一項工作，需要使用架構所提供之豐富 UI 功能的開發人員，必須設計和描述標記中的 UI，然後使用功能區架構 COM 介面將架構連接到主應用程式。
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows 功能區，建立應用程式
- 功能區，建立應用程式
- Windows 功能區，藍圖
- 功能區，藍圖
- Windows 功能區，標記
- 功能區，標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376161"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="972c6-110">建立功能區應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="972c6-111">Windows 功能區架構是由兩個不同但相依的開發平臺所組成：根據 Extensible Application Markup Language 的標記語言 (XAML) 來宣告控制項及其視覺配置，以及 c + + 元件物件模型 (COM) 型介面集，以定義命令功能和應用程式勾點。</span><span class="sxs-lookup"><span data-stu-id="972c6-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="972c6-112">在功能區架構架構中的這一項工作，需要使用架構所提供之豐富 UI 功能的開發人員，必須設計和描述標記中的 UI，然後使用功能區架構 COM 介面將架構連接到主應用程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="972c6-113">功能區藍圖</span><span class="sxs-lookup"><span data-stu-id="972c6-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="972c6-114">寫入標記</span><span class="sxs-lookup"><span data-stu-id="972c6-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="972c6-115">編譯標記</span><span class="sxs-lookup"><span data-stu-id="972c6-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="972c6-116">建立應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="972c6-117">初始化功能區</span><span class="sxs-lookup"><span data-stu-id="972c6-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="972c6-118">將標記連結至應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="972c6-119">編譯應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="972c6-120">執行時間更新和執行次數</span><span class="sxs-lookup"><span data-stu-id="972c6-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="972c6-121">OLE 支援</span><span class="sxs-lookup"><span data-stu-id="972c6-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="972c6-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="972c6-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="972c6-123">功能區藍圖</span><span class="sxs-lookup"><span data-stu-id="972c6-123">Ribbon Roadmap</span></span>

<span data-ttu-id="972c6-124">功能區應用程式的視覺效果（例如顯示的控制項和放置的位置）會在標記中宣告 (請參閱 [使用功能區標記宣告命令和控制項](windowsribbon-schema.md)) 。</span><span class="sxs-lookup"><span data-stu-id="972c6-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="972c6-125">應用程式命令邏輯（例如按下按鈕時所發生的動作）會在程式碼中執行。</span><span class="sxs-lookup"><span data-stu-id="972c6-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="972c6-126">執行功能區並將其併入 Windows 應用程式的程式需要四個基本工作：寫入標記、編譯標記、撰寫程式碼，以及編譯和連結整個應用程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="972c6-127">下圖說明一般功能區執行的工作流程。</span><span class="sxs-lookup"><span data-stu-id="972c6-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![顯示一般功能區執行工作流程的圖表。](images/overviews/ribbonroadmap.png)

<span data-ttu-id="972c6-129">下列各節將更詳細地說明此程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="972c6-130">寫入標記</span><span class="sxs-lookup"><span data-stu-id="972c6-130">Write the Markup</span></span>

<span data-ttu-id="972c6-131">設計功能區 UI 之後，應用程式開發人員的第一個工作就是使用功能區標記來描述 UI。</span><span class="sxs-lookup"><span data-stu-id="972c6-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="972c6-132">功能區架構標記架構檔案（UICC .xsd）是與適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) 一併安裝。</span><span class="sxs-lookup"><span data-stu-id="972c6-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="972c6-133">使用標準安裝路徑時，檔案位於% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 Bin 資料夾中， \] \\ 可供許多 XML 編輯器參考，以提供提示和自動完成。</span><span class="sxs-lookup"><span data-stu-id="972c6-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="972c6-134">功能區控制項、功能區命令 (控制項獨立的元素，這些專案會提供功能區控制項) 的基本功能，而且所有控制項版面配置和視覺關聯性都會在標記中宣告。</span><span class="sxs-lookup"><span data-stu-id="972c6-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="972c6-135">功能區標記的結構強調功能區控制項和命令與兩個主要節點階層之間的差異： [命令和資源](windowsribbon-reference-elements-command.md) 樹狀結構，以及 [視圖](windowsribbon-reference-elements-view.md) 樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="972c6-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="972c6-136">功能區公開的所有容器和動作都會在 [ [命令和資源](windowsribbon-reference-elements-command.md) ] 樹狀結構中宣告。</span><span class="sxs-lookup"><span data-stu-id="972c6-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="972c6-137">每個命令專案都會與 UI 設計所需的一組資源相關聯。</span><span class="sxs-lookup"><span data-stu-id="972c6-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="972c6-138">建立應用程式的命令之後，您可以在 [ [Views](windowsribbon-reference-elements-view.md) ] 樹狀結構中宣告控制項，然後將每個控制項系結至命令以公開命令功能。</span><span class="sxs-lookup"><span data-stu-id="972c6-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="972c6-139">功能區架構會根據此處所宣告的控制項階層，判斷控制項的實際位置。</span><span class="sxs-lookup"><span data-stu-id="972c6-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="972c6-140">下列程式碼範例說明如何宣告按鈕控制項、標示為 Exit 應用程式，並將它與 Exit 命令相關聯。</span><span class="sxs-lookup"><span data-stu-id="972c6-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="972c6-141">雖然您可以針對功能區標記檔案使用任何副檔名，但在檔中使用的是建議的副檔名。</span><span class="sxs-lookup"><span data-stu-id="972c6-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="972c6-142">編譯標記</span><span class="sxs-lookup"><span data-stu-id="972c6-142">Compile the Markup</span></span>

<span data-ttu-id="972c6-143">建立功能區標記檔案之後，必須將它編譯成二進位格式，方法是使用 Windows 軟體發展工具組 (SDK) 隨附的功能區標記編譯器、UI 命令編譯器 (UICC) 。</span><span class="sxs-lookup"><span data-stu-id="972c6-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="972c6-144">主機應用程式在功能區架構初始化期間，會將這個二進位檔案的參考傳遞給 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 方法。</span><span class="sxs-lookup"><span data-stu-id="972c6-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="972c6-145">UICC 可以直接從命令列視窗執行，或新增為 Visual Studio 中的「自訂群組建步驟」。</span><span class="sxs-lookup"><span data-stu-id="972c6-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="972c6-146">下圖顯示 Windows 7 SDK CMD Shell 視窗中的 UICC 標記編譯器。</span><span class="sxs-lookup"><span data-stu-id="972c6-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![在命令列視窗中顯示 uicc.exe 的螢幕擷取畫面。](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="972c6-148">下圖顯示在 Visual Studio 中新增為自訂群組建步驟的 UICC。</span><span class="sxs-lookup"><span data-stu-id="972c6-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![顯示在 visual studio 中新增為自訂群組建步驟 uicc.exe 的螢幕擷取畫面。](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="972c6-150">UICC 會產生三個檔案：標記的二進位版本 (. bml) 、識別碼定義標頭 ( .h 檔) 將標記專案公開給功能區主應用程式，以及 ( .rc 檔的 [資源定義腳本](../menurc/about-resource-files.md) ，) 在編譯時期將功能區影像和字串資源連結至主應用程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="972c6-151">如需編譯功能區架構標記的詳細資訊，請參閱 [編譯功能區標記](windowsribbon-intentcl.md)。</span><span class="sxs-lookup"><span data-stu-id="972c6-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="972c6-152">建置應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-152">Build the Application</span></span>

<span data-ttu-id="972c6-153">功能區應用程式的初步 UI 在標記中設計和實行之後，必須撰寫程式碼來初始化架構、取用標記，然後將標記中宣告的命令系結至應用程式中適當的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="972c6-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="972c6-154">由於功能區架構是以 COM 為基礎，建議功能區專案使用 \_ \_ uuidof () 運算子來參考功能區架構介面 (iid) 的 guid。</span><span class="sxs-lookup"><span data-stu-id="972c6-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="972c6-155">在無法使用 uuidof () 運算子的情況下（ \_ \_ 例如使用非 Microsoft 編譯器或主應用程式是以 C 為基礎的應用程式），iid 必須由應用程式定義，因為它們不包含在 uuid 中。</span><span class="sxs-lookup"><span data-stu-id="972c6-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="972c6-156">如果 Iid 是由應用程式定義，則必須使用 UIRibbon 中指定的 Guid。</span><span class="sxs-lookup"><span data-stu-id="972c6-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="972c6-157">UIRibbon 隨附于 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx) 的一部分，可在% ProgramFiles% \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 包含的標準安裝路徑中找到。</span><span class="sxs-lookup"><span data-stu-id="972c6-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="972c6-158">初始化功能區</span><span class="sxs-lookup"><span data-stu-id="972c6-158">Initialize the Ribbon</span></span>

<span data-ttu-id="972c6-159">下圖說明執行簡單功能區應用程式所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="972c6-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![此圖顯示執行簡單功能區執行所需的步驟。](images/overviews/initializationsteps.png)

<span data-ttu-id="972c6-161">下列步驟詳細說明如何執行簡單的功能區應用程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="972c6-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="972c6-162">CoCreateInstance</span></span>

    <span data-ttu-id="972c6-163">應用程式會使用功能區架構類別識別碼來呼叫標準 COM CoCreateInstance 函數，以取得架構的指標。</span><span class="sxs-lookup"><span data-stu-id="972c6-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="972c6-164">Initialize (hwnd，IUIApplication \*) </span><span class="sxs-lookup"><span data-stu-id="972c6-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="972c6-165">應用程式會呼叫 [**IUIFramework：： Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)，傳遞兩個參數：最上層視窗的控制碼，其中將包含功能區和可讓架構對應用程式進行回呼的 [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 實作為指標。</span><span class="sxs-lookup"><span data-stu-id="972c6-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="972c6-166">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="972c6-166">\[!Important\]</span></span>  
    > <span data-ttu-id="972c6-167">功能區架構會初始化為單一執行緒的單元 (STA) 。</span><span class="sxs-lookup"><span data-stu-id="972c6-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="972c6-168">LoadUI (實例，CoNtext.resourcename) </span><span class="sxs-lookup"><span data-stu-id="972c6-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="972c6-169">應用程式會呼叫 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 來系結標記資源。</span><span class="sxs-lookup"><span data-stu-id="972c6-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="972c6-170">此函數的第一個參數是功能區應用程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="972c6-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="972c6-171">第二個參數是先前編譯之二進位標記資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="972c6-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="972c6-172">藉由將二進位標記傳遞給功能區架構，應用程式就會通知功能區結構應該是什麼，以及控制項的相片順序。</span><span class="sxs-lookup"><span data-stu-id="972c6-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="972c6-173">它也會提供架構資訊清單，以公開 (（例如貼上、剪下、尋找) ），當架構在執行時間進行與命令相關的回呼時，就會使用這些資訊清單。</span><span class="sxs-lookup"><span data-stu-id="972c6-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="972c6-174">[**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) 回呼</span><span class="sxs-lookup"><span data-stu-id="972c6-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="972c6-175">完成步驟1到3之後，功能區架構會知道要在功能區中公開哪些命令。</span><span class="sxs-lookup"><span data-stu-id="972c6-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="972c6-176">不過，在功能區完全正常運作之前，架構仍然需要兩件事：在執行命令時告訴應用程式，以及在執行時間取得命令資源或屬性的方式。</span><span class="sxs-lookup"><span data-stu-id="972c6-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="972c6-177">例如，如果下拉式方塊會出現在 UI 中，則架構必須要求要用來填入下拉式方塊的專案。</span><span class="sxs-lookup"><span data-stu-id="972c6-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="972c6-178">這兩項功能是透過 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) 介面處理。</span><span class="sxs-lookup"><span data-stu-id="972c6-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="972c6-179">具體來說，針對二進位標記中宣告的每個命令 (查看上述) 的步驟3，架構會呼叫 [**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) ，向應用程式要求該命令的 **IUICommandHandler** 物件。</span><span class="sxs-lookup"><span data-stu-id="972c6-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="972c6-180">[**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)介面允許將命令處理常式系結至一或多個命令。</span><span class="sxs-lookup"><span data-stu-id="972c6-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="972c6-181">若要執行 [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 方法 stub （可傳回 E >notimpl），至少需要應用程式， \_ 如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="972c6-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="972c6-182">將標記連結至應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-182">Link the Markup to the Application</span></span>

<span data-ttu-id="972c6-183">此時，標記資源檔必須連結至主應用程式，方法是包含對標記資源定義檔的參考， (其中包含應用程式資源檔中) 標記標頭檔的參考。</span><span class="sxs-lookup"><span data-stu-id="972c6-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="972c6-184">例如，名為 RibbonApp 的應用程式與名為 ribbonUI 的資源檔，需要 RibbonApp .rc 檔中的下列程式列。</span><span class="sxs-lookup"><span data-stu-id="972c6-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="972c6-185">根據所使用的編譯器和連結器，資源定義腳本可能也需要編譯，才能編譯功能區應用程式。</span><span class="sxs-lookup"><span data-stu-id="972c6-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="972c6-186">[資源編譯器 (RC) ](../menurc/using-rc-the-rc-command-line-.md)命令列工具隨附 Microsoft Visual Studio 和 Windows SDK 可用於這項工作。</span><span class="sxs-lookup"><span data-stu-id="972c6-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="972c6-187">編譯應用程式</span><span class="sxs-lookup"><span data-stu-id="972c6-187">Compile the Application</span></span>

<span data-ttu-id="972c6-188">功能區應用程式一經編譯，就可以執行並測試 UI。</span><span class="sxs-lookup"><span data-stu-id="972c6-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="972c6-189">如果 UI 需要調整，而且在核心應用程式程式碼中沒有任何相關聯的命令處理常式變更，請修改標記原始程式檔、使用 UICC.exe 重新編譯標記，然後連結新的標記資源檔。</span><span class="sxs-lookup"><span data-stu-id="972c6-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="972c6-190">當應用程式重新開機時，就會顯示修改過的 UI。</span><span class="sxs-lookup"><span data-stu-id="972c6-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="972c6-191">這一切都可以在不觸及核心應用程式程式碼的情況下使用，這是比標準應用程式開發和散發更大的改進。</span><span class="sxs-lookup"><span data-stu-id="972c6-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="972c6-192">執行時間更新和執行次數</span><span class="sxs-lookup"><span data-stu-id="972c6-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="972c6-193">功能區架構的執行時間通訊結構是以推送和提取或雙向呼叫端（model）為基礎。</span><span class="sxs-lookup"><span data-stu-id="972c6-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="972c6-194">此模型可讓架構在執行命令時通知應用程式，並允許架構和應用程式查詢、更新和使屬性值和功能區資源失效。</span><span class="sxs-lookup"><span data-stu-id="972c6-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="972c6-195">這項功能是透過一些介面和方法提供。</span><span class="sxs-lookup"><span data-stu-id="972c6-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="972c6-196">架構會透過 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法，從功能區應用程式提取更新的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="972c6-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="972c6-197">命令識別碼和屬性索引鍵（可識別要更新的命令屬性）會傳遞至方法，該方法會將該屬性索引鍵的值傳回或推送至架構。</span><span class="sxs-lookup"><span data-stu-id="972c6-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="972c6-198">當執行命令時，架構會呼叫 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) ，同時識別命令識別碼和發生 ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)) 的執行類型。</span><span class="sxs-lookup"><span data-stu-id="972c6-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="972c6-199">這是應用程式為命令指定執行邏輯的位置。</span><span class="sxs-lookup"><span data-stu-id="972c6-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="972c6-200">下圖說明在架構和應用程式之間執行命令的執行時間通訊。</span><span class="sxs-lookup"><span data-stu-id="972c6-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![此圖顯示功能區架構與主應用程式之間的執行時間通訊範例。](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="972c6-202">最初在應用程式中顯示功能區時，不需要執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 和 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 函式。</span><span class="sxs-lookup"><span data-stu-id="972c6-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="972c6-203">不過，若要確保應用程式在使用者執行命令時正確運作，就必須使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="972c6-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="972c6-204">OLE 支援</span><span class="sxs-lookup"><span data-stu-id="972c6-204">OLE Support</span></span>

<span data-ttu-id="972c6-205">功能區應用程式可以設定為 OLE 伺服器，以支援就地 OLE 啟用。</span><span class="sxs-lookup"><span data-stu-id="972c6-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="972c6-206">在 OLE 伺服器應用程式中建立的物件會在插入 (貼上或放置) 至 OLE 用戶端應用程式 (或容器) 時，維持與伺服器應用程式的關聯。</span><span class="sxs-lookup"><span data-stu-id="972c6-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="972c6-207">在就地 OLE 啟用中，按兩下用戶端應用程式中的物件會開啟伺服器應用程式的專用實例，並載入物件進行編輯。</span><span class="sxs-lookup"><span data-stu-id="972c6-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="972c6-208">當伺服器應用程式關閉時，對物件所做的所有變更都會反映在用戶端應用程式中。</span><span class="sxs-lookup"><span data-stu-id="972c6-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="972c6-209">功能區架構不支援就地 OLE 啟用。</span><span class="sxs-lookup"><span data-stu-id="972c6-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="972c6-210">在以功能區為基礎的 OLE 伺服器中建立的物件，無法從 OLE 用戶端應用程式中進行編輯。</span><span class="sxs-lookup"><span data-stu-id="972c6-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="972c6-211">需要伺服器應用程式的外部專用實例。</span><span class="sxs-lookup"><span data-stu-id="972c6-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="972c6-212">相關主題</span><span class="sxs-lookup"><span data-stu-id="972c6-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="972c6-213">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="972c6-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="972c6-214">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="972c6-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="972c6-215">功能區設計流程</span><span class="sxs-lookup"><span data-stu-id="972c6-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




