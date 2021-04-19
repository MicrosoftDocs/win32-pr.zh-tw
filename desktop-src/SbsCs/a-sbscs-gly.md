---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: " (隔離的應用程式和並存元件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983479"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="64d34-103"> (隔離的應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="64d34-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="64d34-104">B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="64d34-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="64d34-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**啟用內容**</span><span class="sxs-lookup"><span data-stu-id="64d34-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-106">記憶體中的資料結構。</span><span class="sxs-lookup"><span data-stu-id="64d34-106">A data structure in memory.</span></span> <span data-ttu-id="64d34-107">此結構的每個區段都包含可並存感知 API 函式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="64d34-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="64d34-108">例如，一個區段可能會有 dll 載入器所使用的 DLL 重新導向資料，而另一個區段可能會有 COM 伺服器資料。</span><span class="sxs-lookup"><span data-stu-id="64d34-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="64d34-109">這項資料可用來將 DLL 的載入重新導向至特定版本、建立 COM 物件，或將視窗建立至與應用程式最相容的版本。</span><span class="sxs-lookup"><span data-stu-id="64d34-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="64d34-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**應用程式設定**</span><span class="sxs-lookup"><span data-stu-id="64d34-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-111">執行應用程式所需之並存元件的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="64d34-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="64d34-112">使用資訊清單部署應用程式時，會明確定義特定版本之共用並存元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="64d34-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="64d34-113">根據預設，資訊清單中指定的元件版本是在啟用時使用的版本。</span><span class="sxs-lookup"><span data-stu-id="64d34-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="64d34-114">全域應用程式設定會指定系統上所有應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="64d34-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="64d34-115">每個應用程式設定可以針對每個應用程式覆寫全域應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="64d34-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="64d34-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**應用程式設定資訊清單**</span><span class="sxs-lookup"><span data-stu-id="64d34-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-117">指定完整或部分隔離應用程式所使用之並存元件的檔案。</span><span class="sxs-lookup"><span data-stu-id="64d34-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="64d34-118">應用程式設定資訊清單檔案會安裝在與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="64d34-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="64d34-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**應用程式資訊清單**</span><span class="sxs-lookup"><span data-stu-id="64d34-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-120">描述隔離應用程式的檔案。</span><span class="sxs-lookup"><span data-stu-id="64d34-120">File that describes an isolated application.</span></span> <span data-ttu-id="64d34-121">它會指定執行應用程式所需的資訊，包括私用元件的相依性、共用元件的特定版本，以及私用元件的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="64d34-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="64d34-122">應用程式資訊清單檔的名稱是應用程式可執行檔的名稱，後接副檔名為 .manifest。</span><span class="sxs-lookup"><span data-stu-id="64d34-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="64d34-123">例如，針對 MySampleApp.exe，資訊清單檔會是 MySampleApp.exe 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="64d34-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="64d34-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**裝配**</span><span class="sxs-lookup"><span data-stu-id="64d34-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-125">命名、系結、版本控制、部署或設定程式設計程式碼區塊的基礎單位。</span><span class="sxs-lookup"><span data-stu-id="64d34-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="64d34-126">這些程式碼元件可能放在 Dll 或 COM 元件中。</span><span class="sxs-lookup"><span data-stu-id="64d34-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="64d34-127">具有一般功能的應用程式可能會執行稱為模組或程式碼元件的程式設計程式碼共用區塊。</span><span class="sxs-lookup"><span data-stu-id="64d34-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="64d34-128">元件安全共用的基礎結構稱為「並存元件共用」。</span><span class="sxs-lookup"><span data-stu-id="64d34-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="64d34-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**組件資訊清單**</span><span class="sxs-lookup"><span data-stu-id="64d34-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="64d34-130">並存元件的描述。</span><span class="sxs-lookup"><span data-stu-id="64d34-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="64d34-131">它會指定名稱、版本、檔案、元件的資源、元件專案的系結資料，以及其他並存元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="64d34-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="64d34-132">組件資訊清單檔可以有任何有效的檔案名，只要後面跟副檔名資訊清單即可。</span><span class="sxs-lookup"><span data-stu-id="64d34-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



