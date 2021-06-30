---
title: 啟用視覺化樣式
description: 本主題說明如何設定您的應用程式，以確保通用控制項會顯示在使用者的慣用視覺效果樣式中。
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102167"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="40b34-103">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="40b34-103">Enabling Visual Styles</span></span>

<span data-ttu-id="40b34-104">本主題說明如何設定您的應用程式，以確保通用控制項會顯示在使用者的慣用視覺效果樣式中。</span><span class="sxs-lookup"><span data-stu-id="40b34-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="40b34-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="40b34-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="40b34-106">使用資訊清單或指示詞，以確保視覺效果樣式可以套用至應用程式</span><span class="sxs-lookup"><span data-stu-id="40b34-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="40b34-107">在只使用標準延伸模組的應用程式中使用 ComCtl32.dll 第6版</span><span class="sxs-lookup"><span data-stu-id="40b34-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="40b34-108">在主控台中使用 Comctl32.dll 第6版或 RunDll32.exe執行的 DLL </span><span class="sxs-lookup"><span data-stu-id="40b34-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="40b34-109">將視覺化樣式支援新增至延伸模組、外掛程式、MMC 嵌入式管理單元或進入進程的 DLL</span><span class="sxs-lookup"><span data-stu-id="40b34-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="40b34-110">關閉視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="40b34-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="40b34-111">使用視覺效果樣式搭配 HTML 內容</span><span class="sxs-lookup"><span data-stu-id="40b34-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="40b34-112">未套用視覺化樣式時</span><span class="sxs-lookup"><span data-stu-id="40b34-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="40b34-113">讓您的應用程式與舊版 Windows 相容</span><span class="sxs-lookup"><span data-stu-id="40b34-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="40b34-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="40b34-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="40b34-115">使用資訊清單或指示詞，以確保視覺效果樣式可以套用至應用程式</span><span class="sxs-lookup"><span data-stu-id="40b34-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="40b34-116">若要讓您的應用程式使用視覺化樣式，您必須使用 ComCtl32.dll 6 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="40b34-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="40b34-117">因為第6版無法轉散發套件，只有當您的應用程式是在包含它的 Windows 版本上執行時才可使用。</span><span class="sxs-lookup"><span data-stu-id="40b34-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="40b34-118">Windows 隨附第5版和第6版。</span><span class="sxs-lookup"><span data-stu-id="40b34-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="40b34-119">ComCtl32.dll 第6版包含使用者控制項和通用控制項。</span><span class="sxs-lookup"><span data-stu-id="40b34-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="40b34-120">根據預設，應用程式會使用 User32.dll 中定義的使用者控制項，以及 ComCtl32.dll 第5版中所定義的通用控制項。</span><span class="sxs-lookup"><span data-stu-id="40b34-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="40b34-121">如需 DLL 版本及其散發平臺清單，請參閱 [通用控制項版本](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="40b34-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="40b34-122">如果您想要讓應用程式使用視覺化樣式，則必須加入應用程式資訊清單或編譯器指示詞，指出如果有的話，應使用 ComCtl32.dll 第6版。</span><span class="sxs-lookup"><span data-stu-id="40b34-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="40b34-123">應用程式資訊清單可讓應用程式指定所需的元件版本。</span><span class="sxs-lookup"><span data-stu-id="40b34-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="40b34-124">在 Microsoft Win32 中，元件是一組 Dll 以及這些 Dll 中包含的可擴充區分版本物件清單。</span><span class="sxs-lookup"><span data-stu-id="40b34-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="40b34-125">資訊清單是以 XML 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="40b34-125">Manifests are written in XML.</span></span> <span data-ttu-id="40b34-126">應用程式資訊清單檔的名稱是可執行檔的名稱，後面接著副檔名 .manifest;例如 MyApp.exe 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="40b34-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="40b34-127">下列範例資訊清單顯示第一個區段描述資訊清單本身。</span><span class="sxs-lookup"><span data-stu-id="40b34-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="40b34-128">下表顯示 [資訊清單描述] 區段中 **assemblyIdentity** 元素所設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="40b34-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="40b34-129">屬性</span><span class="sxs-lookup"><span data-stu-id="40b34-129">Attribute</span></span>             | <span data-ttu-id="40b34-130">描述</span><span class="sxs-lookup"><span data-stu-id="40b34-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b34-131">version</span><span class="sxs-lookup"><span data-stu-id="40b34-131">version</span></span>               | <span data-ttu-id="40b34-132">資訊清單的版本。</span><span class="sxs-lookup"><span data-stu-id="40b34-132">Version of the manifest.</span></span> <span data-ttu-id="40b34-133">版本的格式必須是 (主要的.. n n n n. n n n n. n n n n. n n n <= 65535) 。</span><span class="sxs-lookup"><span data-stu-id="40b34-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="40b34-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="40b34-134">processorArchitecture</span></span> | <span data-ttu-id="40b34-135">開發應用程式的處理器。</span><span class="sxs-lookup"><span data-stu-id="40b34-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="40b34-136">NAME</span><span class="sxs-lookup"><span data-stu-id="40b34-136">name</span></span>                  | <span data-ttu-id="40b34-137">包括公司名稱、產品名稱和應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="40b34-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="40b34-138">type</span><span class="sxs-lookup"><span data-stu-id="40b34-138">type</span></span>                  | <span data-ttu-id="40b34-139">應用程式的類型，例如 Win32。</span><span class="sxs-lookup"><span data-stu-id="40b34-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="40b34-140">範例資訊清單也會提供應用程式的描述，並指定應用程式相依性。</span><span class="sxs-lookup"><span data-stu-id="40b34-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="40b34-141">下表顯示 [相依性] 區段中 **assemblyIdentity** 元素所設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="40b34-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="40b34-142">屬性</span><span class="sxs-lookup"><span data-stu-id="40b34-142">Attribute</span></span>             | <span data-ttu-id="40b34-143">描述</span><span class="sxs-lookup"><span data-stu-id="40b34-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="40b34-144">type</span><span class="sxs-lookup"><span data-stu-id="40b34-144">type</span></span>                  | <span data-ttu-id="40b34-145">相依性元件的類型，例如 Win32。</span><span class="sxs-lookup"><span data-stu-id="40b34-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="40b34-146">NAME</span><span class="sxs-lookup"><span data-stu-id="40b34-146">name</span></span>                  | <span data-ttu-id="40b34-147">元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="40b34-147">Name of the component.</span></span>                           |
| <span data-ttu-id="40b34-148">version</span><span class="sxs-lookup"><span data-stu-id="40b34-148">version</span></span>               | <span data-ttu-id="40b34-149">元件的版本。</span><span class="sxs-lookup"><span data-stu-id="40b34-149">Version of the component.</span></span>                        |
| <span data-ttu-id="40b34-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="40b34-150">processorArchitecture</span></span> | <span data-ttu-id="40b34-151">設計元件的處理器。</span><span class="sxs-lookup"><span data-stu-id="40b34-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="40b34-152">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="40b34-152">publicKeyToken</span></span>        | <span data-ttu-id="40b34-153">與此元件搭配使用的金鑰 token。</span><span class="sxs-lookup"><span data-stu-id="40b34-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="40b34-154">語言</span><span class="sxs-lookup"><span data-stu-id="40b34-154">language</span></span>              | <span data-ttu-id="40b34-155">元件的語言。</span><span class="sxs-lookup"><span data-stu-id="40b34-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="40b34-156">以下是資訊清單檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="40b34-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40b34-157">如果您的應用程式是以32位 Windows 平臺為目標，請將 **processorArchitecture** 專案設定為 **"X86"** ，如果您的應用程式是以64位 windows 平臺為目標，則設定為 **"amd64"** 。</span><span class="sxs-lookup"><span data-stu-id="40b34-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="40b34-158">您也可以指定 **" \* "**，以確保所有平臺皆為目標，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="40b34-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="40b34-159">如果您使用 Microsoft Visual C++ 2005 或更新版本，您可以將下列編譯器指示詞新增至您的原始程式碼，而不是以手動方式建立資訊清單。</span><span class="sxs-lookup"><span data-stu-id="40b34-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="40b34-160">為了方便閱讀，此指示詞分成數行。</span><span class="sxs-lookup"><span data-stu-id="40b34-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="40b34-161">下列主題描述將視覺效果樣式套用至不同應用程式類型的步驟。</span><span class="sxs-lookup"><span data-stu-id="40b34-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="40b34-162">請注意，資訊清單格式在每個案例中都相同。</span><span class="sxs-lookup"><span data-stu-id="40b34-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="40b34-163">在只使用標準延伸模組的應用程式中使用 ComCtl32.dll 第6版</span><span class="sxs-lookup"><span data-stu-id="40b34-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="40b34-164">以下是未使用協力廠商擴充功能的應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="40b34-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="40b34-165">Calculator</span><span class="sxs-lookup"><span data-stu-id="40b34-165">Calculator</span></span>
-   <span data-ttu-id="40b34-166">Windows Vista 和 Windows 7) 的空當接龍 (</span><span class="sxs-lookup"><span data-stu-id="40b34-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="40b34-167">Windows Vista 和 Windows 7) 的 < a0/&gt; 掃雷 (</span><span class="sxs-lookup"><span data-stu-id="40b34-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="40b34-168">[記事本]</span><span class="sxs-lookup"><span data-stu-id="40b34-168">Notepad</span></span>
-   <span data-ttu-id="40b34-169">Windows Vista 和 Windows 7) 的紙牌 (</span><span class="sxs-lookup"><span data-stu-id="40b34-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="40b34-170">**建立資訊清單，並讓您的應用程式使用視覺化樣式。**</span><span class="sxs-lookup"><span data-stu-id="40b34-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="40b34-171">連結至 Comctl32.dll .lib 並呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)。</span><span class="sxs-lookup"><span data-stu-id="40b34-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="40b34-172">將名為 YourApp.exe 的檔案新增至具有 XML 資訊清單格式的來源樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="40b34-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="40b34-173">將資訊清單新增至您應用程式的資源檔，如下所示：</span><span class="sxs-lookup"><span data-stu-id="40b34-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="40b34-174">當您將前一個專案加入至資源時，您必須將它格式化為一行。</span><span class="sxs-lookup"><span data-stu-id="40b34-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="40b34-175">或者，您可以將 XML 資訊清單檔案放在與應用程式可執行檔相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="40b34-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="40b34-176">作業系統會先從檔案系統載入資訊清單，然後檢查可執行檔的資源區段。</span><span class="sxs-lookup"><span data-stu-id="40b34-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="40b34-177">檔案系統版本優先。</span><span class="sxs-lookup"><span data-stu-id="40b34-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="40b34-178">當您建立應用程式時，資訊清單會新增為二進位資源。</span><span class="sxs-lookup"><span data-stu-id="40b34-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="40b34-179">在主控台中使用 Comctl32.dll 第6版或 RunDll32.exe 執行的 DLL</span><span class="sxs-lookup"><span data-stu-id="40b34-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="40b34-180">**建立資訊清單，並讓您的應用程式使用視覺化樣式。**</span><span class="sxs-lookup"><span data-stu-id="40b34-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="40b34-181">連結至 Comctl32.dll .lib 並呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)。</span><span class="sxs-lookup"><span data-stu-id="40b34-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="40b34-182">將名為 YourApp.cpl 的檔案新增至具有 XML 資訊清單格式的來源樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="40b34-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="40b34-183">將資訊清單新增至您應用程式的資源檔，作為資源識別碼123。</span><span class="sxs-lookup"><span data-stu-id="40b34-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="40b34-184">當您撰寫主控台的應用程式時，請將它放在適當的類別中。</span><span class="sxs-lookup"><span data-stu-id="40b34-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="40b34-185">主控台現在支援主控台應用程式的分類。</span><span class="sxs-lookup"><span data-stu-id="40b34-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="40b34-186">這表示主控台的應用程式可以被指派識別碼，並區分為工作區域，例如新增或移除程式、外觀和主題，或日期、時間、語言和地區選項。</span><span class="sxs-lookup"><span data-stu-id="40b34-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="40b34-187">將視覺化樣式支援新增至延伸模組、外掛程式、MMC 嵌入式管理單元或進入進程的 DLL</span><span class="sxs-lookup"><span data-stu-id="40b34-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="40b34-188">視覺化樣式的支援可新增至延伸模組、外掛程式、MMC 嵌入式管理單元，或進入進程的 DLL。</span><span class="sxs-lookup"><span data-stu-id="40b34-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="40b34-189">例如，使用下列步驟來新增 Microsoft Management Console (MMC) 嵌入式管理單元的視覺化樣式支援。</span><span class="sxs-lookup"><span data-stu-id="40b34-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="40b34-190">使用-DISOLATION 感知啟用旗標編譯您的嵌入式管理單元， \_ \_ 或在 \# 包含 "windows .h" 語句之前插入下列語句。</span><span class="sxs-lookup"><span data-stu-id="40b34-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="40b34-191">如需啟用隔離感知的詳細資訊 \_ \_ ，請參閱 [隔離元件](/windows/desktop/SbsCs/isolating-components)。</span><span class="sxs-lookup"><span data-stu-id="40b34-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="40b34-192">在嵌入式管理單元來源中包含通用控制標頭檔。</span><span class="sxs-lookup"><span data-stu-id="40b34-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="40b34-193">將名為 YourApp 的檔案新增至使用 XML 資訊清單格式的來源樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="40b34-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="40b34-194">將資訊清單新增至嵌入式管理單元的資源檔。</span><span class="sxs-lookup"><span data-stu-id="40b34-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="40b34-195">如需將資訊清單新增至資源檔的詳細資訊，請參閱 [在使用延伸模組、外掛程式或 DLL 的應用程式中使用 comctl32.dll 第6版](/previous-versions//ms649781(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="40b34-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="40b34-196">關閉視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="40b34-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="40b34-197">您可以藉由呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 函式來關閉控制項或視窗中所有控制項的視覺化樣式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="40b34-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="40b34-198">在上述範例中， *hwnd* 是停用視覺化樣式的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="40b34-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="40b34-199">在呼叫之後，控制項不會呈現視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="40b34-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="40b34-200">使用視覺效果樣式搭配 HTML 內容</span><span class="sxs-lookup"><span data-stu-id="40b34-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="40b34-201">修改階層式樣式表 (CSS) 屬性（例如背景或框線）的 HTML 頁面未套用視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="40b34-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="40b34-202">它們會顯示指定的 CSS 屬性。</span><span class="sxs-lookup"><span data-stu-id="40b34-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="40b34-203">當指定為內容的一部分時，大部分的 CSS 屬性會套用至已套用視覺化樣式的元素。</span><span class="sxs-lookup"><span data-stu-id="40b34-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="40b34-204">根據預設，視覺效果樣式會套用至 Microsoft Internet Explorer 6 和更新版本中所顯示頁面上的內部 HTML 控制項。</span><span class="sxs-lookup"><span data-stu-id="40b34-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="40b34-205">若要關閉 HTML 網頁的視覺化樣式，請將中繼標記新增至</span><span class="sxs-lookup"><span data-stu-id="40b34-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="40b34-206">＞一節探討各類型資料來源的重新整理。</span><span class="sxs-lookup"><span data-stu-id="40b34-206">section.</span></span> <span data-ttu-id="40b34-207">這項技術也適用于封裝為 HTML 應用程式 (Hta) 的內容。</span><span class="sxs-lookup"><span data-stu-id="40b34-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="40b34-208">若要關閉視覺化樣式，中繼標記必須如下所示：</span><span class="sxs-lookup"><span data-stu-id="40b34-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="40b34-209">如果瀏覽器設定和標記設定不一致，則頁面不會套用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="40b34-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="40b34-210">例如，如果中繼標籤設定為 [否]，而瀏覽器設定為啟用視覺化樣式，則視覺效果樣式不會套用至頁面。</span><span class="sxs-lookup"><span data-stu-id="40b34-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="40b34-211">但是，如果瀏覽器或中繼標籤設定為 [是]，而未指定其他專案，則會套用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="40b34-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="40b34-212">視覺化樣式可能會變更內容的版面配置。</span><span class="sxs-lookup"><span data-stu-id="40b34-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="40b34-213">此外，如果您在內部 HTML 控制項（例如按鈕的寬度）上設定某些屬性，您可能會發現按鈕上的標籤在某些視覺效果樣式下無法閱讀。</span><span class="sxs-lookup"><span data-stu-id="40b34-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="40b34-214">您必須使用視覺化樣式來徹底測試您的內容，以判斷套用視覺效果樣式對您的內容和配置是否有負面影響。</span><span class="sxs-lookup"><span data-stu-id="40b34-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="40b34-215">未套用視覺化樣式時</span><span class="sxs-lookup"><span data-stu-id="40b34-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="40b34-216">若要避免將視覺效果樣式套用至最上層視窗，請為視窗提供非 null 區域 (**SetWindowRgn**) 。</span><span class="sxs-lookup"><span data-stu-id="40b34-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="40b34-217">系統會假設具有非 Null 區域的視窗是未使用視覺化樣式的特製化視窗。</span><span class="sxs-lookup"><span data-stu-id="40b34-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="40b34-218">與非視覺效果樣式的最上層視窗相關聯的子視窗仍可能套用視覺化樣式，即使父視窗沒有。</span><span class="sxs-lookup"><span data-stu-id="40b34-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="40b34-219">如果您想要停用應用程式中所有視窗的視覺化樣式，請呼叫 [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) ，不要通過 STAP \_ 允許非工作區 \_ 旗標。</span><span class="sxs-lookup"><span data-stu-id="40b34-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="40b34-220">如果應用程式未呼叫 **SetThemeAppProperties**，則假設的旗標值為 STAP \_ 允許非工作 \_ \| STAP \_ 允許 \_ 控制項 \| STAP \_ 允許 \_ WEBCONTENT。</span><span class="sxs-lookup"><span data-stu-id="40b34-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="40b34-221">假設的值會使非工作區、控制項和 web 內容套用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="40b34-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="40b34-222">讓您的應用程式與舊版 Windows 相容</span><span class="sxs-lookup"><span data-stu-id="40b34-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="40b34-223">許多視覺化樣式架構的設計目的，是為了讓您在不支援變更控制面板的舊版 Windows 上繼續交付您的產品。</span><span class="sxs-lookup"><span data-stu-id="40b34-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="40b34-224">當您為一個以上的作業系統傳送應用程式時，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="40b34-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="40b34-225">在 Windows 8 之前的 Windows 版本中，當高對比開啟時，視覺化樣式會關閉。</span><span class="sxs-lookup"><span data-stu-id="40b34-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="40b34-226">為了支援高對比，支援視覺效果樣式的繼承應用程式必須提供個別的程式碼路徑，才能適當地以高對比繪製 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="40b34-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="40b34-227">在 Windows 8 中，高對比是視覺化樣式的一部分;不過，Windows 8 的應用程式 (其中一個應用程式資訊清單的 [相容性] 區段中包含 Windows 8 GUID) 仍然需要提供個別的程式碼路徑，以便在先前的 Windows 7 上正確呈現。</span><span class="sxs-lookup"><span data-stu-id="40b34-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="40b34-228">如果您使用 ComCtl32.dll 第6版中的功能（例如圖格視圖或連結控制項），就必須處理使用者電腦上無法使用這些控制項的情況。</span><span class="sxs-lookup"><span data-stu-id="40b34-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="40b34-229">ComCtl32.dll 第6版無法轉散發。</span><span class="sxs-lookup"><span data-stu-id="40b34-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="40b34-230">測試您的應用程式，以確定您未先檢查目前的版本，而不依賴 ComCtl32.dll 版本6的功能。</span><span class="sxs-lookup"><span data-stu-id="40b34-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="40b34-231">請勿連結至 UxTheme .lib。</span><span class="sxs-lookup"><span data-stu-id="40b34-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="40b34-232">當視覺效果樣式未如預期般運作時，為實例撰寫錯誤處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="40b34-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="40b34-233">在較舊版本中安裝應用程式的資訊清單不會影響控制項的呈現。</span><span class="sxs-lookup"><span data-stu-id="40b34-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b34-234">相關主題</span><span class="sxs-lookup"><span data-stu-id="40b34-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b34-235">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="40b34-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
