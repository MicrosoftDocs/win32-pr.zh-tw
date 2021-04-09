---
description: 如果您希望應用程式的使用者或核心 DLL 能夠變更使用者介面的語言，您應該考慮將語言資源放在不同的附屬資源 Dll 中。
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: 使用具有多語系消費者介面的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690151"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="df6f5-103">使用具有多語系消費者介面的元件</span><span class="sxs-lookup"><span data-stu-id="df6f5-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="df6f5-104">如果您希望應用程式的使用者或核心 DLL 能夠變更使用者介面的語言，您應該考慮將語言資源放在不同的附屬資源 Dll 中。</span><span class="sxs-lookup"><span data-stu-id="df6f5-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="df6f5-105">如需使用附屬資源 Dll 的詳細資訊，請參閱 [ (MUI) 的多語言消費者介面 ](/windows/desktop/Intl/multilingual-user-interface)。</span><span class="sxs-lookup"><span data-stu-id="df6f5-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="df6f5-106">每個附屬 DLL 都包含不同語言的資源。</span><span class="sxs-lookup"><span data-stu-id="df6f5-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="df6f5-107">核心 DLL 可作為元件提供，而且每個附屬 Dll 都可以提供為個別的附屬元件。</span><span class="sxs-lookup"><span data-stu-id="df6f5-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="df6f5-108">在此情況下，每個附屬元件都應該有自己的自我描述組件資訊清單。</span><span class="sxs-lookup"><span data-stu-id="df6f5-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="df6f5-109">附屬元件的資訊清單不應描述其他元件的任何相依性。</span><span class="sxs-lookup"><span data-stu-id="df6f5-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="df6f5-110">其他元件上附屬元件的任何相依性，應該改為在核心元件的資訊清單中描述。</span><span class="sxs-lookup"><span data-stu-id="df6f5-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="df6f5-111">[多語系消費者介面 (MUI) ](/windows/desktop/Intl/multilingual-user-interface)版本的 Windows，可讓使用者根據其喜好設定指定使用者介面語言，前提是已在系統中新增必要的語言。</span><span class="sxs-lookup"><span data-stu-id="df6f5-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="df6f5-112">核心元件可使用多個 MUI 元件來支援多種語言。</span><span class="sxs-lookup"><span data-stu-id="df6f5-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="df6f5-113">在此情況下，每個 MUI 元件都應該有自己的資訊清單，而其他元件的任何相依性應該只在核心元件的資訊清單中描述。</span><span class="sxs-lookup"><span data-stu-id="df6f5-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="df6f5-114">例如，Proseware 可能是相依于 Proseware. SampleAssembly 元件的核心並存元件，而此元件則會發生。</span><span class="sxs-lookup"><span data-stu-id="df6f5-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="df6f5-115">如果 Proseware 使用 MUI 來支援多種語言，則可以為每種語言提供個別的 MUI 元件。</span><span class="sxs-lookup"><span data-stu-id="df6f5-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="df6f5-116">每個 MUI 元件都應該有自己的資訊清單，描述這個特定的附屬資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="df6f5-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="df6f5-117">MUI 元件資訊清單不應包含其他元件之相依性的任何參考。</span><span class="sxs-lookup"><span data-stu-id="df6f5-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="df6f5-118">描述核心元件 Proseware 的資訊清單應該描述 Proseware 的相依性。 Proseware. SampleAssembly 元件上的 Pop。</span><span class="sxs-lookup"><span data-stu-id="df6f5-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="df6f5-119">附屬元件之 **assemblyIdentity** 元素的屬性與基底元件資訊清單中的屬性類似。</span><span class="sxs-lookup"><span data-stu-id="df6f5-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="df6f5-120">**Name** 屬性應該與基底元件相同，並加入「資源」。</span><span class="sxs-lookup"><span data-stu-id="df6f5-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="df6f5-121">例如，如果基底元件中的名稱是 "Proseware. 拼字檢查"，則資源元件中的名稱會是 "Proseware. 拼字檢查. 資源"。</span><span class="sxs-lookup"><span data-stu-id="df6f5-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="df6f5-122">**Language** 屬性應該識別資源元件的語言。</span><span class="sxs-lookup"><span data-stu-id="df6f5-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="df6f5-123">**檔** 屬性應該包含屬於資源 dll 的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="df6f5-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="df6f5-124">下列是 Proseware 資訊清單的範例，例如拼字檢查。執行時間程式庫資源元件的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="df6f5-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="df6f5-125">基底元件描述資源元件的選擇性相依性。</span><span class="sxs-lookup"><span data-stu-id="df6f5-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="df6f5-126">在此範例中，如果使用者執行的 Windows 具有指定為德文的地區設定，則使用 Proseware 拼字檢查元件的應用程式會顯示德文中的文字。</span><span class="sxs-lookup"><span data-stu-id="df6f5-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
