---
description: MsiAssembly 資料表和 MsiAssemblyName 資料表會指定 common language runtime 元件和 Win32 元件的 Windows Installer 設定。
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: MsiAssemblyName 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997986"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="531b6-103">MsiAssemblyName 資料表</span><span class="sxs-lookup"><span data-stu-id="531b6-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="531b6-104">[MsiAssembly 資料表](msiassembly-table.md)和 MsiAssemblyName 資料表會指定 common language runtime 元件和 Win32 元件的 Windows Installer 設定。</span><span class="sxs-lookup"><span data-stu-id="531b6-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="531b6-105">如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="531b6-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="531b6-106">MsiAssemblyName 資料表會針對 .NET Framework 或 Win32 元件的強式組件快取名稱指定元素的架構。</span><span class="sxs-lookup"><span data-stu-id="531b6-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="531b6-107">名稱的建立方式是附加具有相同元件索引鍵的所有元素 \_ 。</span><span class="sxs-lookup"><span data-stu-id="531b6-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="531b6-108">請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="531b6-108">See the following example.</span></span>

<span data-ttu-id="531b6-109">Windows Installer 可以將 Win32 元件安裝為 [並存元件](side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="531b6-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="531b6-110">如需詳細資訊，請參閱 [並存元件 API](../sbscs/side-by-side-assembly-api.md)。</span><span class="sxs-lookup"><span data-stu-id="531b6-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="531b6-111">MsiAssemblyName 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="531b6-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="531b6-112">Column</span><span class="sxs-lookup"><span data-stu-id="531b6-112">Column</span></span>      | <span data-ttu-id="531b6-113">類型</span><span class="sxs-lookup"><span data-stu-id="531b6-113">Type</span></span>                         | <span data-ttu-id="531b6-114">答案</span><span class="sxs-lookup"><span data-stu-id="531b6-114">Key</span></span> | <span data-ttu-id="531b6-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="531b6-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="531b6-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="531b6-116">Component\_</span></span> | [<span data-ttu-id="531b6-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="531b6-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="531b6-118">Y</span><span class="sxs-lookup"><span data-stu-id="531b6-118">Y</span></span>   | <span data-ttu-id="531b6-119">N</span><span class="sxs-lookup"><span data-stu-id="531b6-119">N</span></span>        |
| <span data-ttu-id="531b6-120">Name</span><span class="sxs-lookup"><span data-stu-id="531b6-120">Name</span></span>        | [<span data-ttu-id="531b6-121">Text</span><span class="sxs-lookup"><span data-stu-id="531b6-121">Text</span></span>](text.md)             | <span data-ttu-id="531b6-122">Y</span><span class="sxs-lookup"><span data-stu-id="531b6-122">Y</span></span>   | <span data-ttu-id="531b6-123">N</span><span class="sxs-lookup"><span data-stu-id="531b6-123">N</span></span>        |
| <span data-ttu-id="531b6-124">值</span><span class="sxs-lookup"><span data-stu-id="531b6-124">Value</span></span>       | [<span data-ttu-id="531b6-125">Text</span><span class="sxs-lookup"><span data-stu-id="531b6-125">Text</span></span>](text.md)             | <span data-ttu-id="531b6-126">N</span><span class="sxs-lookup"><span data-stu-id="531b6-126">N</span></span>   | <span data-ttu-id="531b6-127">N</span><span class="sxs-lookup"><span data-stu-id="531b6-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="531b6-128">資料行</span><span class="sxs-lookup"><span data-stu-id="531b6-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="531b6-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="531b6-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="531b6-130">指定包含此元件之 Windows Installer 元件的 [元件資料表](component-table.md) 中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="531b6-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="531b6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="531b6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="531b6-132">與 [值] 資料行中指定的值相關聯之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="531b6-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="531b6-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="531b6-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="531b6-134">與 [名稱] 資料行中指定之名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="531b6-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="531b6-135">備註</span><span class="sxs-lookup"><span data-stu-id="531b6-135">Remarks</span></span>

<span data-ttu-id="531b6-136">撰寫至 MsiAssemblyName 資料表的資訊必須符合元件的資訊清單檔中的資訊。</span><span class="sxs-lookup"><span data-stu-id="531b6-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="531b6-137">如果資訊清單和 MsiAssemblyName 資料表中的資訊不相符，則移除應用程式可能會將元件保留在電腦上。</span><span class="sxs-lookup"><span data-stu-id="531b6-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="531b6-138">針對 Win32 元件，[名稱] 欄位中的每個專案都必須在 MsiAssemblyName 資料表中有一個資料列： type、Name、version、language、publicKeyToken 和 processorArchitecture。</span><span class="sxs-lookup"><span data-stu-id="531b6-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="531b6-139">您可以在 [值] 欄位中輸入每個名稱的對應值。</span><span class="sxs-lookup"><span data-stu-id="531b6-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="531b6-140">MsiAssemblyName 資料表中的名稱/值組必須符合元件資訊清單中的類型、名稱、版本、語言、publicKeyToken 和 processorArchitecture 屬性。</span><span class="sxs-lookup"><span data-stu-id="531b6-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="531b6-141">若為私用 common language runtime 元件 ( .NET Frameworkversions 1.0 和 1.1) ，MsiAssemblyName 資料表必須針對 [名稱] 欄位中的每個專案都包含一個資料列： [名稱]、[版本] 和 [文化特性]。</span><span class="sxs-lookup"><span data-stu-id="531b6-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="531b6-142">您可以在 [值] 欄位中輸入每個名稱的對應值。</span><span class="sxs-lookup"><span data-stu-id="531b6-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="531b6-143">針對全域通用語言執行平臺元件 ( .NET Framework 1.0 和 1.1) 版本，MsiAssemblyName 資料表的 [名稱] 欄位中的每個專案都必須包含一個資料列： [名稱]、[版本]、[文化特性] 和 [PublicKeyToken]。</span><span class="sxs-lookup"><span data-stu-id="531b6-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="531b6-144">您可以在 [值] 欄位中輸入每個名稱的對應值。</span><span class="sxs-lookup"><span data-stu-id="531b6-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="531b6-145">.NET Framework 版本1.1 是最小版本，可用來執行全域通用語言執行平臺元件的就地更新。</span><span class="sxs-lookup"><span data-stu-id="531b6-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="531b6-146">您可以檢查版本的 [**MsiNetAssemblySupport**](msinetassemblysupport.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="531b6-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="531b6-147">MsiAssemblyName 資料表也必須有 FileVersion 欄位，因為這種類型的元件更新只會變更 FileVersion。</span><span class="sxs-lookup"><span data-stu-id="531b6-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="531b6-148">如需詳細資訊，請參閱 [更新元件](updating-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="531b6-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="531b6-149">例如，ComponentA 的組件資訊清單可能會有 Win32 元件的 assemblyIdentity 區段，如下所示。</span><span class="sxs-lookup"><span data-stu-id="531b6-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="531b6-150">在此情況下，請填入 MsiAssemblyName 資料表，如下所示。</span><span class="sxs-lookup"><span data-stu-id="531b6-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="531b6-151">元件</span><span class="sxs-lookup"><span data-stu-id="531b6-151">Component</span></span>  | <span data-ttu-id="531b6-152">Name</span><span class="sxs-lookup"><span data-stu-id="531b6-152">Name</span></span>                  | <span data-ttu-id="531b6-153">值</span><span class="sxs-lookup"><span data-stu-id="531b6-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="531b6-154">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-154">ComponentA</span></span> | <span data-ttu-id="531b6-155">類型</span><span class="sxs-lookup"><span data-stu-id="531b6-155">type</span></span>                  | <span data-ttu-id="531b6-156">win32</span><span class="sxs-lookup"><span data-stu-id="531b6-156">win32</span></span>             |
| <span data-ttu-id="531b6-157">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-157">ComponentA</span></span> | <span data-ttu-id="531b6-158">NAME</span><span class="sxs-lookup"><span data-stu-id="531b6-158">name</span></span>                  | <span data-ttu-id="531b6-159">sxstest-簡單</span><span class="sxs-lookup"><span data-stu-id="531b6-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="531b6-160">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-160">ComponentA</span></span> | <span data-ttu-id="531b6-161">version</span><span class="sxs-lookup"><span data-stu-id="531b6-161">version</span></span>               | <span data-ttu-id="531b6-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="531b6-162">1.0.0.0</span></span>           |
| <span data-ttu-id="531b6-163">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-163">ComponentA</span></span> | <span data-ttu-id="531b6-164">語言</span><span class="sxs-lookup"><span data-stu-id="531b6-164">language</span></span>              | <span data-ttu-id="531b6-165">en</span><span class="sxs-lookup"><span data-stu-id="531b6-165">en</span></span>                |
| <span data-ttu-id="531b6-166">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-166">ComponentA</span></span> | <span data-ttu-id="531b6-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="531b6-167">publicKeyToken</span></span>        | <span data-ttu-id="531b6-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="531b6-168">1111111111222222</span></span>  |
| <span data-ttu-id="531b6-169">ComponentA</span><span class="sxs-lookup"><span data-stu-id="531b6-169">ComponentA</span></span> | <span data-ttu-id="531b6-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="531b6-170">processorArchitecture</span></span> | <span data-ttu-id="531b6-171">x86</span><span class="sxs-lookup"><span data-stu-id="531b6-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="531b6-172">驗證</span><span class="sxs-lookup"><span data-stu-id="531b6-172">Validation</span></span>

<dl>

[<span data-ttu-id="531b6-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="531b6-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="531b6-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="531b6-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="531b6-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="531b6-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="531b6-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="531b6-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="531b6-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="531b6-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
