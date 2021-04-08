---
description: 從 Windows XP 開始，您可以建立私用元件，並將它提供給特定的應用程式使用。
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: 使用私用元件來修正現有的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026160"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="9b962-103">使用私用元件來修正現有的應用程式</span><span class="sxs-lookup"><span data-stu-id="9b962-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="9b962-104">從 Windows XP 開始，您可以建立私用元件，並將它提供給特定的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="9b962-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="9b962-105">這項功能可以用來修正與更新不相容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b962-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="9b962-106">例如，在升級作業系統之後，應用程式會變成與最新版 MSVCRT.DLL 不相容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b962-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="9b962-107">在此情況下，您沒有取代系統版本的選項，因為 MSVCRT.DLL 是 Windows 受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="9b962-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="9b962-108">您可以建立 MSVCRT.LIB 的私用元件，並將其安裝在您的應用程式資料夾中，而不需要重寫應用程式來使用新版 MSVCRT.LIB。</span><span class="sxs-lookup"><span data-stu-id="9b962-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="9b962-109">請注意，並非每個共用元件都是私用並存元件的適當候選元件，而某些元件具有可安裝其元件之位置的授許可權制。</span><span class="sxs-lookup"><span data-stu-id="9b962-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="9b962-110">此元件必須符合並存元件的準則。</span><span class="sxs-lookup"><span data-stu-id="9b962-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="9b962-111">如果可提供適當的元件，請詢問元件的發行者。</span><span class="sxs-lookup"><span data-stu-id="9b962-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="9b962-112">私用元件的資訊清單和應用程式資訊清單都應該安裝在與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9b962-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="9b962-113">當應用程式執行時，它會查閱應用程式資訊清單，並載入應用程式私用的 MSVCRT.LIB 版本。</span><span class="sxs-lookup"><span data-stu-id="9b962-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="9b962-114">在此範例中，私用元件會同時包含 MSVCRT.DLL 和 MSVCIRT.DLL，如下列組件資訊清單所示：</span><span class="sxs-lookup"><span data-stu-id="9b962-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="9b962-115">以下是可能的應用程式資訊清單範例。</span><span class="sxs-lookup"><span data-stu-id="9b962-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



