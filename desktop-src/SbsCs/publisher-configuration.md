---
description: 發行者設定檔會全域重新導向應用程式和元件相依于並存元件的一個版本，以使用相同元件的另一個版本。
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: 發行者設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194537"
---
# <a name="publisher-configuration"></a><span data-ttu-id="465f1-103">發行者設定</span><span class="sxs-lookup"><span data-stu-id="465f1-103">Publisher Configuration</span></span>

<span data-ttu-id="465f1-104">[發行者設定檔](publisher-configuration-files.md)會全域重新導向應用程式和元件相依于並存元件的一個版本，以使用相同元件的另一個版本。</span><span class="sxs-lookup"><span data-stu-id="465f1-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="465f1-105">這可讓應用程式和元件使用更新的元件，而不需要重建所有受影響的應用程式。</span><span class="sxs-lookup"><span data-stu-id="465f1-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="465f1-106">[發行者設定檔](publisher-configuration-files.md) 可能會在發行具有相容錯誤修正或安全性更新的新版本元件時，由元件發行者提供。</span><span class="sxs-lookup"><span data-stu-id="465f1-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="465f1-107">更新後的版本應該完全相容。</span><span class="sxs-lookup"><span data-stu-id="465f1-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="465f1-108">除非更新完全相容，否則不應該使用發行者設定檔來新增功能。</span><span class="sxs-lookup"><span data-stu-id="465f1-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="465f1-109">發行者設定檔絕不能用來遞增元件的主要或次要版本。</span><span class="sxs-lookup"><span data-stu-id="465f1-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="465f1-110">例如，請勿將元件版本6.0.0.0 重新導向至7.0.0.0 或6.1.0.0。</span><span class="sxs-lookup"><span data-stu-id="465f1-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="465f1-111">發行者設定檔案只應由元件的發行者發出。</span><span class="sxs-lookup"><span data-stu-id="465f1-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="465f1-112">元件開發人員應該簽署共用的並存元件和發行者設定檔案。</span><span class="sxs-lookup"><span data-stu-id="465f1-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="465f1-113">使用相同的金鑰來簽署元件和相關聯的發行者設定檔。</span><span class="sxs-lookup"><span data-stu-id="465f1-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="465f1-114">發行者設定檔應該使用與元件所用的相同工具來簽署，請參閱 [元件簽署範例](assembly-signing-example.md) 和 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。</span><span class="sxs-lookup"><span data-stu-id="465f1-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="465f1-115">一般來說，元件的新版本和相關聯的發行者設定檔將會安裝在 service pack 更新中。</span><span class="sxs-lookup"><span data-stu-id="465f1-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="465f1-116">因為安裝發行者設定檔案會全域重新導向系統上的元件，所以永遠不應該將應用程式提供給發行者設定檔案作為可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="465f1-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="465f1-117">如果要更新的元件是以可轉散發套件的形式提供，發行者應提供下列兩者。</span><span class="sxs-lookup"><span data-stu-id="465f1-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="465f1-118">Windows Installer 封裝 ( .msi 檔案) ，其中包含具有發行者設定的新元件版本。</span><span class="sxs-lookup"><span data-stu-id="465f1-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="465f1-119">這可能會安裝為 service pack 或 QFE，因為在此情況下，客戶已選擇全域更新系統。</span><span class="sxs-lookup"><span data-stu-id="465f1-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="465f1-120">應用程式永遠不會安裝此套件版本。</span><span class="sxs-lookup"><span data-stu-id="465f1-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="465f1-121">Windows Installer merge 模組 ( .msm 檔案) 只包含新版本的元件。</span><span class="sxs-lookup"><span data-stu-id="465f1-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="465f1-122">此版本可能包含在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="465f1-122">This version may be included with applications.</span></span>

<span data-ttu-id="465f1-123">需要最低版本元件的應用程式應該在最低版本上陳述其相依性，如果系統上的最小版本無法使用，則應用程式將無法啟動。</span><span class="sxs-lookup"><span data-stu-id="465f1-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="465f1-124">如果是可轉散發套件，則應該包含在應用程式安裝程式中。</span><span class="sxs-lookup"><span data-stu-id="465f1-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="465f1-125">例如，安裝下列 [發行者設定檔](publisher-configuration-files.md) 會將系結從 SampleAssembly 的2.0.0.0 版重新導向至版本2.0.1.0。</span><span class="sxs-lookup"><span data-stu-id="465f1-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="465f1-126">這會將名為1.1.0.0 的新原則新增至% systemDrive% \\ windows \\ winsxs 原則 \\ x86 \\ SampleAssembly \_ \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>。</span><span class="sxs-lookup"><span data-stu-id="465f1-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="465f1-127">針對相同元件安裝下列發行者設定檔，會將 SampleAssembly 的版本2.0.0.0 的系結重新導向至版本2.0.3.0。</span><span class="sxs-lookup"><span data-stu-id="465f1-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="465f1-128">這會將名為2.1.0.0 的另一個原則新增至% systemDrive% \\ windows \\ winsxs 原則 x86 SampleAssembly \\ \\ \_ \_ 75e377300ab7b886 \_ x-x-ww \_ < *hashvalue*>。</span><span class="sxs-lookup"><span data-stu-id="465f1-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



