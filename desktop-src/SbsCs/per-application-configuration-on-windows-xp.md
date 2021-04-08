---
description: 在 Windows XP 中，每個應用程式設定會以個別應用程式為基礎覆寫預設設定和發行者設定。
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Windows XP 上的每個應用程式設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851779"
---
# <a name="per-application-configuration-on-windows-xp"></a><span data-ttu-id="750dd-103">Windows XP 上的每個應用程式設定</span><span class="sxs-lookup"><span data-stu-id="750dd-103">Per-application Configuration on Windows XP</span></span>

<span data-ttu-id="750dd-104">在 Windows XP 中，每個應用程式設定會以個別應用程式為基礎覆寫 [預設](default-configuration.md) 設定和 [發行者](publisher-configuration.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-104">On Windows XP, per-application configuration overrides both [default configuration](default-configuration.md) and [publisher configuration](publisher-configuration.md) on a per-application basis.</span></span> <span data-ttu-id="750dd-105">這會將特定應用程式的相依性從並存元件的某個版本重新導向至另一個指定版本的元件。</span><span class="sxs-lookup"><span data-stu-id="750dd-105">This redirects the dependence of a specific application from one version of a side-by-side assembly to another specified version of the assembly.</span></span>

> [!Note]  
> <span data-ttu-id="750dd-106">從 Windows Server 2003 開始，只有在 [應用程式佈建檔](application-configuration-files.md)在 **>publisherpolicy** 中指定 *apply = "No"* ，且應用程式相容性資料庫中有對應的專案時，每個應用程式設定才會覆寫每個應用程式的 [發行者](publisher-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-106">Starting with Windows Server 2003, per-application configuration overrides [publisher configuration](publisher-configuration.md) on a per-application basis only if the [application configuration file](application-configuration-files.md) specifies *apply="no"* in **publisherPolicy** and there is a corresponding entry present in the Application Compatibility database.</span></span> <span data-ttu-id="750dd-107">每個應用程式設定一律會覆寫 [預設](default-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-107">Per-application configuration always overrides the [default configuration](default-configuration.md).</span></span> <span data-ttu-id="750dd-108">如需詳細資訊，請參閱 [每個應用程式](per-application-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-108">For information see [per-application configuration](per-application-configuration.md).</span></span>

 

<span data-ttu-id="750dd-109">如果特定應用程式的正確作業需要的元件版本與通常指定為預設或發行者設定的版本不同，則每個應用程式的設定可能會變成必要。</span><span class="sxs-lookup"><span data-stu-id="750dd-109">A per-application configuration may become necessary if the correct operation of a particular application requires an assembly version that is different than the version normally specified as a default or publisher configuration.</span></span> <span data-ttu-id="750dd-110">例如，發行者的元件版本全域更新可能會修正元件，但會中斷這個特定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="750dd-110">For example, a global update of the assembly version by the publisher might fix the assembly but break this particular application.</span></span> <span data-ttu-id="750dd-111">在此情況下，每個應用程式的設定可能會用來讓應用程式繼續以先前的元件版本執行。</span><span class="sxs-lookup"><span data-stu-id="750dd-111">In this case, per-application configuration might be used to enable the application to continue to run with the previous assembly version.</span></span> <span data-ttu-id="750dd-112">另一個範例是包含元件更新的 service pack 安裝，可以使用「 [發行者](publisher-configuration.md) 設定」，將系統上所有應用程式和元件的相依性，從1.0.0.0 版重新導向至1.0.1.0 版。</span><span class="sxs-lookup"><span data-stu-id="750dd-112">Another example, a service pack installation containing an assembly update might use [publisher configuration](publisher-configuration.md) to redirect the dependencies of all applications and assemblies on the system from version 1.0.0.0 to 1.0.1.0.</span></span> <span data-ttu-id="750dd-113">如果有需要1.0.0.0 版才能正常運作的應用程式，可以使用每一應用程式的設定，將它重新導向至1.0.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="750dd-113">If there is an application that requires version 1.0.0.0 to work correctly, it can be redirected to version 1.0.0.0 by using per-application configuration.</span></span>

<span data-ttu-id="750dd-114">應用程式系統管理員可以藉由撰寫和安裝 [應用程式佈建檔](application-configuration-files.md)，來執行每個應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-114">Application administrators can implement a per-application configuration by authoring and installing [application configuration files](application-configuration-files.md).</span></span> <span data-ttu-id="750dd-115">這些會將特定應用程式重新導向至一個並存元件版本的相依性，以相依于其他版本。</span><span class="sxs-lookup"><span data-stu-id="750dd-115">These redirect a specific application from dependence on one version of a side-by-side assembly to dependence on another version.</span></span> <span data-ttu-id="750dd-116">[*應用程式佈建*](/windows/desktop/Msi/a-gly) 檔可以覆寫 [發行者設定檔](publisher-configuration-files.md) 和 [應用程式資訊清單](application-manifests.md) 和 [組件資訊清單](assembly-manifests.md)所指定的預設設定。</span><span class="sxs-lookup"><span data-stu-id="750dd-116">[*Application configuration*](/windows/desktop/Msi/a-gly) files can override [publisher configuration files](publisher-configuration-files.md) and the default configuration specified by [application manifests](application-manifests.md) and [assembly manifests](assembly-manifests.md).</span></span> <span data-ttu-id="750dd-117">應用程式佈建檔包含在呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 時載入器所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="750dd-117">The application configuration file includes information used by the loader when [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span>

<span data-ttu-id="750dd-118">若要將應用程式設定為覆寫應用程式資訊清單和發行者設定，開發人員必須撰寫應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="750dd-118">To configure an application to override both the application manifest and the publisher configuration, a developer must author an application configuration file.</span></span> <span data-ttu-id="750dd-119">然後，應用程式佈建檔會部署並安裝到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="750dd-119">The application configuration file is then deployed and installed into the same folder as the application's executable file.</span></span> <span data-ttu-id="750dd-120">如需檔案架構的清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="750dd-120">For a listing of the file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="750dd-121">請注意，如果您的應用程式使用每個應用程式設定，它將不會收到任何重要的安全性修正或錯誤修正。元件的發行者可能會以發行者設定檔的形式發行。</span><span class="sxs-lookup"><span data-stu-id="750dd-121">Note that if your application uses per-application configuration, it will not receive any important security fixes or bug fixes the publisher of the assembly might issue as publisher configuration files.</span></span> <span data-ttu-id="750dd-122">因此，使用每個應用程式設定的應用程式可能會維持不安全，或即使在具有這些修正程式的新元件套用至系統之後仍無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="750dd-122">An application that uses per-application configuration may therefore remain unsecure or continue to work incorrectly even after a new assembly with these fixes are applied to the system.</span></span> <span data-ttu-id="750dd-123">基於這個理由，應用程式開發人員絕對不應該使用每個應用程式的設定來傳送應用程式。</span><span class="sxs-lookup"><span data-stu-id="750dd-123">For this reason, application developers should never ship an application with a per-application configuration.</span></span> <span data-ttu-id="750dd-124">只有在發行者設定中斷應用程式時，公司系統管理員才能使用每個應用程式設定做為暫時的修正程式。</span><span class="sxs-lookup"><span data-stu-id="750dd-124">Per-application configuration should only be used by corporate administrators as a temporary fix when the application is broken by a publisher configuration.</span></span> <span data-ttu-id="750dd-125">在此情況下，永久的解決方案是元件的開發人員和應用程式開發人員必須共同合作，以確保具有發行者設定的元件能完全回溯相容。</span><span class="sxs-lookup"><span data-stu-id="750dd-125">In this case, the permanent solution is that the developers of the assembly and the developers of the application will need to work together to ensure that the assemblies with publisher configuration are fully backwards compatible.</span></span>

<span data-ttu-id="750dd-126">以下是應用程式佈建檔的範例。</span><span class="sxs-lookup"><span data-stu-id="750dd-126">The following is an example of an application configuration file.</span></span> <span data-ttu-id="750dd-127">如需詳細資訊，請參閱 [應用程式佈建檔](application-configuration-files.md)。</span><span class="sxs-lookup"><span data-stu-id="750dd-127">For more information, see [Application Configuration Files](application-configuration-files.md).</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
