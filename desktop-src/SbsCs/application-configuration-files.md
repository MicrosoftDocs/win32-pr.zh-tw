---
description: 應用程式佈建檔是用來控制元件系結的 XML 檔。
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: 應用程式組態檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112717"
---
# <a name="application-configuration-files"></a><span data-ttu-id="52b0a-103">應用程式組態檔</span><span class="sxs-lookup"><span data-stu-id="52b0a-103">Application Configuration Files</span></span>

<span data-ttu-id="52b0a-104">應用程式佈建檔是用來控制元件系結的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="52b0a-104">An application configuration file is an XML file used to control assembly binding.</span></span> <span data-ttu-id="52b0a-105">它可以將應用程式從使用一種並存元件的版本重新導向至相同元件的另一個版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-105">It can redirect an application from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="52b0a-106">這稱為 [每個應用程式](per-application-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="52b0a-106">This is called [per-application configuration](per-application-configuration.md).</span></span> <span data-ttu-id="52b0a-107">應用程式佈建檔只適用于特定的應用程式資訊清單和相依元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-107">An application configuration file applies only to a specific application manifest and dependent assemblies.</span></span> <span data-ttu-id="52b0a-108">使用內嵌 ISOLATIONAWARE \_ 資訊清單 \_ 資源識別碼資訊清單編譯的隔離元件 \_ 需要個別的應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="52b0a-108">Isolated components compiled with an embedded ISOLATIONAWARE\_MANIFEST\_RESOURCE\_ID manifest require a separate application configuration file.</span></span> <span data-ttu-id="52b0a-109">使用 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) 管理的資訊清單需要個別的應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="52b0a-109">Manifests managed with [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) require a separate application configuration file.</span></span>

<span data-ttu-id="52b0a-110">應用程式佈建檔所指定的重新導向可覆寫 [應用程式資訊清單](application-manifests.md) 和 [發行者設定檔](publisher-configuration-files.md)案所指定的元件版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-110">The redirection specified by an application configuration file can override the assembly versions specified by [application manifests](application-manifests.md) and [publisher configuration files](publisher-configuration-files.md).</span></span> <span data-ttu-id="52b0a-111">例如，如果發行者設定檔指定將元件的所有參考從1.0.0.0 版重新導向至1.1.0.0，則可以使用應用程式佈建檔重新導向特定應用程式以使用1.0.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="52b0a-111">For example, if a publisher configuration file specifies that all references to an assembly be redirected from version 1.0.0.0 to 1.1.0.0, an application configuration file can be used to redirect a particular application to use version 1.0.0.0.</span></span> <span data-ttu-id="52b0a-112">應用程式佈建檔僅適用于指定的應用程式資訊清單和相依元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-112">An application configuration file applies only to the specified application manifest and dependent assemblies.</span></span>

<span data-ttu-id="52b0a-113">如需 XML 架構的完整清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="52b0a-113">For a complete listing of the XML schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="52b0a-114">應用程式佈建檔具有下表所示的元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-114">Application configuration files have the elements and attributes shown in the following table.</span></span>



| <span data-ttu-id="52b0a-115">項目</span><span class="sxs-lookup"><span data-stu-id="52b0a-115">Element</span></span>               | <span data-ttu-id="52b0a-116">屬性</span><span class="sxs-lookup"><span data-stu-id="52b0a-116">Attributes</span></span>                | <span data-ttu-id="52b0a-117">必要</span><span class="sxs-lookup"><span data-stu-id="52b0a-117">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="52b0a-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="52b0a-118">**configuration**</span></span>     |                           | <span data-ttu-id="52b0a-119">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-119">Yes</span></span>      |
| <span data-ttu-id="52b0a-120">**windows**</span><span class="sxs-lookup"><span data-stu-id="52b0a-120">**windows**</span></span>           |                           | <span data-ttu-id="52b0a-121">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-121">Yes</span></span>      |
| <span data-ttu-id="52b0a-122">**>publisherpolicy**</span><span class="sxs-lookup"><span data-stu-id="52b0a-122">**publisherPolicy**</span></span>   |                           | <span data-ttu-id="52b0a-123">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-123">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-124">**應用**</span><span class="sxs-lookup"><span data-stu-id="52b0a-124">**apply**</span></span>                 | <span data-ttu-id="52b0a-125">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-125">Yes</span></span>      |
| <span data-ttu-id="52b0a-126">**執行階段**</span><span class="sxs-lookup"><span data-stu-id="52b0a-126">**runtime**</span></span>           |                           | <span data-ttu-id="52b0a-127">No</span><span class="sxs-lookup"><span data-stu-id="52b0a-127">No</span></span>       |
| <span data-ttu-id="52b0a-128">**assemblyBinding**</span><span class="sxs-lookup"><span data-stu-id="52b0a-128">**assemblyBinding**</span></span>   |                           | <span data-ttu-id="52b0a-129">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-129">Yes</span></span>      |
| <span data-ttu-id="52b0a-130">**探討**</span><span class="sxs-lookup"><span data-stu-id="52b0a-130">**probing**</span></span>           |                           | <span data-ttu-id="52b0a-131">No</span><span class="sxs-lookup"><span data-stu-id="52b0a-131">No</span></span>       |
|                       | <span data-ttu-id="52b0a-132">**privatePath**</span><span class="sxs-lookup"><span data-stu-id="52b0a-132">**privatePath**</span></span>           | <span data-ttu-id="52b0a-133">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-133">Yes</span></span>      |
| <span data-ttu-id="52b0a-134">**依賴**</span><span class="sxs-lookup"><span data-stu-id="52b0a-134">**dependency**</span></span>        |                           | <span data-ttu-id="52b0a-135">No</span><span class="sxs-lookup"><span data-stu-id="52b0a-135">No</span></span>       |
| <span data-ttu-id="52b0a-136">**y**</span><span class="sxs-lookup"><span data-stu-id="52b0a-136">**dependentAssembly**</span></span> |                           | <span data-ttu-id="52b0a-137">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-137">Yes</span></span>      |
| <span data-ttu-id="52b0a-138">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="52b0a-138">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="52b0a-139">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-139">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-140">**type**</span><span class="sxs-lookup"><span data-stu-id="52b0a-140">**type**</span></span>                  | <span data-ttu-id="52b0a-141">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-141">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-142">**name**</span><span class="sxs-lookup"><span data-stu-id="52b0a-142">**name**</span></span>                  | <span data-ttu-id="52b0a-143">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-143">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-144">**language**</span><span class="sxs-lookup"><span data-stu-id="52b0a-144">**language**</span></span>              | <span data-ttu-id="52b0a-145">No</span><span class="sxs-lookup"><span data-stu-id="52b0a-145">No</span></span>       |
|                       | <span data-ttu-id="52b0a-146">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="52b0a-146">**processorArchitecture**</span></span> | <span data-ttu-id="52b0a-147">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-147">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-148">**version**</span><span class="sxs-lookup"><span data-stu-id="52b0a-148">**version**</span></span>               | <span data-ttu-id="52b0a-149">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-149">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-150">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="52b0a-150">**publicKeyToken**</span></span>        | <span data-ttu-id="52b0a-151">No</span><span class="sxs-lookup"><span data-stu-id="52b0a-151">No</span></span>       |
| <span data-ttu-id="52b0a-152">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="52b0a-152">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="52b0a-153">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-153">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-154">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="52b0a-154">**oldVersion**</span></span>            | <span data-ttu-id="52b0a-155">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-155">Yes</span></span>      |
|                       | <span data-ttu-id="52b0a-156">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="52b0a-156">**newVersion**</span></span>            | <span data-ttu-id="52b0a-157">Yes</span><span class="sxs-lookup"><span data-stu-id="52b0a-157">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="52b0a-158">檔案位置</span><span class="sxs-lookup"><span data-stu-id="52b0a-158">File Location</span></span>

<span data-ttu-id="52b0a-159">應用程式佈建檔必須安裝在與應用程式 [應用程式資訊清單](application-manifests.md)相同的位置。</span><span class="sxs-lookup"><span data-stu-id="52b0a-159">Application configuration files must be installed in the same location as the application's [application manifest](application-manifests.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="52b0a-160">檔名語法</span><span class="sxs-lookup"><span data-stu-id="52b0a-160">File Name Syntax</span></span>

<span data-ttu-id="52b0a-161">應用程式佈建檔的名稱是應用程式可執行檔的名稱，後面接著 .config。</span><span class="sxs-lookup"><span data-stu-id="52b0a-161">The name of an application configuration file is the name of the application executable followed by .config.</span></span>

<span data-ttu-id="52b0a-162">例如，參考 Example.exe 或 Example.dll 的應用程式佈建檔會使用下列範例所示的檔案名語法。</span><span class="sxs-lookup"><span data-stu-id="52b0a-162">For example, an application configuration file that refers to Example.exe or Example.dll would use the file name syntax shown in the following example.</span></span> <span data-ttu-id="52b0a-163">如果將設定檔安裝為個別檔案，或資源識別碼為1，您可以省略 <*資源識別碼*> 的欄位。</span><span class="sxs-lookup"><span data-stu-id="52b0a-163">You can omit the field for <*resource ID*> if installing the configuration file as a separate file or if the resource ID is 1.</span></span>

<span data-ttu-id="52b0a-164">**example.exe。 <*資源識別碼\* C1.config*\*</span><span class="sxs-lookup"><span data-stu-id="52b0a-164">**example.exe.<*resource ID*>.config**</span></span>

<span data-ttu-id="52b0a-165">**example.dll。 <*資源識別碼\* C1.config*\*</span><span class="sxs-lookup"><span data-stu-id="52b0a-165">**example.dll.<*resource ID*>.config**</span></span>

## <a name="elements"></a><span data-ttu-id="52b0a-166">元素</span><span class="sxs-lookup"><span data-stu-id="52b0a-166">Elements</span></span>

<span data-ttu-id="52b0a-167">元素和屬性的名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="52b0a-167">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="52b0a-168">專案和屬性的值全都不區分大小寫，但 type 屬性的值除外。</span><span class="sxs-lookup"><span data-stu-id="52b0a-168">The values of elements and attributes are all case-insensitive, except for the value of the type attribute.</span></span>

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a><span data-ttu-id="52b0a-169">組態</span><span class="sxs-lookup"><span data-stu-id="52b0a-169">configuration</span></span>

<span data-ttu-id="52b0a-170">應用程式佈建檔的 **windows** 與 **運行** 時間專案的容器元素。</span><span class="sxs-lookup"><span data-stu-id="52b0a-170">A container element for the **windows** and **runtime** elements of an application configuration file.</span></span> <span data-ttu-id="52b0a-171">必要。</span><span class="sxs-lookup"><span data-stu-id="52b0a-171">Required.</span></span>

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a><span data-ttu-id="52b0a-172">windows</span><span class="sxs-lookup"><span data-stu-id="52b0a-172">windows</span></span>

<span data-ttu-id="52b0a-173">包含應用程式佈建檔的元件，該元件會套用至 Win32 元件的重新導向。</span><span class="sxs-lookup"><span data-stu-id="52b0a-173">Includes the parts of the application configuration file that apply to the redirection of Win32 assemblies.</span></span>

> [!Note]  
> <span data-ttu-id="52b0a-174">應用程式的作者不應包含具有 **windows** 子項目的設定檔，做為其應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="52b0a-174">The author of an application should not include a configuration file with a **windows** subelement as part of their application.</span></span> <span data-ttu-id="52b0a-175">如果設定檔的唯一目的是要啟用 **探查** 元素的 **privatePath** 功能，則可能會允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="52b0a-175">This may be permitted if the configuration file's only purpose is to enable the **privatePath** functionality of a **probing** element.</span></span> <span data-ttu-id="52b0a-176">Windows Server 2008 R2 和 Windows 7 之前的系統無法使用 **探查** 元素。</span><span class="sxs-lookup"><span data-stu-id="52b0a-176">The **probing** element is unavailable on systems earlier than Windows Server 2008 R2 and Windows 7.</span></span>

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a><span data-ttu-id="52b0a-177">>publisherpolicy</span><span class="sxs-lookup"><span data-stu-id="52b0a-177">publisherPolicy</span></span>

<span data-ttu-id="52b0a-178">指定是否要套用發行者原則。</span><span class="sxs-lookup"><span data-stu-id="52b0a-178">Specifies whether to apply publisher policy.</span></span>

<span data-ttu-id="52b0a-179">此元素具有下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-179">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="52b0a-180">屬性</span><span class="sxs-lookup"><span data-stu-id="52b0a-180">Attribute</span></span> | <span data-ttu-id="52b0a-181">描述</span><span class="sxs-lookup"><span data-stu-id="52b0a-181">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b0a-182">**應用**</span><span class="sxs-lookup"><span data-stu-id="52b0a-182">**apply**</span></span> | <span data-ttu-id="52b0a-183">值為 "yes" 時，會套用發行者原則。</span><span class="sxs-lookup"><span data-stu-id="52b0a-183">A value of "yes" applies the publisher policy.</span></span> <span data-ttu-id="52b0a-184">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="52b0a-184">This is the default setting.</span></span> <span data-ttu-id="52b0a-185">值為 "no" 時，不會套用發行者原則。</span><span class="sxs-lookup"><span data-stu-id="52b0a-185">The value "no" does not apply the publisher policy.</span></span> |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a><span data-ttu-id="52b0a-186">執行階段</span><span class="sxs-lookup"><span data-stu-id="52b0a-186">runtime</span></span>

<span data-ttu-id="52b0a-187">包含應用程式佈建檔的部分，適用于 .Net 元件的重新導向。</span><span class="sxs-lookup"><span data-stu-id="52b0a-187">Includes the parts of the application configuration file that apply to redirection of .Net assemblies.</span></span>

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a><span data-ttu-id="52b0a-188">assemblyBinding</span><span class="sxs-lookup"><span data-stu-id="52b0a-188">assemblyBinding</span></span>

<span data-ttu-id="52b0a-189">包含應用程式的重新導向資訊，以及受此應用程式佈建檔影響的元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-189">Includes the redirection information for the application and the assembly affected by this application configuration file.</span></span> <span data-ttu-id="52b0a-190">**AssemblyBinding** 的第一個子項目必須是可識別應用程式的 **assemblyIdentity** 。</span><span class="sxs-lookup"><span data-stu-id="52b0a-190">The first subelement of **assemblyBinding** must be an **assemblyIdentity** that identifies the application.</span></span>

<span data-ttu-id="52b0a-191">從 Windows Server 2008 R2 和 Windows 7 開始， **assemblyBinding** 元素可以包含 **探查** 子項目。</span><span class="sxs-lookup"><span data-stu-id="52b0a-191">Starting with Windows Server 2008 R2 and Windows 7 an **assemblyBinding** element can include a **probing** subelement.</span></span>

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a><span data-ttu-id="52b0a-192">探查</span><span class="sxs-lookup"><span data-stu-id="52b0a-192">probing</span></span>

<span data-ttu-id="52b0a-193">**AssemblyBinding** 專案的選擇性元素，可將元件的搜尋延伸至其他目錄。</span><span class="sxs-lookup"><span data-stu-id="52b0a-193">An optional subelement of an **assemblyBinding** element that extends the search for assemblies into additional directories.</span></span> <span data-ttu-id="52b0a-194">其他目錄不需要是元件目錄的子目錄。</span><span class="sxs-lookup"><span data-stu-id="52b0a-194">The additional directories are not required to be subdirectories of the directory of the assembly.</span></span>

> [!Note]  
> <span data-ttu-id="52b0a-195">此元素無法在 Windows Server 2008 R2 和 Windows 7 之前的系統上使用，而且只能在 **windows** 專案內使用。</span><span class="sxs-lookup"><span data-stu-id="52b0a-195">This element is unavailable on systems earlier than Windows Server 2008 R2 and Windows 7 and can only be used within a **windows** element.</span></span>

<span data-ttu-id="52b0a-196">此元素具有下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-196">This element has the attributes shown in the following table.</span></span>

| <span data-ttu-id="52b0a-197">屬性</span><span class="sxs-lookup"><span data-stu-id="52b0a-197">Attribute</span></span>       | <span data-ttu-id="52b0a-198">描述</span><span class="sxs-lookup"><span data-stu-id="52b0a-198">Description</span></span>                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b0a-199">**privatePath**</span><span class="sxs-lookup"><span data-stu-id="52b0a-199">**privatePath**</span></span> | <span data-ttu-id="52b0a-200">指定可能包含元件的應用程式基底目錄之子目錄的 [相對路徑](/windows/desktop/FileIO/naming-a-file) 。</span><span class="sxs-lookup"><span data-stu-id="52b0a-200">Specifies the [relative paths](/windows/desktop/FileIO/naming-a-file) of subdirectories of the application's base directory that might contain assemblies.</span></span> <span data-ttu-id="52b0a-201">最多可以指定九個子目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="52b0a-201">A maximum of nine subdirectory paths can be specified.</span></span> <span data-ttu-id="52b0a-202">使用分號分隔每個子目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="52b0a-202">Delimit each subdirectory path with a semicolon.</span></span> |

<span data-ttu-id="52b0a-203">您可以在路徑中使用雙點特殊規範，以表示目前的目錄的上層目錄。</span><span class="sxs-lookup"><span data-stu-id="52b0a-203">You can use the double-dots special specifier in a path to denote the parent directory of the current directory.</span></span> <span data-ttu-id="52b0a-204">您可以使用雙點來指定目前目錄上方的兩個層級。</span><span class="sxs-lookup"><span data-stu-id="52b0a-204">No more than two levels above the current directory can be specified using double-dots.</span></span> <span data-ttu-id="52b0a-205">請勿使用三個點。</span><span class="sxs-lookup"><span data-stu-id="52b0a-205">Do not use triple-dots.</span></span> <span data-ttu-id="52b0a-206">例如，使用下列 **探查** 元素的應用程式會檢查元件的其他目錄。</span><span class="sxs-lookup"><span data-stu-id="52b0a-206">For example, an application using the following **probing** element checks additional directories for an assembly.</span></span>

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="52b0a-207">相依性</span><span class="sxs-lookup"><span data-stu-id="52b0a-207">dependency</span></span>
<span data-ttu-id="52b0a-208">至少一個 **y** 的容器元素。</span><span class="sxs-lookup"><span data-stu-id="52b0a-208">A container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="52b0a-209">每個 **y** 都可以只在 **一個相依** 性內。</span><span class="sxs-lookup"><span data-stu-id="52b0a-209">Every **dependentAssembly** can be inside exactly one **dependency**.</span></span> <span data-ttu-id="52b0a-210">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-210">This element has no attributes.</span></span> <span data-ttu-id="52b0a-211">選擇性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-211">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="52b0a-212">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="52b0a-212">dependentAssembly</span></span>

<span data-ttu-id="52b0a-213">第一個子項目必須是 **assemblyIdentity** 專案，可識別應用程式佈建檔重新導向的並存元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-213">The first subelement must be an **assemblyIdentity** element that identifies the side-by-side assembly being redirected by the application configuration file.</span></span> <span data-ttu-id="52b0a-214">**Y** 沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-214">A **dependentAssembly** has no attributes.</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="52b0a-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="52b0a-215">assemblyIdentity</span></span>

<span data-ttu-id="52b0a-216">**AssemblyIdentity** 會以 **assemblyBinding** 專案的第一個子項目來描述和唯一識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="52b0a-216">As the first subelement of an **assemblyBinding** element, **assemblyIdentity** describes and uniquely identifies an application.</span></span> <span data-ttu-id="52b0a-217">應用程式佈建檔會將此應用程式的系結重新導向至並存元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-217">The application configuration file redirects the binding of this application to side-by-side assemblies.</span></span> <span data-ttu-id="52b0a-218">例如，下列 **assemblyIdentity** 表示應用程式佈建檔會影響應用程式 >mysampleapp 對並存元件的系結。</span><span class="sxs-lookup"><span data-stu-id="52b0a-218">For example, the following **assemblyIdentity** indicates that the application configuration file affects the binding of the application mysampleApp to side-by-side assemblies.</span></span> <span data-ttu-id="52b0a-219">重新導向的元件會在 **y** 中識別。</span><span class="sxs-lookup"><span data-stu-id="52b0a-219">The assemblies being redirected would be identified in a **dependentAssembly**.</span></span>

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

<span data-ttu-id="52b0a-220">**AssemblyIdentity** 會以 **y** 專案的第一個子項目，描述應用程式所相依的並存元件。</span><span class="sxs-lookup"><span data-stu-id="52b0a-220">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly on which the application depends.</span></span> <span data-ttu-id="52b0a-221">應用程式佈建檔會重新設定此必要元件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="52b0a-221">The application configuration file reconfigures the identity of this required assembly.</span></span> <span data-ttu-id="52b0a-222">例如，下列 **assemblyIdentity** 和 **BindingRedirect** 會將 SampleAssembly 的相依性從2.0.0.0 版重新配置到 version 2.1.0.0。</span><span class="sxs-lookup"><span data-stu-id="52b0a-222">For example, the following **assemblyIdentity** and **bindingRedirect** reconfigures a dependency on Microsoft.Windows.SampleAssembly from version 2.0.0.0 to version 2.1.0.0.</span></span>

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="52b0a-223">請注意， **y** 中包含的每個 **assemblyIdentity** 都必須完全符合元件本身的 [組件資訊清單](assembly-manifests.md)中的 **assemblyIdentity** 。</span><span class="sxs-lookup"><span data-stu-id="52b0a-223">Note that every **assemblyIdentity** included in a **dependentAssembly** must exactly match the **assemblyIdentity** in the assembly's own [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="52b0a-224">**AssemblyIdentity** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-224">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="52b0a-225">它沒有子項目。</span><span class="sxs-lookup"><span data-stu-id="52b0a-225">It has no subelements.</span></span>

| <span data-ttu-id="52b0a-226">屬性</span><span class="sxs-lookup"><span data-stu-id="52b0a-226">Attribute</span></span>                 | <span data-ttu-id="52b0a-227">描述</span><span class="sxs-lookup"><span data-stu-id="52b0a-227">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b0a-228">**type**</span><span class="sxs-lookup"><span data-stu-id="52b0a-228">**type**</span></span>                  | <span data-ttu-id="52b0a-229">值必須是 win32 (小寫) 。</span><span class="sxs-lookup"><span data-stu-id="52b0a-229">The value must be win32 (lower case).</span></span> <span data-ttu-id="52b0a-230">必要。</span><span class="sxs-lookup"><span data-stu-id="52b0a-230">Required.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="52b0a-231">**name**</span><span class="sxs-lookup"><span data-stu-id="52b0a-231">**name**</span></span>                  | <span data-ttu-id="52b0a-232">Name 屬性會識別受應用程式佈建檔或正在重新導向的元件所影響的應用程式。</span><span class="sxs-lookup"><span data-stu-id="52b0a-232">The name attribute identifies the application being affected by the application configuration file or the assembly being redirected.</span></span> <span data-ttu-id="52b0a-233">針對名稱，請使用下列格式： Organization.Division.Name。</span><span class="sxs-lookup"><span data-stu-id="52b0a-233">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="52b0a-234">必要。</span><span class="sxs-lookup"><span data-stu-id="52b0a-234">Required.</span></span> <span data-ttu-id="52b0a-235">例如： >mysampleapp 或 MysampleAsm 的內容。</span><span class="sxs-lookup"><span data-stu-id="52b0a-235">For example: Microsoft.Windows.MysampleApp or Microsoft.Windows.MysampleAsm.</span></span><br/>            |
| <span data-ttu-id="52b0a-236">**language**</span><span class="sxs-lookup"><span data-stu-id="52b0a-236">**language**</span></span>              | <span data-ttu-id="52b0a-237">識別語言。</span><span class="sxs-lookup"><span data-stu-id="52b0a-237">Identifies the language.</span></span> <span data-ttu-id="52b0a-238">選擇性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-238">Optional.</span></span> <span data-ttu-id="52b0a-239">對於參考元件的 **assemblyIdentity** ，如果元件是語言特定的，請指定 DHTML 語言代碼。</span><span class="sxs-lookup"><span data-stu-id="52b0a-239">For an **assemblyIdentity** referring to an assembly, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="52b0a-240">如果元件適用于全球使用 (中性語言) 將值設定為 " \* "。</span><span class="sxs-lookup"><span data-stu-id="52b0a-240">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                            |
| <span data-ttu-id="52b0a-241">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="52b0a-241">**processorArchitecture**</span></span> | <span data-ttu-id="52b0a-242">指定執行應用程式的處理器。</span><span class="sxs-lookup"><span data-stu-id="52b0a-242">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="52b0a-243">**version**</span><span class="sxs-lookup"><span data-stu-id="52b0a-243">**version**</span></span>               | <span data-ttu-id="52b0a-244">指定應用程式或元件的版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-244">Specifies the version of the application or assembly.</span></span> <span data-ttu-id="52b0a-245">使用四部分的版本語法： mmmm. oooo. pppp。</span><span class="sxs-lookup"><span data-stu-id="52b0a-245">Use four-part version syntax: mmmm.nnnn.oooo.pppp.</span></span> <span data-ttu-id="52b0a-246">必要。</span><span class="sxs-lookup"><span data-stu-id="52b0a-246">Required.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="52b0a-247">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="52b0a-247">**publicKeyToken**</span></span>        | <span data-ttu-id="52b0a-248">若為參考元件的 **assemblyIdentity** ，則為16字元的十六進位字串，代表簽署元件之公開金鑰的 sha-1 雜湊最後8個位元組。</span><span class="sxs-lookup"><span data-stu-id="52b0a-248">For an **assemblyIdentity** referring to an assembly, a 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="52b0a-249">用來簽署目錄的公開金鑰必須是2048位或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-249">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="52b0a-250">所有共用並存元件的必要項。</span><span class="sxs-lookup"><span data-stu-id="52b0a-250">Required for all shared side-by-side assemblies.</span></span> |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a><span data-ttu-id="52b0a-251">bindingRedirect</span><span class="sxs-lookup"><span data-stu-id="52b0a-251">bindingRedirect</span></span>

<span data-ttu-id="52b0a-252">**BindingRedirect** 元素包含元件系結的重新導向資訊。</span><span class="sxs-lookup"><span data-stu-id="52b0a-252">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span> <span data-ttu-id="52b0a-253">每個 **bindingRedirect** 都必須只包含在一個 **y** 中。</span><span class="sxs-lookup"><span data-stu-id="52b0a-253">Each **bindingRedirect** must be included in exactly one **dependentAssembly**.</span></span> <span data-ttu-id="52b0a-254">新版本和舊版本的四部分版本語法必須指定相同的主要和次要版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-254">The four-part version syntax of the new version and the old version must specify the same major and minor versions.</span></span>

<span data-ttu-id="52b0a-255">此元素具有下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="52b0a-255">This element has the attributes shown in the following table.</span></span>

| <span data-ttu-id="52b0a-256">屬性</span><span class="sxs-lookup"><span data-stu-id="52b0a-256">Attribute</span></span>      | <span data-ttu-id="52b0a-257">描述</span><span class="sxs-lookup"><span data-stu-id="52b0a-257">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b0a-258">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="52b0a-258">**oldVersion**</span></span> | <span data-ttu-id="52b0a-259">指定要覆寫和重新導向的元件版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-259">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="52b0a-260">使用四部分的版本語法 nnnnn。</span><span class="sxs-lookup"><span data-stu-id="52b0a-260">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="52b0a-261">以沒有空格的虛線來指定版本範圍。</span><span class="sxs-lookup"><span data-stu-id="52b0a-261">Specify a range of versions by a dash without spaces.</span></span> <span data-ttu-id="52b0a-262">例如，2.14.3.0 或 2.14.3.0 2.16.0.0。</span><span class="sxs-lookup"><span data-stu-id="52b0a-262">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="52b0a-263">必要。</span><span class="sxs-lookup"><span data-stu-id="52b0a-263">Required.</span></span> |
| <span data-ttu-id="52b0a-264">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="52b0a-264">**newVersion**</span></span> | <span data-ttu-id="52b0a-265">指定取代元件的版本。</span><span class="sxs-lookup"><span data-stu-id="52b0a-265">Specifies the replacement assembly version.</span></span> <span data-ttu-id="52b0a-266">使用四部分的版本語法 nnnnn。</span><span class="sxs-lookup"><span data-stu-id="52b0a-266">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |

## <a name="remarks"></a><span data-ttu-id="52b0a-267">備註</span><span class="sxs-lookup"><span data-stu-id="52b0a-267">Remarks</span></span>

<span data-ttu-id="52b0a-268">應用程式佈建檔不會指定檔案。</span><span class="sxs-lookup"><span data-stu-id="52b0a-268">Application configuration files do not specify files.</span></span>

## <a name="example"></a><span data-ttu-id="52b0a-269">範例</span><span class="sxs-lookup"><span data-stu-id="52b0a-269">Example</span></span>

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
