---
description: 在 Windows Server 2003 上，WinHTTP 會實作為並存元件，而且必須連結到。 請注意，這並不適用于 Windows Vista 和更新版本。
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: 使用 WinHTTP 作為並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690432"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="dc2a7-104">使用 WinHTTP 作為並存元件</span><span class="sxs-lookup"><span data-stu-id="dc2a7-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="dc2a7-105">在 Windows Server 2003 上，WinHTTP 會實作為並存元件，而且必須連結到。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="dc2a7-106">請注意，這並不適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="dc2a7-107">並存元件</span><span class="sxs-lookup"><span data-stu-id="dc2a7-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="dc2a7-108">從 Microsoft Windows XP 開始，提供並存元件機制來控制執行時間連結，以避免動態連結程式庫 (DLL) 版本控制衝突。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="dc2a7-109">如需並存元件的詳細資訊，請參閱 [關於隔離應用程式和並存元件](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="dc2a7-110">若要使用此機制連結至 Windows Server 2003 上的 WinHTTP 5.1 版，應用程式必須併入指定 WinHTTP 作為相依元件的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="dc2a7-111">如需如何進行這項操作的詳細資訊，請參閱 [使用並存元件](/windows/desktop/SbsCs/using-side-by-side-assemblies) 。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="dc2a7-112">範例 WinHTTP 應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="dc2a7-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="dc2a7-113">以下範例資訊清單說明可用來連結至 WinHTTP 的應用程式資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="dc2a7-114">"" 的 "type" 以外的所有屬性都 <assembly> <assemblyIdentity> 必須適當地針對您的特定應用程式加以修改。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="dc2a7-115">" &lt; Description" 元素的內容也是相同的 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="dc2a7-116">此外，請確定 "" 的 "processorArchitecture" 屬性 <dependentAssembly> <assemblyIdentity> 符合 "" 的 "processorArchitecture" 屬性 <assembly> <assemblyIdentity> 。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="dc2a7-117">例如，在下列兩者都設定為 "x86"。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="dc2a7-118">所有不是您應用程式特有的值都應該採用如下所示的表單。</span><span class="sxs-lookup"><span data-stu-id="dc2a7-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
