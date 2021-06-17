---
description: 所謂應用程式資訊清單，就是說明並識別共用和私用並存組件的 XML 檔，這些並存組件是應用程式要在執行時間加以繫結的組件。
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: 應用程式資訊清單
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230239"
---
# <a name="application-manifests"></a><span data-ttu-id="ff167-103">應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="ff167-103">Application Manifests</span></span>

<span data-ttu-id="ff167-104">所謂應用程式資訊清單，就是說明並識別共用和私用並存組件的 XML 檔，這些並存組件是應用程式要在執行時間加以繫結的組件。</span><span class="sxs-lookup"><span data-stu-id="ff167-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="ff167-105">並存組件的版本必須與用來測試應用程式的組件版本相同。</span><span class="sxs-lookup"><span data-stu-id="ff167-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="ff167-106">應用程式資訊清單可能也會說明應用程式私用檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ff167-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="ff167-107">如需 XML 架構的完整清單，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="ff167-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="ff167-108">應用程式資訊清單具有下列元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="ff167-109">項目</span><span class="sxs-lookup"><span data-stu-id="ff167-109">Element</span></span>                               | <span data-ttu-id="ff167-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-110">Attributes</span></span>                | <span data-ttu-id="ff167-111">必要</span><span class="sxs-lookup"><span data-stu-id="ff167-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="ff167-112">**裝配**</span><span class="sxs-lookup"><span data-stu-id="ff167-112">**assembly**</span></span>                          |                           | <span data-ttu-id="ff167-113">是</span><span class="sxs-lookup"><span data-stu-id="ff167-113">Yes</span></span>      |
|                                       | <span data-ttu-id="ff167-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="ff167-114">**manifestVersion**</span></span>       | <span data-ttu-id="ff167-115">是</span><span class="sxs-lookup"><span data-stu-id="ff167-115">Yes</span></span>      |
| <span data-ttu-id="ff167-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="ff167-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="ff167-117">否</span><span class="sxs-lookup"><span data-stu-id="ff167-117">No</span></span>       |
| <span data-ttu-id="ff167-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="ff167-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="ff167-119">是</span><span class="sxs-lookup"><span data-stu-id="ff167-119">Yes</span></span>      |
|                                       | <span data-ttu-id="ff167-120">**type**</span><span class="sxs-lookup"><span data-stu-id="ff167-120">**type**</span></span>                  | <span data-ttu-id="ff167-121">是</span><span class="sxs-lookup"><span data-stu-id="ff167-121">Yes</span></span>      |
|                                       | <span data-ttu-id="ff167-122">**name**</span><span class="sxs-lookup"><span data-stu-id="ff167-122">**name**</span></span>                  | <span data-ttu-id="ff167-123">是</span><span class="sxs-lookup"><span data-stu-id="ff167-123">Yes</span></span>      |
|                                       | <span data-ttu-id="ff167-124">**language**</span><span class="sxs-lookup"><span data-stu-id="ff167-124">**language**</span></span>              | <span data-ttu-id="ff167-125">否</span><span class="sxs-lookup"><span data-stu-id="ff167-125">No</span></span>       |
|                                       | <span data-ttu-id="ff167-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="ff167-126">**processorArchitecture**</span></span> | <span data-ttu-id="ff167-127">否</span><span class="sxs-lookup"><span data-stu-id="ff167-127">No</span></span>       |
|                                       | <span data-ttu-id="ff167-128">**version**</span><span class="sxs-lookup"><span data-stu-id="ff167-128">**version**</span></span>               | <span data-ttu-id="ff167-129">是</span><span class="sxs-lookup"><span data-stu-id="ff167-129">Yes</span></span>      |
|                                       | <span data-ttu-id="ff167-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="ff167-130">**publicKeyToken**</span></span>        | <span data-ttu-id="ff167-131">否</span><span class="sxs-lookup"><span data-stu-id="ff167-131">No</span></span>       |
| <span data-ttu-id="ff167-132">**相容性**</span><span class="sxs-lookup"><span data-stu-id="ff167-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="ff167-133">否</span><span class="sxs-lookup"><span data-stu-id="ff167-133">No</span></span>       |
| <span data-ttu-id="ff167-134">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="ff167-134">**application**</span></span>                       |                           | <span data-ttu-id="ff167-135">否</span><span class="sxs-lookup"><span data-stu-id="ff167-135">No</span></span>       |
| <span data-ttu-id="ff167-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="ff167-136">**supportedOS**</span></span>                       | <span data-ttu-id="ff167-137">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="ff167-137">**Id**</span></span>                    | <span data-ttu-id="ff167-138">否</span><span class="sxs-lookup"><span data-stu-id="ff167-138">No</span></span>       |
| <span data-ttu-id="ff167-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="ff167-139">**maxversiontested**</span></span>                  | <span data-ttu-id="ff167-140">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="ff167-140">**Id**</span></span>                    | <span data-ttu-id="ff167-141">否</span><span class="sxs-lookup"><span data-stu-id="ff167-141">No</span></span>       |
| <span data-ttu-id="ff167-142">**依賴**</span><span class="sxs-lookup"><span data-stu-id="ff167-142">**dependency**</span></span>                        |                           | <span data-ttu-id="ff167-143">否</span><span class="sxs-lookup"><span data-stu-id="ff167-143">No</span></span>       |
| <span data-ttu-id="ff167-144">**y**</span><span class="sxs-lookup"><span data-stu-id="ff167-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="ff167-145">否</span><span class="sxs-lookup"><span data-stu-id="ff167-145">No</span></span>       |
| <span data-ttu-id="ff167-146">**file**</span><span class="sxs-lookup"><span data-stu-id="ff167-146">**file**</span></span>                              |                           | <span data-ttu-id="ff167-147">否</span><span class="sxs-lookup"><span data-stu-id="ff167-147">No</span></span>       |
|                                       | <span data-ttu-id="ff167-148">**name**</span><span class="sxs-lookup"><span data-stu-id="ff167-148">**name**</span></span>                  | <span data-ttu-id="ff167-149">否</span><span class="sxs-lookup"><span data-stu-id="ff167-149">No</span></span>       |
|                                       | <span data-ttu-id="ff167-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="ff167-150">**hashalg**</span></span>               | <span data-ttu-id="ff167-151">否</span><span class="sxs-lookup"><span data-stu-id="ff167-151">No</span></span>       |
|                                       | <span data-ttu-id="ff167-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="ff167-152">**hash**</span></span>                  | <span data-ttu-id="ff167-153">否</span><span class="sxs-lookup"><span data-stu-id="ff167-153">No</span></span>       |
| <span data-ttu-id="ff167-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="ff167-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="ff167-155">否</span><span class="sxs-lookup"><span data-stu-id="ff167-155">No</span></span>       |
| <span data-ttu-id="ff167-156">**autoElevate**</span><span class="sxs-lookup"><span data-stu-id="ff167-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="ff167-157">否</span><span class="sxs-lookup"><span data-stu-id="ff167-157">No</span></span>       |
| <span data-ttu-id="ff167-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="ff167-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="ff167-159">否</span><span class="sxs-lookup"><span data-stu-id="ff167-159">No</span></span>       |
| <span data-ttu-id="ff167-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="ff167-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="ff167-161">否</span><span class="sxs-lookup"><span data-stu-id="ff167-161">No</span></span>       |
| <span data-ttu-id="ff167-162">**DPIAware**</span><span class="sxs-lookup"><span data-stu-id="ff167-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="ff167-163">否</span><span class="sxs-lookup"><span data-stu-id="ff167-163">No</span></span>       |
| <span data-ttu-id="ff167-164">**DPIAwareness**</span><span class="sxs-lookup"><span data-stu-id="ff167-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="ff167-165">否</span><span class="sxs-lookup"><span data-stu-id="ff167-165">No</span></span>       |
| <span data-ttu-id="ff167-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="ff167-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="ff167-167">否</span><span class="sxs-lookup"><span data-stu-id="ff167-167">No</span></span>       |
| <span data-ttu-id="ff167-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="ff167-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="ff167-169">否</span><span class="sxs-lookup"><span data-stu-id="ff167-169">No</span></span>       |
| <span data-ttu-id="ff167-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="ff167-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="ff167-171">否</span><span class="sxs-lookup"><span data-stu-id="ff167-171">No</span></span>       |
| <span data-ttu-id="ff167-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="ff167-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="ff167-173">否</span><span class="sxs-lookup"><span data-stu-id="ff167-173">No</span></span>       |
| <span data-ttu-id="ff167-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="ff167-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="ff167-175">否</span><span class="sxs-lookup"><span data-stu-id="ff167-175">No</span></span>       |
| <span data-ttu-id="ff167-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="ff167-176">**msix**</span></span>                              |                           | <span data-ttu-id="ff167-177">否</span><span class="sxs-lookup"><span data-stu-id="ff167-177">No</span></span>       |
| <span data-ttu-id="ff167-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="ff167-178">**heapType**</span></span>                          |                           | <span data-ttu-id="ff167-179">否</span><span class="sxs-lookup"><span data-stu-id="ff167-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="ff167-180">檔案位置</span><span class="sxs-lookup"><span data-stu-id="ff167-180">File Location</span></span>

<span data-ttu-id="ff167-181">應用程式資訊清單應該以資源的形式包含在應用程式的 EXE 檔案或 DLL 中。</span><span class="sxs-lookup"><span data-stu-id="ff167-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="ff167-182">如需詳細資訊，請參閱 [安裝並存元件](installing-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="ff167-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="ff167-183">檔名語法</span><span class="sxs-lookup"><span data-stu-id="ff167-183">File Name Syntax</span></span>

<span data-ttu-id="ff167-184">應用程式資訊清單檔的名稱是應用程式的可執行檔名稱，後面接著 .manifest。</span><span class="sxs-lookup"><span data-stu-id="ff167-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="ff167-185">例如，參考 example.exe 或 example.dll 的應用程式資訊清單會使用下列檔案名語法。</span><span class="sxs-lookup"><span data-stu-id="ff167-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="ff167-186">如果資源識別碼為1，您可以省略 <*資源識別碼*>] 欄位。</span><span class="sxs-lookup"><span data-stu-id="ff167-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="ff167-187">**example.exe。 <*資源識別碼*> 的資訊清單**</span><span class="sxs-lookup"><span data-stu-id="ff167-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="ff167-188">**example.dll。 <*資源識別碼*> 的資訊清單**</span><span class="sxs-lookup"><span data-stu-id="ff167-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="ff167-189">元素</span><span class="sxs-lookup"><span data-stu-id="ff167-189">Elements</span></span>

<span data-ttu-id="ff167-190">元素和屬性的名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ff167-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="ff167-191">元素和屬性的值不區分大小寫，但 type 屬性的值除外。</span><span class="sxs-lookup"><span data-stu-id="ff167-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="ff167-192">組件</span><span class="sxs-lookup"><span data-stu-id="ff167-192">assembly</span></span>

<span data-ttu-id="ff167-193">容器元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-193">A container element.</span></span> <span data-ttu-id="ff167-194">它的第一個子項目必須是 **noInherit** 或 **assemblyIdentity** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="ff167-195">必要。</span><span class="sxs-lookup"><span data-stu-id="ff167-195">Required.</span></span>

<span data-ttu-id="ff167-196">**Assembly** 元素必須在命名空間 "urn：架構-microsoft-com： asm" 中。</span><span class="sxs-lookup"><span data-stu-id="ff167-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="ff167-197">元件的子專案也必須在這個命名空間中，繼承或標記。</span><span class="sxs-lookup"><span data-stu-id="ff167-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="ff167-198">**Assembly** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="ff167-199">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-199">Attribute</span></span>           | <span data-ttu-id="ff167-200">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="ff167-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="ff167-201">**manifestVersion**</span></span> | <span data-ttu-id="ff167-202">**ManifestVersion** 屬性必須設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="ff167-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="ff167-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="ff167-203">noInherit</span></span>

<span data-ttu-id="ff167-204">在應用程式資訊清單中包含這個專案，以使用「無繼承」旗標來設定從資訊清單產生的 [啟用](activation-contexts.md) 內容。</span><span class="sxs-lookup"><span data-stu-id="ff167-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="ff167-205">當此旗標未在啟用內容中設定，且啟用內容為作用中時，會由相同進程、windows、視窗程式和 [非同步程序呼叫](/windows/desktop/Sync/asynchronous-procedure-calls)中的新執行緒繼承。</span><span class="sxs-lookup"><span data-stu-id="ff167-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="ff167-206">設定此旗標可防止新的物件繼承使用中的內容。</span><span class="sxs-lookup"><span data-stu-id="ff167-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="ff167-207">**NoInherit** 元素是選擇性的，通常會省略。</span><span class="sxs-lookup"><span data-stu-id="ff167-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="ff167-208">大部分的元件無法正確地使用「無繼承」啟用內容，因為元件必須明確設計來管理本身的啟用內容的傳播。</span><span class="sxs-lookup"><span data-stu-id="ff167-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="ff167-209">使用 **noInherit** 元素時，應用程式資訊清單所參考的任何相依元件都必須具有其 [組件資訊清單](assembly-manifests.md)中的 **noInherit** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="ff167-210">如果在資訊清單中使用 **noInherit** ，它必須是 **元件** 專案的第一個子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="ff167-211">**AssemblyIdentity** 元素應該緊接在 **noInherit** 元素之後。</span><span class="sxs-lookup"><span data-stu-id="ff167-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="ff167-212">如果未使用 **noInherit** ， **assemblyIdentity** 必須是 **assembly** 專案的第一個子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="ff167-213">**NoInherit** 元素沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="ff167-214">它不是 [組件資訊清單](assembly-manifests.md)中的有效元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="ff167-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="ff167-215">assemblyIdentity</span></span>

<span data-ttu-id="ff167-216">作為 **元件** 專案的第一個子項目， **assemblyIdentity** 會描述和唯一識別擁有此應用程式資訊清單的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff167-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="ff167-217">**AssemblyIdentity** 是 **y** 專案的第一個子項目，描述應用程式所需的並存元件。</span><span class="sxs-lookup"><span data-stu-id="ff167-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="ff167-218">請注意，應用程式資訊清單中所參考的每個元件都需要 **assemblyIdentity** ，以完全符合參考元件本身的組件資訊清單中的 **assemblyIdentity** 。</span><span class="sxs-lookup"><span data-stu-id="ff167-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="ff167-219">**AssemblyIdentity** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="ff167-220">它沒有子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-220">It has no subelements.</span></span>

| <span data-ttu-id="ff167-221">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-221">Attribute</span></span>                 | <span data-ttu-id="ff167-222">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff167-223">**type**</span><span class="sxs-lookup"><span data-stu-id="ff167-223">**type**</span></span>                  | <span data-ttu-id="ff167-224">指定應用程式或元件類型。</span><span class="sxs-lookup"><span data-stu-id="ff167-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="ff167-225">值必須是 Win32，而且全部都是小寫。</span><span class="sxs-lookup"><span data-stu-id="ff167-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="ff167-226">必要。</span><span class="sxs-lookup"><span data-stu-id="ff167-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ff167-227">**name**</span><span class="sxs-lookup"><span data-stu-id="ff167-227">**name**</span></span>                  | <span data-ttu-id="ff167-228">將應用程式或元件命名為唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff167-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="ff167-229">針對名稱，請使用下列格式： Organization.Division.Name。</span><span class="sxs-lookup"><span data-stu-id="ff167-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="ff167-230">例如，>mysampleapp。</span><span class="sxs-lookup"><span data-stu-id="ff167-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="ff167-231">必要。</span><span class="sxs-lookup"><span data-stu-id="ff167-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ff167-232">**language**</span><span class="sxs-lookup"><span data-stu-id="ff167-232">**language**</span></span>              | <span data-ttu-id="ff167-233">識別應用程式或元件的語言。</span><span class="sxs-lookup"><span data-stu-id="ff167-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="ff167-234">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-234">Optional.</span></span> <span data-ttu-id="ff167-235">如果應用程式或元件是特定語言，請指定 DHTML 語言代碼。</span><span class="sxs-lookup"><span data-stu-id="ff167-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="ff167-236">在適用于全球用途 (語言的應用程式 **assemblyIdentity** 中) 省略 language 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="ff167-237">在適用于全球用途 (語言的元件 **assemblyIdentity** 中) 將 language 的值設定為 " \* "。</span><span class="sxs-lookup"><span data-stu-id="ff167-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="ff167-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="ff167-238">**processorArchitecture**</span></span> | <span data-ttu-id="ff167-239">指定處理器。</span><span class="sxs-lookup"><span data-stu-id="ff167-239">Specifies the processor.</span></span> <span data-ttu-id="ff167-240">有效值包括 `x86`、`amd64`、`arm` 和 `arm64`。</span><span class="sxs-lookup"><span data-stu-id="ff167-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="ff167-241">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ff167-242">**version**</span><span class="sxs-lookup"><span data-stu-id="ff167-242">**version**</span></span>               | <span data-ttu-id="ff167-243">指定應用程式或元件版本。</span><span class="sxs-lookup"><span data-stu-id="ff167-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="ff167-244">使用四部分版本格式：好吃. ooooo. ppppp。</span><span class="sxs-lookup"><span data-stu-id="ff167-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="ff167-245">以句號分隔的每個部分都可以是0-65535 （含）。</span><span class="sxs-lookup"><span data-stu-id="ff167-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="ff167-246">如需詳細資訊，請參閱 [元件版本](assembly-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="ff167-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="ff167-247">必要。</span><span class="sxs-lookup"><span data-stu-id="ff167-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="ff167-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="ff167-248">**publicKeyToken**</span></span>        | <span data-ttu-id="ff167-249">16字元的十六進位字串，表示用來簽署應用程式或元件之公開金鑰的 SHA-1 雜湊最後8個位元組。</span><span class="sxs-lookup"><span data-stu-id="ff167-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="ff167-250">用來簽署目錄的公開金鑰必須是2048位或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="ff167-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="ff167-251">所有共用並存元件的必要項。</span><span class="sxs-lookup"><span data-stu-id="ff167-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="ff167-252">相容性</span><span class="sxs-lookup"><span data-stu-id="ff167-252">compatibility</span></span>

<span data-ttu-id="ff167-253">包含至少一個 **應用程式**。</span><span class="sxs-lookup"><span data-stu-id="ff167-253">Contains at least one **application**.</span></span> <span data-ttu-id="ff167-254">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-254">It has no attributes.</span></span> <span data-ttu-id="ff167-255">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-255">Optional.</span></span> <span data-ttu-id="ff167-256">沒有相容性元素的應用程式資訊清單預設為 windows 7 上的 Windows Vista 相容性。</span><span class="sxs-lookup"><span data-stu-id="ff167-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="ff167-257">應用程式</span><span class="sxs-lookup"><span data-stu-id="ff167-257">application</span></span>

<span data-ttu-id="ff167-258">包含至少一個 **supportedOS** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="ff167-259">從 Windows 10 版本1903開始，它也可以包含一個選擇性的 **maxversiontested** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="ff167-260">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-260">It has no attributes.</span></span> <span data-ttu-id="ff167-261">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="ff167-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="ff167-262">supportedOS</span></span>

<span data-ttu-id="ff167-263">**SupportedOS** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="ff167-264">它沒有子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-264">It has no subelements.</span></span>

| <span data-ttu-id="ff167-265">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-265">Attribute</span></span> | <span data-ttu-id="ff167-266">說明</span><span class="sxs-lookup"><span data-stu-id="ff167-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="ff167-267">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="ff167-267">**Id**</span></span>    | <span data-ttu-id="ff167-268">將識別碼屬性設定為 **{e2011457-1546-43c5-a5fe-008deee3d3f0}** ，以使用 Vista 功能來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff167-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="ff167-269">這可以讓針對 Windows Vista 設計的應用程式在較新的作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="ff167-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="ff167-270">將識別碼屬性設定為 **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** ，以使用 Windows 7 功能來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff167-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="ff167-271">支援 Windows Vista、Windows 7 和 Windows 8 功能的應用程式不需要個別的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ff167-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="ff167-272">在此情況下，請新增所有 Windows 作業系統的 Guid。</span><span class="sxs-lookup"><span data-stu-id="ff167-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="ff167-273">如需 Windows 中 **識別碼** 屬性行為的詳細資訊，請參閱 [Windows 8 和 Windows Server 2012 相容性操作手冊](https://www.microsoft.com/download/details.aspx?id=27416)。</span><span class="sxs-lookup"><span data-stu-id="ff167-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="ff167-274">下列 Guid 對應于指出的作業系統：</span><span class="sxs-lookup"><span data-stu-id="ff167-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="ff167-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10、windows server 2016 和 windows server 2019</span><span class="sxs-lookup"><span data-stu-id="ff167-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="ff167-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 和 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ff167-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="ff167-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 和 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff167-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="ff167-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> windows 7 和 windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff167-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="ff167-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> windows Vista 和 windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff167-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="ff167-280">您可以在 Windows 7 或 Windows 8. x 上進行測試，方法是執行資源監視器 (resmon) ，前往 [CPU] 索引標籤，以滑鼠右鍵按一下資料行標籤，選取 [選取資料行]，然後核取 [作業系統內容]。</span><span class="sxs-lookup"><span data-stu-id="ff167-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="ff167-281">在 Windows 8. x 上，您也可以在 [工作管理員 (taskmgr) 中找到此資料行。</span><span class="sxs-lookup"><span data-stu-id="ff167-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="ff167-282">資料行的內容會顯示找到的最大值或 "Windows Vista" 作為預設值。</span><span class="sxs-lookup"><span data-stu-id="ff167-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="ff167-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="ff167-283">maxversiontested</span></span>

<span data-ttu-id="ff167-284">**Maxversiontested** 元素會指定從應用程式所支援的最低 OS 版本開始，開始測試應用程式的 Windows 版本，最高可達最高版本。</span><span class="sxs-lookup"><span data-stu-id="ff167-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="ff167-285">您可以在 [這裡](https://developer.microsoft.com/windows/downloads/sdk-archive/)找到完整的版本集合。</span><span class="sxs-lookup"><span data-stu-id="ff167-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="ff167-286">這是為了讓使用 [XAML 孤島](/windows/apps/desktop/modernize/xaml-islands) 且未部署在 MSIX 套件中的桌面應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="ff167-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="ff167-287">在 Windows 10、1903版和更新版本中支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="ff167-288">**Maxversiontested** 元素具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="ff167-289">它沒有子項目。</span><span class="sxs-lookup"><span data-stu-id="ff167-289">It has no subelements.</span></span>

| <span data-ttu-id="ff167-290">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-290">Attribute</span></span> | <span data-ttu-id="ff167-291">說明</span><span class="sxs-lookup"><span data-stu-id="ff167-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="ff167-292">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="ff167-292">**Id**</span></span>    | <span data-ttu-id="ff167-293">將識別碼屬性設定為4部分版本字串，以指定測試應用程式所針對的 Windows 最大版本。</span><span class="sxs-lookup"><span data-stu-id="ff167-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="ff167-294">例如，"10.0.18226.0"。</span><span class="sxs-lookup"><span data-stu-id="ff167-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="ff167-295">相依性</span><span class="sxs-lookup"><span data-stu-id="ff167-295">dependency</span></span>

<span data-ttu-id="ff167-296">包含至少一個 **y**。</span><span class="sxs-lookup"><span data-stu-id="ff167-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="ff167-297">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-297">It has no attributes.</span></span> <span data-ttu-id="ff167-298">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="ff167-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="ff167-299">dependentAssembly</span></span>

<span data-ttu-id="ff167-300">**Y** 的第一個子項目必須是描述應用程式所需並存元件的 **assemblyIdentity** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="ff167-301">每個 **y** 都必須正好在 **一個相依** 性內。</span><span class="sxs-lookup"><span data-stu-id="ff167-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="ff167-302">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="ff167-303">file</span><span class="sxs-lookup"><span data-stu-id="ff167-303">file</span></span>

<span data-ttu-id="ff167-304">指定應用程式私用的檔案。</span><span class="sxs-lookup"><span data-stu-id="ff167-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="ff167-305">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff167-305">Optional.</span></span>

<span data-ttu-id="ff167-306">**File** 元素具有下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="ff167-307">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-307">Attribute</span></span>   | <span data-ttu-id="ff167-308">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff167-309">**name**</span><span class="sxs-lookup"><span data-stu-id="ff167-309">**name**</span></span>    | <span data-ttu-id="ff167-310">檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff167-310">Name of the file.</span></span> <span data-ttu-id="ff167-311">例如，Comctl32.dll。</span><span class="sxs-lookup"><span data-stu-id="ff167-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="ff167-312">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="ff167-312">**hashalg**</span></span> | <span data-ttu-id="ff167-313">用來建立檔案雜湊的演算法。</span><span class="sxs-lookup"><span data-stu-id="ff167-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="ff167-314">此值應為 SHA1。</span><span class="sxs-lookup"><span data-stu-id="ff167-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="ff167-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="ff167-315">**hash**</span></span>    | <span data-ttu-id="ff167-316">名稱所參考之檔案的雜湊。</span><span class="sxs-lookup"><span data-stu-id="ff167-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="ff167-317">長度的十六進位字串，取決於雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ff167-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="ff167-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="ff167-318">activeCodePage</span></span>

<span data-ttu-id="ff167-319">強制處理常式使用 UTF-8 作為程式字碼頁。</span><span class="sxs-lookup"><span data-stu-id="ff167-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="ff167-320">**activeCodePage** 已新增到 Windows 1903 版 (2019) 更新。</span><span class="sxs-lookup"><span data-stu-id="ff167-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="ff167-321">您可以宣告此屬性並在舊版 Windows 組建上執行，但是您必須如往常般處理舊版字碼頁偵測和轉換。</span><span class="sxs-lookup"><span data-stu-id="ff167-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="ff167-322">如需詳細資訊，請參閱 [使用 utf-8 字碼頁](/windows/uwp/design/globalizing/use-utf8-code-page) 。</span><span class="sxs-lookup"><span data-stu-id="ff167-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="ff167-323">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-323">This element has no attributes.</span></span> <span data-ttu-id="ff167-324">**Utf-8** 只是 **activeCodePage** 元素的有效值。</span><span class="sxs-lookup"><span data-stu-id="ff167-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="ff167-325">autoElevate</span><span class="sxs-lookup"><span data-stu-id="ff167-325">autoElevate</span></span>

<span data-ttu-id="ff167-326">指定是否啟用自動提升許可權。</span><span class="sxs-lookup"><span data-stu-id="ff167-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="ff167-327">**TRUE** 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="ff167-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="ff167-328">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="ff167-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="ff167-329">disableTheming</span></span>

<span data-ttu-id="ff167-330">指定是否要為 UI 元素提供主題停用。</span><span class="sxs-lookup"><span data-stu-id="ff167-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="ff167-331">**TRUE** 表示已停用。</span><span class="sxs-lookup"><span data-stu-id="ff167-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="ff167-332">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="ff167-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="ff167-333">disableWindowFiltering</span></span>

<span data-ttu-id="ff167-334">指定是否要停用視窗篩選。</span><span class="sxs-lookup"><span data-stu-id="ff167-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="ff167-335">**TRUE** 會停用視窗篩選，讓您可以從桌面列舉沉浸式視窗。</span><span class="sxs-lookup"><span data-stu-id="ff167-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="ff167-336">**disableWindowFiltering** 已加入 Windows 8 且沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="ff167-337">DPIAware</span><span class="sxs-lookup"><span data-stu-id="ff167-337">dpiAware</span></span>

<span data-ttu-id="ff167-338">指定目前的進程是否為每英寸的點 (DPI) 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="ff167-339">**Windows 10，版本1607：** 如果 **DPIAwareness** 元素存在，則會忽略 **DPIAware** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="ff167-340">如果您想要為 Windows 10 的版本1607指定不同的行為，您可以在資訊清單中包含這兩個元素，而不是舊版作業系統。</span><span class="sxs-lookup"><span data-stu-id="ff167-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="ff167-341">下表描述根據 **DPIAware** 專案是否存在，以及它所包含的文字所產生的行為。</span><span class="sxs-lookup"><span data-stu-id="ff167-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="ff167-342">元素內的文字不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ff167-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="ff167-343">**DpiAware** 元素的狀態</span><span class="sxs-lookup"><span data-stu-id="ff167-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="ff167-344">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="ff167-345">Absent</span><span class="sxs-lookup"><span data-stu-id="ff167-345">Absent</span></span>                            | <span data-ttu-id="ff167-346">目前的進程預設為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="ff167-347">您可以藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。</span><span class="sxs-lookup"><span data-stu-id="ff167-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="ff167-348">包含 "true"</span><span class="sxs-lookup"><span data-stu-id="ff167-348">Contains "true"</span></span>                   | <span data-ttu-id="ff167-349">目前的進程是系統 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ff167-350">包含 "false"</span><span class="sxs-lookup"><span data-stu-id="ff167-350">Contains "false"</span></span>                  | <span data-ttu-id="ff167-351">**Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。</span><span class="sxs-lookup"><span data-stu-id="ff167-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="ff167-352">**Windows 8.1 和 Windows 10：** 目前的進程不感知 DPI，而且您無法藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，以程式設計方式變更此設定。</span><span class="sxs-lookup"><span data-stu-id="ff167-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="ff167-353">包含 "true/pm"</span><span class="sxs-lookup"><span data-stu-id="ff167-353">Contains "true/pm"</span></span>                | <span data-ttu-id="ff167-354">**Windows Vista、windows 7 和 Windows 8：** 目前的進程是系統 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="ff167-355">**Windows 8.1 和 Windows 10：** 目前的進程是個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="ff167-356">包含「每個監視器」</span><span class="sxs-lookup"><span data-stu-id="ff167-356">Contains "per monitor"</span></span>            | <span data-ttu-id="ff167-357">**Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。</span><span class="sxs-lookup"><span data-stu-id="ff167-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="ff167-358">**Windows 8.1 和 Windows 10：** 目前的進程是個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="ff167-359">包含任何其他字串</span><span class="sxs-lookup"><span data-stu-id="ff167-359">Contains any other string</span></span>         | <span data-ttu-id="ff167-360">**Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。</span><span class="sxs-lookup"><span data-stu-id="ff167-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="ff167-361">**Windows 8.1 和 Windows 10：** 目前的進程不感知 DPI，而且您無法藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，以程式設計方式變更此設定。</span><span class="sxs-lookup"><span data-stu-id="ff167-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="ff167-362">如需 DPI 感知設定的詳細資訊，請參閱 [Dpi 感知層級的比較](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))。</span><span class="sxs-lookup"><span data-stu-id="ff167-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="ff167-363">**DPIAware** 沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="ff167-364">DPIAwareness</span><span class="sxs-lookup"><span data-stu-id="ff167-364">dpiAwareness</span></span>

<span data-ttu-id="ff167-365">指定目前的進程是否為每英寸的點 (DPI) 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="ff167-366">支援 **DPIAwareness** 元素之作業系統的最低版本是 Windows 10 1607 版。</span><span class="sxs-lookup"><span data-stu-id="ff167-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="ff167-367">針對支援 **DPIAwareness** 專案的版本， **DPIAwareness** 會覆寫 **DPIAware** 元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="ff167-368">如果您想要為 Windows 10 的版本1607指定不同的行為，您可以在資訊清單中包含這兩個元素，而不是舊版作業系統。</span><span class="sxs-lookup"><span data-stu-id="ff167-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="ff167-369">**DpiAwareness** 元素可以包含單一專案或逗點分隔專案的清單。</span><span class="sxs-lookup"><span data-stu-id="ff167-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="ff167-370">在後者的情況下，會使用作業系統所辨識清單中第一個 (最左邊的) 專案。</span><span class="sxs-lookup"><span data-stu-id="ff167-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="ff167-371">如此一來，您就可以指定未來 Windows 作業系統版本所支援的不同行為。</span><span class="sxs-lookup"><span data-stu-id="ff167-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="ff167-372">下表描述根據 **DPIAwareness** 元素是否存在，以及其在最左邊辨識的專案中包含的文字所產生的行為。</span><span class="sxs-lookup"><span data-stu-id="ff167-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="ff167-373">元素內的文字不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ff167-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="ff167-374">**DPIAwareness** 元素狀態：</span><span class="sxs-lookup"><span data-stu-id="ff167-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="ff167-375">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="ff167-376">元素不存在</span><span class="sxs-lookup"><span data-stu-id="ff167-376">Element is absent</span></span>                       | <span data-ttu-id="ff167-377">**DpiAware** 元素會指定進程是否為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="ff167-378">未包含任何可識別的專案</span><span class="sxs-lookup"><span data-stu-id="ff167-378">Contains no recognized items</span></span>            | <span data-ttu-id="ff167-379">目前的進程預設為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="ff167-380">您可以藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。</span><span class="sxs-lookup"><span data-stu-id="ff167-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="ff167-381">第一個被辨識的專案是 "system"</span><span class="sxs-lookup"><span data-stu-id="ff167-381">First recognized item is "system"</span></span>       | <span data-ttu-id="ff167-382">目前的進程是系統 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="ff167-383">第一個被辨識的專案是 "permonitor"</span><span class="sxs-lookup"><span data-stu-id="ff167-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="ff167-384">目前的進程是個別監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="ff167-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="ff167-385">第一個被辨識的專案是 "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="ff167-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="ff167-386">目前的進程會使用每個監視器-v2 DPI 感知內容。</span><span class="sxs-lookup"><span data-stu-id="ff167-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="ff167-387">此專案只會在 Windows 10 版本1703或更新版本上識別。</span><span class="sxs-lookup"><span data-stu-id="ff167-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="ff167-388">第一個被辨識的專案是「不知道」</span><span class="sxs-lookup"><span data-stu-id="ff167-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="ff167-389">目前的進程不會察覺 DPI。</span><span class="sxs-lookup"><span data-stu-id="ff167-389">The current process is dpi unaware.</span></span> <span data-ttu-id="ff167-390">您 **無法** 藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。</span><span class="sxs-lookup"><span data-stu-id="ff167-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="ff167-391">如需此元素所支援之 DPI 感知設定的詳細資訊，請參閱 [DPI \_ 感知](/windows/desktop/api/windef/ne-windef-dpi_awareness) 和 [DPI \_ 感知 \_ 內容](/windows/desktop/hidpi/dpi-awareness-context)。</span><span class="sxs-lookup"><span data-stu-id="ff167-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="ff167-392">**DPIAwareness** 沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="ff167-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="ff167-393">gdiScaling</span></span>

<span data-ttu-id="ff167-394">指定是否啟用 GDI 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="ff167-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="ff167-395">支援 **gdiScaling** 元素之作業系統的最低版本是 Windows 10 版本1703。</span><span class="sxs-lookup"><span data-stu-id="ff167-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="ff167-396">GDI (圖形裝置介面) framework 可以針對個別監視器將 DPI 縮放比例套用至基本和文字，而不需要更新應用程式本身。</span><span class="sxs-lookup"><span data-stu-id="ff167-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="ff167-397">這對於不會再主動更新的 GDI 應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="ff167-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="ff167-398">非向量圖形 (例如點陣圖、圖示或工具列) 無法由此元素縮放。</span><span class="sxs-lookup"><span data-stu-id="ff167-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="ff167-399">此外，在應用程式動態建立的點陣圖內出現的圖形和文字也無法由此元素進行縮放。</span><span class="sxs-lookup"><span data-stu-id="ff167-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="ff167-400">**TRUE** 表示已啟用這個元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="ff167-401">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="ff167-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="ff167-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="ff167-403">指定是否啟用高解析度滾動感知功能。</span><span class="sxs-lookup"><span data-stu-id="ff167-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="ff167-404">**TRUE** 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="ff167-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="ff167-405">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="ff167-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="ff167-406">longPathAware</span></span>

<span data-ttu-id="ff167-407">啟用長度超過 **MAX_PATH** 的長路徑。</span><span class="sxs-lookup"><span data-stu-id="ff167-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="ff167-408">在 Windows 10、1607版和更新版本中支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="ff167-409">如需詳細資訊，請參閱[這篇文章](../fileio/maximum-file-path-limitation.md)。</span><span class="sxs-lookup"><span data-stu-id="ff167-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="ff167-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="ff167-410">printerDriverIsolation</span></span>

<span data-ttu-id="ff167-411">指定是否啟用印表機驅動程式隔離。</span><span class="sxs-lookup"><span data-stu-id="ff167-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="ff167-412">**TRUE** 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="ff167-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="ff167-413">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-413">It has no attributes.</span></span> <span data-ttu-id="ff167-414">印表機驅動程式隔離可讓印表機驅動程式在與執行列印多工緩衝處理器不同的處理常式中執行，藉以改善 Windows 列印服務的可靠性。</span><span class="sxs-lookup"><span data-stu-id="ff167-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="ff167-415">在 Windows 7 和 Windows Server 2008 R2 中開始支援印表機驅動程式隔離。</span><span class="sxs-lookup"><span data-stu-id="ff167-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="ff167-416">應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以獨立于印表機驅動程式，並改善其可靠性。</span><span class="sxs-lookup"><span data-stu-id="ff167-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="ff167-417">也就是說，如果印表機驅動程式發生錯誤，應用程式將不會損毀。</span><span class="sxs-lookup"><span data-stu-id="ff167-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="ff167-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="ff167-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="ff167-419">指定是否啟用超高解析度-滾動功能感知功能。</span><span class="sxs-lookup"><span data-stu-id="ff167-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="ff167-420">**TRUE** 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="ff167-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="ff167-421">它沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="ff167-422">msix</span><span class="sxs-lookup"><span data-stu-id="ff167-422">msix</span></span>

<span data-ttu-id="ff167-423">為目前的應用程式指定 [稀疏 MSIX 封裝](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) 的身分識別資訊。</span><span class="sxs-lookup"><span data-stu-id="ff167-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="ff167-424">在 Windows 10、2004版和更新版本中支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="ff167-425">**Msix** 元素必須在命名空間中 `urn:schemas-microsoft-com:msix.v1` 。</span><span class="sxs-lookup"><span data-stu-id="ff167-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="ff167-426">它包含下表所示的屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="ff167-427">屬性</span><span class="sxs-lookup"><span data-stu-id="ff167-427">Attribute</span></span>   | <span data-ttu-id="ff167-428">描述</span><span class="sxs-lookup"><span data-stu-id="ff167-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff167-429">**publisher**</span><span class="sxs-lookup"><span data-stu-id="ff167-429">**publisher**</span></span>    | <span data-ttu-id="ff167-430">描述發行者資訊。</span><span class="sxs-lookup"><span data-stu-id="ff167-430">Describes the publisher information.</span></span> <span data-ttu-id="ff167-431">這個值必須符合您的稀疏套件資訊清單中 [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity)元素的 **發行者** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="ff167-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="ff167-432">**packageName**</span></span> | <span data-ttu-id="ff167-433">描述封裝的內容。</span><span class="sxs-lookup"><span data-stu-id="ff167-433">Describes the contents of the package.</span></span> <span data-ttu-id="ff167-434">這個值必須符合您的稀疏套件資訊清單中 [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity)元素的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="ff167-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="ff167-435">**applicationId**</span></span>    | <span data-ttu-id="ff167-436">應用程式的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff167-436">The unique identifier of the application.</span></span> <span data-ttu-id="ff167-437">這個值必須符合您的稀疏套件資訊清單中 [應用程式](/uwp/schemas/appxpackage/uapmanifestschema/element-application)元素的 **識別碼** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="ff167-438">heapType</span><span class="sxs-lookup"><span data-stu-id="ff167-438">heapType</span></span>

<span data-ttu-id="ff167-439">覆寫 [Win32 堆積 api](../Memory/heap-functions.md) 要使用的預設堆積執行。</span><span class="sxs-lookup"><span data-stu-id="ff167-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="ff167-440">值 **SegmentHeap** 表示將使用區段堆積。</span><span class="sxs-lookup"><span data-stu-id="ff167-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="ff167-441">區段堆積是新式的堆積執行，通常會降低整體記憶體的使用量。</span><span class="sxs-lookup"><span data-stu-id="ff167-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="ff167-442">Windows 10 2004 版 (build 19041) 和更新版本支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="ff167-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="ff167-443">所有其他值都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ff167-443">All other values are ignored.</span></span>

<span data-ttu-id="ff167-444">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="ff167-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="ff167-445">範例</span><span class="sxs-lookup"><span data-stu-id="ff167-445">Example</span></span>

<span data-ttu-id="ff167-446">以下是名為 MySampleApp.exe 之應用程式的應用程式資訊清單範例。</span><span class="sxs-lookup"><span data-stu-id="ff167-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="ff167-447">應用程式會使用 SampleAssembly 並存元件。</span><span class="sxs-lookup"><span data-stu-id="ff167-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
