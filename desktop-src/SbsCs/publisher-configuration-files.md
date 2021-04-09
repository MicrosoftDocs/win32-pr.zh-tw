---
description: 發行者設定檔是一種 XML 檔案，可將應用程式和元件從使用一種並存元件版本，重新導向至相同元件的另一個版本。
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: 發行者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851772"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="1bd69-103">發行者設定檔</span><span class="sxs-lookup"><span data-stu-id="1bd69-103">Publisher Configuration Files</span></span>

<span data-ttu-id="1bd69-104">發行者設定檔是一種 XML 檔案，可將應用程式和元件從使用一種並存元件版本，重新導向至相同元件的另一個版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="1bd69-105">一般來說，元件的發行者會發出發行者設定檔案，以與 service pack 更新一起安裝，以針對每個元件發出相容的更新或安全性修正程式。</span><span class="sxs-lookup"><span data-stu-id="1bd69-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="1bd69-106">這稱為「 [發行者](publisher-configuration.md)設定」。</span><span class="sxs-lookup"><span data-stu-id="1bd69-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="1bd69-107">如需此類型設定的詳細資訊 [，請參閱](configuration.md) 發行者設定。</span><span class="sxs-lookup"><span data-stu-id="1bd69-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="1bd69-108">發行者設定檔具有下列元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="1bd69-109">如需 XML 架構的完整清單，請參閱 [發行者設定檔架構](publisher-configuration-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="1bd69-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="1bd69-110">項目</span><span class="sxs-lookup"><span data-stu-id="1bd69-110">Element</span></span>               | <span data-ttu-id="1bd69-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1bd69-111">Attributes</span></span>                | <span data-ttu-id="1bd69-112">必要</span><span class="sxs-lookup"><span data-stu-id="1bd69-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="1bd69-113">**裝配**</span><span class="sxs-lookup"><span data-stu-id="1bd69-113">**assembly**</span></span>          |                           | <span data-ttu-id="1bd69-114">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-114">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-115">**manifestVersion**</span></span>       | <span data-ttu-id="1bd69-116">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-116">Yes</span></span>      |
| <span data-ttu-id="1bd69-117">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="1bd69-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="1bd69-118">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-118">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-119">**type**</span><span class="sxs-lookup"><span data-stu-id="1bd69-119">**type**</span></span>                  | <span data-ttu-id="1bd69-120">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-120">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-121">**name**</span><span class="sxs-lookup"><span data-stu-id="1bd69-121">**name**</span></span>                  | <span data-ttu-id="1bd69-122">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-122">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-123">**language**</span><span class="sxs-lookup"><span data-stu-id="1bd69-123">**language**</span></span>              | <span data-ttu-id="1bd69-124">No</span><span class="sxs-lookup"><span data-stu-id="1bd69-124">No</span></span>       |
|                       | <span data-ttu-id="1bd69-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="1bd69-125">**processorArchitecture**</span></span> | <span data-ttu-id="1bd69-126">No</span><span class="sxs-lookup"><span data-stu-id="1bd69-126">No</span></span>       |
|                       | <span data-ttu-id="1bd69-127">**version**</span><span class="sxs-lookup"><span data-stu-id="1bd69-127">**version**</span></span>               | <span data-ttu-id="1bd69-128">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-128">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="1bd69-129">**publicKeyToken**</span></span>        | <span data-ttu-id="1bd69-130">No</span><span class="sxs-lookup"><span data-stu-id="1bd69-130">No</span></span>       |
| <span data-ttu-id="1bd69-131">**依賴**</span><span class="sxs-lookup"><span data-stu-id="1bd69-131">**dependency**</span></span>        |                           | <span data-ttu-id="1bd69-132">No</span><span class="sxs-lookup"><span data-stu-id="1bd69-132">No</span></span>       |
| <span data-ttu-id="1bd69-133">**y**</span><span class="sxs-lookup"><span data-stu-id="1bd69-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="1bd69-134">No</span><span class="sxs-lookup"><span data-stu-id="1bd69-134">No</span></span>       |
| <span data-ttu-id="1bd69-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="1bd69-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="1bd69-136">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-136">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-137">**oldVersion**</span></span>            | <span data-ttu-id="1bd69-138">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-138">Yes</span></span>      |
|                       | <span data-ttu-id="1bd69-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-139">**newVersion**</span></span>            | <span data-ttu-id="1bd69-140">Yes</span><span class="sxs-lookup"><span data-stu-id="1bd69-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="1bd69-141">檔案位置</span><span class="sxs-lookup"><span data-stu-id="1bd69-141">File Location</span></span>

<span data-ttu-id="1bd69-142">發行者設定檔必須安裝在 WinSxS 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="1bd69-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="1bd69-143">它們通常會安裝為個別的檔案，但發行者設定檔也可以包含為 DLL 中的資源。</span><span class="sxs-lookup"><span data-stu-id="1bd69-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="1bd69-144">發行者設定檔無法以資源的形式包含在 EXE 檔案中。</span><span class="sxs-lookup"><span data-stu-id="1bd69-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="1bd69-145">EXE 檔案可能會包含 [應用程式資訊清單](application-manifests.md) 做為資源。</span><span class="sxs-lookup"><span data-stu-id="1bd69-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="1bd69-146">檔名語法</span><span class="sxs-lookup"><span data-stu-id="1bd69-146">File Name Syntax</span></span>

<span data-ttu-id="1bd69-147">發行者設定檔案的檔案名具有表單 *原則*。*主要*。*次要*。*assemblyname* ，其中 *主要* 和 *次要* 會參考受影響之 [元件版本](assembly-versions.md) 的主要和次要部分。</span><span class="sxs-lookup"><span data-stu-id="1bd69-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="1bd69-148">*Assemblyname* 指的是元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bd69-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="1bd69-149">例如，Microsoft 的6.0 版發行者設定檔會有下列名稱： < 組解碼：</span><span class="sxs-lookup"><span data-stu-id="1bd69-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="1bd69-150">policy. Windows. 一般控制項</span><span class="sxs-lookup"><span data-stu-id="1bd69-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="1bd69-151">請勿使用原則設定檔來遞增元件的主要或次要版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="1bd69-152">例如，請勿將 version 6.0.0.0 重新導向至7.0.0.0 或6.1.0.0。</span><span class="sxs-lookup"><span data-stu-id="1bd69-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="1bd69-153">當應用程式參考元件版本（例如6.0.0.0）時，並存檢查是否有任何具有指定主要和次要版本的原則設定檔，例如6.0。</span><span class="sxs-lookup"><span data-stu-id="1bd69-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="1bd69-154">然後，應用程式會重新導向至另一個版本的元件，例如6.0.1.0。</span><span class="sxs-lookup"><span data-stu-id="1bd69-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="1bd69-155">如果發行者設定檔遞增元件的主要或次要版本，則元件的後續重新導向可能需要發出多個原則設定檔案。</span><span class="sxs-lookup"><span data-stu-id="1bd69-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="1bd69-156">元素</span><span class="sxs-lookup"><span data-stu-id="1bd69-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="1bd69-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**裝配**</span><span class="sxs-lookup"><span data-stu-id="1bd69-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="1bd69-158">容器元素。</span><span class="sxs-lookup"><span data-stu-id="1bd69-158">A container element.</span></span> <span data-ttu-id="1bd69-159">它的第一個子項目必須是 **assemblyIdentity**。</span><span class="sxs-lookup"><span data-stu-id="1bd69-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="1bd69-160">必要。</span><span class="sxs-lookup"><span data-stu-id="1bd69-160">Required.</span></span>

<span data-ttu-id="1bd69-161">Assembly 元素必須位於命名空間 **urn：架構-microsoft-com： .asm** 中。</span><span class="sxs-lookup"><span data-stu-id="1bd69-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="1bd69-162">元件的子專案也必須在這個命名空間中，繼承或標記。</span><span class="sxs-lookup"><span data-stu-id="1bd69-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="1bd69-163">**Assembly** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="1bd69-164">屬性</span><span class="sxs-lookup"><span data-stu-id="1bd69-164">Attribute</span></span>           | <span data-ttu-id="1bd69-165">描述</span><span class="sxs-lookup"><span data-stu-id="1bd69-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="1bd69-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-166">**manifestVersion**</span></span> | <span data-ttu-id="1bd69-167">**ManifestVersion** 屬性必須設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="1bd69-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1bd69-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="1bd69-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="1bd69-169">描述和唯一識別並存元件。</span><span class="sxs-lookup"><span data-stu-id="1bd69-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="1bd69-170">作為 **元件** 專案的第一個子項目， **assemblyIdentity** 會描述有一或多個元件相依性變更的並存元件。</span><span class="sxs-lookup"><span data-stu-id="1bd69-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="1bd69-171">發行者設定檔會重新導向所識別元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="1bd69-172">例如，下列 **assemblyIdentity** 表示發行者設定檔會影響 x86 6.0.0.0 元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="1bd69-173">**AssemblyIdentity** 是 **y** 專案的第一個子項目，描述並存元件相依性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="1bd69-174">發行者設定檔會重新設定此必要並存元件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="1bd69-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="1bd69-175">變更會在 **bindingRedirect** 中指定。</span><span class="sxs-lookup"><span data-stu-id="1bd69-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="1bd69-176">例如，下列 **assemblyIdentity** 會將 SampleAssembly 2.0.0.0 版的相依性變更為 SampleAssembly version 2.0.1.0 的相依性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="1bd69-177">**AssemblyIdentity** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="1bd69-178">它沒有子項目。</span><span class="sxs-lookup"><span data-stu-id="1bd69-178">It has no sub-elements.</span></span>



| <span data-ttu-id="1bd69-179">屬性</span><span class="sxs-lookup"><span data-stu-id="1bd69-179">Attribute</span></span>                 | <span data-ttu-id="1bd69-180">描述</span><span class="sxs-lookup"><span data-stu-id="1bd69-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd69-181">**type**</span><span class="sxs-lookup"><span data-stu-id="1bd69-181">**type**</span></span>                  | <span data-ttu-id="1bd69-182">指定元件類型。</span><span class="sxs-lookup"><span data-stu-id="1bd69-182">Specifies the assembly type.</span></span> <span data-ttu-id="1bd69-183">必要。</span><span class="sxs-lookup"><span data-stu-id="1bd69-183">Required.</span></span> <span data-ttu-id="1bd69-184">在受影響之元件的 **assemblyIdentity** 中， **type** 屬性的值必須設定為 win32 原則。</span><span class="sxs-lookup"><span data-stu-id="1bd69-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="1bd69-185">Win32 原則的值必須全部都是小寫字母。</span><span class="sxs-lookup"><span data-stu-id="1bd69-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="1bd69-186">在變更元件相依性的 **assemblyIdentity** 中， **類型** 屬性的值必須設定為 [win32]。</span><span class="sxs-lookup"><span data-stu-id="1bd69-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="1bd69-187">Win32 的值必須全部都是小寫字母。</span><span class="sxs-lookup"><span data-stu-id="1bd69-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="1bd69-188">**name**</span><span class="sxs-lookup"><span data-stu-id="1bd69-188">**name**</span></span>                  | <span data-ttu-id="1bd69-189">唯一命名元件。</span><span class="sxs-lookup"><span data-stu-id="1bd69-189">Uniquely names an assembly.</span></span> <span data-ttu-id="1bd69-190">必要。</span><span class="sxs-lookup"><span data-stu-id="1bd69-190">Required.</span></span> <span data-ttu-id="1bd69-191">在受影響之元件的 **assemblyIdentity** 中，名稱具有表單 *原則*。*主要*。*次要*。*assemblyname* ，其中 *主要* 和 *次要* 指的是 [元件版本](assembly-versions.md)的主要和次要部分。</span><span class="sxs-lookup"><span data-stu-id="1bd69-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="1bd69-192">在變更元件相依性的 **assemblyIdentity** 中，名稱的格式為 Organization.Division.Name。</span><span class="sxs-lookup"><span data-stu-id="1bd69-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="1bd69-193">例如，>mysampleapp。</span><span class="sxs-lookup"><span data-stu-id="1bd69-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="1bd69-194">**language**</span><span class="sxs-lookup"><span data-stu-id="1bd69-194">**language**</span></span>              | <span data-ttu-id="1bd69-195">識別元件的語言。</span><span class="sxs-lookup"><span data-stu-id="1bd69-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="1bd69-196">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-196">Optional.</span></span> <span data-ttu-id="1bd69-197">在受影響之元件的 **assemblyIdentity** 中，如果元件是語言特定的，請指定 DHTML 語言代碼。</span><span class="sxs-lookup"><span data-stu-id="1bd69-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="1bd69-198">如果元件適用于全球使用 (語言中性) ，請省略此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="1bd69-199">在變更元件相依性的 **assemblyIdentity** 中，如果元件是語言特定的，請指定 DHTML 語言代碼。</span><span class="sxs-lookup"><span data-stu-id="1bd69-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="1bd69-200">如果元件適用于全球使用 (中性語言) 將值設定為 " \* "。</span><span class="sxs-lookup"><span data-stu-id="1bd69-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="1bd69-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="1bd69-201">**processorArchitecture**</span></span> | <span data-ttu-id="1bd69-202">指定執行應用程式的處理器。</span><span class="sxs-lookup"><span data-stu-id="1bd69-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1bd69-203">**version**</span><span class="sxs-lookup"><span data-stu-id="1bd69-203">**version**</span></span>               | <span data-ttu-id="1bd69-204">指定組件版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-204">Specifies the assembly version.</span></span> <span data-ttu-id="1bd69-205">使用四部分版本語法： mmmm. oooo. pppp</span><span class="sxs-lookup"><span data-stu-id="1bd69-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="1bd69-206">只有在 DEF-coNtext **assemblyIdentity** 中才需要。</span><span class="sxs-lookup"><span data-stu-id="1bd69-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="1bd69-207">請勿在 REF 內容 **assemblyIdentity** 中指定 version 屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1bd69-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="1bd69-208">**publicKeyToken**</span></span>        | <span data-ttu-id="1bd69-209">16字元的十六進位字串，代表用來簽署元件之公開金鑰的 SHA-1 雜湊最後8個位元組。</span><span class="sxs-lookup"><span data-stu-id="1bd69-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="1bd69-210">用來簽署目錄的公開金鑰必須是2048位或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="1bd69-211">所有共用並存元件都需要 publicKeyToken。</span><span class="sxs-lookup"><span data-stu-id="1bd69-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="1bd69-212">用於發行者設定檔的 publicKeyToken 應與簽署的元件使用的金鑰相同。</span><span class="sxs-lookup"><span data-stu-id="1bd69-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="1bd69-213">發行者設定檔可以使用與元件搭配使用的相同工具來簽署，請參閱 [元件簽署範例](assembly-signing-example.md) 和 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。</span><span class="sxs-lookup"><span data-stu-id="1bd69-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="1bd69-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**依賴**</span><span class="sxs-lookup"><span data-stu-id="1bd69-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="1bd69-215">至少一個 **y** 的選擇性容器元素。</span><span class="sxs-lookup"><span data-stu-id="1bd69-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="1bd69-216">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1bd69-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**y**</span><span class="sxs-lookup"><span data-stu-id="1bd69-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="1bd69-218">每個 **y** 都必須正好在 **一個相依** 性內。</span><span class="sxs-lookup"><span data-stu-id="1bd69-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="1bd69-219">**Y** 沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="1bd69-220">**Y** 的第一個子項目必須是由發行者設定重新設定之並存元件的 **assemblyIdentity** 。</span><span class="sxs-lookup"><span data-stu-id="1bd69-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1bd69-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="1bd69-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="1bd69-222">**BindingRedirect** 元素包含元件系結的重新導向資訊。</span><span class="sxs-lookup"><span data-stu-id="1bd69-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="1bd69-223">此元素具有下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="1bd69-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="1bd69-224">屬性</span><span class="sxs-lookup"><span data-stu-id="1bd69-224">Attribute</span></span>      | <span data-ttu-id="1bd69-225">描述</span><span class="sxs-lookup"><span data-stu-id="1bd69-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd69-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-226">**oldVersion**</span></span> | <span data-ttu-id="1bd69-227">指定要覆寫和重新導向的元件版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="1bd69-228">使用四部分的版本語法 nnnnn。</span><span class="sxs-lookup"><span data-stu-id="1bd69-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="1bd69-229">以沒有空格的虛線來指定版本範圍。</span><span class="sxs-lookup"><span data-stu-id="1bd69-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="1bd69-230">例如，2.14.3.0 或 2.14.3.0 2.16.0.0。</span><span class="sxs-lookup"><span data-stu-id="1bd69-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="1bd69-231">必要。</span><span class="sxs-lookup"><span data-stu-id="1bd69-231">Required.</span></span> |
| <span data-ttu-id="1bd69-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="1bd69-232">**newVersion**</span></span> | <span data-ttu-id="1bd69-233">指定取代元件的版本。</span><span class="sxs-lookup"><span data-stu-id="1bd69-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="1bd69-234">使用四部分的版本語法 nnnnn。</span><span class="sxs-lookup"><span data-stu-id="1bd69-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bd69-235">備註</span><span class="sxs-lookup"><span data-stu-id="1bd69-235">Remarks</span></span>

<span data-ttu-id="1bd69-236">發行者設定檔不會指定檔案。</span><span class="sxs-lookup"><span data-stu-id="1bd69-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="1bd69-237">請注意，特定語言的原則檔案與發行者設定檔不同。</span><span class="sxs-lookup"><span data-stu-id="1bd69-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="1bd69-238">範例</span><span class="sxs-lookup"><span data-stu-id="1bd69-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




