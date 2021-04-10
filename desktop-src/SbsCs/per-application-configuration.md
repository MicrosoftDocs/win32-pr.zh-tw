---
description: 每個應用程式設定會將特定應用程式的相依性，從並存元件的某個版本重新導向至元件的另一個版本。
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: 每個應用程式設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194539"
---
# <a name="per-application-configuration"></a><span data-ttu-id="05400-103">每個應用程式設定</span><span class="sxs-lookup"><span data-stu-id="05400-103">Per-application Configuration</span></span>

<span data-ttu-id="05400-104">每個應用程式設定會將特定應用程式的相依性，從並存元件的某個版本重新導向至元件的另一個版本。</span><span class="sxs-lookup"><span data-stu-id="05400-104">Per-application configuration redirects the dependence of a particular application from one version of a side-by-side assembly to another version of the assembly.</span></span> <span data-ttu-id="05400-105">如果特定應用程式的正確作業需要的元件版本與通常指定為 [預設](default-configuration.md) 設定或 [發行者](publisher-configuration.md)設定的版本不同，則可能會需要個別應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="05400-105">A per-application configuration may become necessary if the correct operation of a particular application requires an assembly version that is different than the version normally specified as a [default configuration](default-configuration.md) or [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="05400-106">例如，發行者的元件版本全域更新可能會修正元件，但會中斷這個特定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="05400-106">For example, a global update of the assembly version by the publisher might fix the assembly but break this particular application.</span></span> <span data-ttu-id="05400-107">在此情況下，每個應用程式的設定可能會用來讓應用程式繼續以先前的元件版本執行。</span><span class="sxs-lookup"><span data-stu-id="05400-107">In this case, per-application configuration might be used to enable the application to continue to run with the previous assembly version.</span></span>

<span data-ttu-id="05400-108">從 Windows Server 2003 開始，每個應用程式設定一律會以個別應用程式為基礎覆寫 [預設](default-configuration.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="05400-108">Starting with Windows Server 2003, per-application configuration always overrides the [default configuration](default-configuration.md) on a per-application basis.</span></span> <span data-ttu-id="05400-109">只有當 [應用程式佈建檔](application-configuration-files.md)在 **>publisherpolicy** 中指定 *apply = "No"* ，且應用程式相容性資料庫中有對應的專案時，每個應用程式設定才會覆寫每個應用程式的 [發行者](publisher-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="05400-109">Per-application configuration overrides [publisher configuration](publisher-configuration.md) on a per-application basis only if the [application configuration file](application-configuration-files.md) specifies *apply="no"* in **publisherPolicy** and there is a corresponding entry present in the Application Compatibility database.</span></span>

> [!Note]  
> <span data-ttu-id="05400-110">在 Windows XP 中，每個應用程式設定會以個別應用程式為基礎覆寫 [預設](default-configuration.md) 設定和 [發行者](publisher-configuration.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="05400-110">On Windows XP, per-application configuration overrides both [default configuration](default-configuration.md) and [publisher configuration](publisher-configuration.md) on a per-application basis.</span></span> <span data-ttu-id="05400-111">如需詳細資訊，請參閱 [WINDOWS XP 上的每個應用程式](per-application-configuration-on-windows-xp.md)設定。</span><span class="sxs-lookup"><span data-stu-id="05400-111">For information, see [Per-application Configuration on Windows XP](per-application-configuration-on-windows-xp.md).</span></span>

 

<span data-ttu-id="05400-112">從 Windows Server 2003 開始，如果 [應用程式佈建檔](application-configuration-files.md)在 **>publisherpolicy** 中指定 *apply = "yes"* ，且已針對應用程式相容性資料庫中的應用程式設定 EnableAppConfig 旗標，則每個應用程式的設定將會覆寫 [發行者](publisher-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="05400-112">Starting with Windows Server 2003, a per-application configuration will override a [publisher configuration](publisher-configuration.md) if the [application configuration file](application-configuration-files.md) specifies *apply="yes"* in **publisherPolicy** and the EnableAppConfig flag is set for the application in the Application Compatibility database.</span></span> <span data-ttu-id="05400-113">使用每一應用程式設定覆寫發行者設定的這項功能，可讓應用程式在安全模式中執行。</span><span class="sxs-lookup"><span data-stu-id="05400-113">This capability to override a publisher configuration using a per-application configuration enables the application to be run in Safemode.</span></span> <span data-ttu-id="05400-114">如需有關應用程式相容性資料庫和安全模式的詳細資訊，請參閱 Windows 應用程式相容性工具組。</span><span class="sxs-lookup"><span data-stu-id="05400-114">For more information about the Application Compatibility database and Safemode, see the Windows Application Compatibility Toolkit.</span></span> <span data-ttu-id="05400-115">您可以從取得 Windows 應用程式相容性工具組 [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) 。</span><span class="sxs-lookup"><span data-stu-id="05400-115">You can obtain the Windows Application Compatibility Toolkit from [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/).</span></span>

> [!Note]  
> <span data-ttu-id="05400-116">如果您使用 [應用程式佈建檔](application-configuration-files.md)來傳送元件 ( .config 檔案) 在 **>publisherpolicy** 中指定 *apply = "no"* ，這會導致產生啟用內容失敗。</span><span class="sxs-lookup"><span data-stu-id="05400-116">If you ship components with an [application configuration file](application-configuration-files.md) (.config file) that specifies *apply="no"* in **publisherPolicy**, this will cause the generation of the activation context to fail.</span></span> <span data-ttu-id="05400-117">如果您在 **>publisherpolicy** 中以指定 *apply = "yes"* 的 .config 檔案傳送元件，則會忽略每個應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="05400-117">The per-application configuration will be ignored if you ship components with a .config file specifying *apply="yes"* in **publisherPolicy**.</span></span>

 

<span data-ttu-id="05400-118">應用程式系統管理員可以撰寫和安裝應用程式佈建檔，並更新應用程式相容性資料庫，以執行每個應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="05400-118">Application administrators can implement a per-application configuration by authoring and installing application configuration files and updating the application compatibility database.</span></span> <span data-ttu-id="05400-119">然後，應用程式佈建檔應該部署並安裝到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="05400-119">The application configuration file should then be deployed and installed into the same folder as the application's executable file.</span></span> <span data-ttu-id="05400-120">如需檔案架構的清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="05400-120">For a listing of the file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span> <span data-ttu-id="05400-121">應用程式相容性資料庫必須依照應用程式相容性工具組中的說明進行散發。</span><span class="sxs-lookup"><span data-stu-id="05400-121">The application compatibility database must be distributed as described in the Application Compatibility Toolkit.</span></span>

> [!Note]  
> <span data-ttu-id="05400-122">如果您的應用程式在安全模式中執行，它將不會收到任何重要的安全性修正或錯誤修正。元件的發行者可能會以發行者設定檔的形式發行。</span><span class="sxs-lookup"><span data-stu-id="05400-122">If your application runs in Safemode, it will not receive any important security fixes or bug fixes the publisher of the assembly might issue as publisher configuration files.</span></span> <span data-ttu-id="05400-123">因此，使用每個應用程式設定的應用程式可能會維持不安全，或即使在具有這些修正程式的新元件套用至系統之後仍無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05400-123">An application that uses per-application configuration may therefore remain unsecure or continue to work incorrectly even after a new assembly with these fixes are applied to the system.</span></span> <span data-ttu-id="05400-124">基於這個理由，應用程式開發人員絕對不應該使用每個應用程式的設定來傳送應用程式。</span><span class="sxs-lookup"><span data-stu-id="05400-124">For this reason, application developers should never ship an application with a per-application configuration.</span></span> <span data-ttu-id="05400-125">只有在發行者設定中斷應用程式時，公司系統管理員才能使用每個應用程式設定做為暫時的修正程式。</span><span class="sxs-lookup"><span data-stu-id="05400-125">Per-application configuration should only be used by corporate administrators as a temporary fix when the application is broken by a publisher configuration.</span></span> <span data-ttu-id="05400-126">在此情況下，永久的解決方案是元件的開發人員和應用程式開發人員必須共同合作，以確保具有發行者設定的元件能完全回溯相容。</span><span class="sxs-lookup"><span data-stu-id="05400-126">In this case, the permanent solution is that the developers of the assembly and the developers of the application will need to work together to ensure that the assemblies with publisher configuration are fully backwards compatible.</span></span>

 

<span data-ttu-id="05400-127">以下是應用程式佈建檔的範例。</span><span class="sxs-lookup"><span data-stu-id="05400-127">The following is an example of an application configuration file.</span></span> <span data-ttu-id="05400-128">如需詳細資訊，請參閱應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="05400-128">For more information, see Application Configuration Files.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

<span data-ttu-id="05400-129">應用程式系統管理員應該將必要的專案加入至應用程式相容性資料庫。</span><span class="sxs-lookup"><span data-stu-id="05400-129">The application administrator should add the required entries to the Application Compatibility database.</span></span> <span data-ttu-id="05400-130">從下載並安裝 Windows 應用程式相容性工具組 2.6 [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) 。</span><span class="sxs-lookup"><span data-stu-id="05400-130">Download and install the Windows Application Compatibility Toolkit 2.6 from [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/).</span></span> <span data-ttu-id="05400-131">使用此工具組中所述的相容性系統管理員，建立新的自訂或更新現有的資料庫。</span><span class="sxs-lookup"><span data-stu-id="05400-131">Create a new custom or update your existing database using the Compatibility Administrator as outlined in the toolkit.</span></span> <span data-ttu-id="05400-132">您想要為應用程式的相容性層級選擇的相容性修正程式是 EnableAppConfig。</span><span class="sxs-lookup"><span data-stu-id="05400-132">The Compatibility Fix you want to choose for the compatibility layer for your application is EnableAppConfig.</span></span> <span data-ttu-id="05400-133">您必須一律先測試應用程式，再安裝新的相容性資料庫。</span><span class="sxs-lookup"><span data-stu-id="05400-133">You must always test applications before installing a new compatibility database.</span></span>

 

 



