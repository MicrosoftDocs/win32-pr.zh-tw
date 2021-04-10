---
description: Windows Installer 開發人員可以使用本主題中的指導方針來撰寫包含元件的 Windows Installer 套件。
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: 將元件加入封裝中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192471"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="7d1a9-103">將元件加入封裝中</span><span class="sxs-lookup"><span data-stu-id="7d1a9-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="7d1a9-104">Windows Installer 開發人員可以使用本主題中的指導方針來撰寫包含元件的 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="7d1a9-105">下列指導方針適用于 Win32 元件，以及 Microsoft .NET Framework 的 common language runtime 所使用的元件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="7d1a9-106">Windows Installer 的元件不能包含一個以上的元件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="7d1a9-107">元件中的所有檔案都應該在單一元件中。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="7d1a9-108">包含元件的每個元件都應該在 [MsiAssembly](msiassembly-table.md) 資料表中有一個專案。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="7d1a9-109">每個元件的強式組件快取名稱都應該撰寫到 [MsiAssemblyName](msiassemblyname-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="7d1a9-110">當您註冊元件的 COM Interop [時，請使用登錄表，](registry-table.md) 而不是 [類別](class-table.md) 表。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="7d1a9-111">具有相同強式名稱的元件是相同的元件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="7d1a9-112">當不同的應用程式安裝相同的元件時，包含元件的元件應該在其 [元件](component-table.md) 資料表中使用相同的值。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="7d1a9-113">產品公告可識別可由不同應用程式安裝和使用的元件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="7d1a9-114">產品公告未識別私用元件。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="7d1a9-115">加入 Win32 元件</span><span class="sxs-lookup"><span data-stu-id="7d1a9-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="7d1a9-116">當您包含 Win32 元件時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="7d1a9-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="7d1a9-117">[元件資料表中](component-table.md)包含 Win32 元件的 KeyPath 值不應為 Null。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="7d1a9-118">[元件資料表中](component-table.md)包含 Win32 原則元件的 KeyPath 值應該是資訊清單檔。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="7d1a9-119">[元件資料表中](component-table.md)包含 Win32 元件的 KeyPath 值，不是原則元件，不應該是資訊清單檔案或類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="7d1a9-120">它應該是元件中的不同檔案。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="7d1a9-121">針對 Win32 元件資訊清單的 **assemblyIdentity** 區段中所列的每個名稱和值組，將資料列加入至 [MsiAssemblyName](msiassemblyname-table.md)資料表。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="7d1a9-122">加入與 .NET Framework 搭配使用的元件</span><span class="sxs-lookup"><span data-stu-id="7d1a9-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="7d1a9-123">當您包含 .NET Framework 的 common language runtime 所使用的元件時，請使用下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="7d1a9-124">[元件資料表中](component-table.md)包含元件的 KeyPath 值不應為 Null。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="7d1a9-125">當您將 common language runtime 所使用的元件安裝到全域組件快取時，MsiAssembly 資料表的 File Application 資料行中的值 \_ 必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="7d1a9-126">針對元件強式名稱的每個屬性，將資料列加入至 [MsiAssemblyName](msiassemblyname-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="7d1a9-127">所有元件都必須有 MsiAssemblyName 資料表中所指定的名稱、版本和文化特性屬性。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="7d1a9-128">全域程式集需要 publicKeyToken 屬性。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="7d1a9-129">下表是通用語言執行平臺使用之通用群組件的 MsiAssemblyName 資料表範例。</span><span class="sxs-lookup"><span data-stu-id="7d1a9-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="7d1a9-130">MsiAssemblyName 資料表</span><span class="sxs-lookup"><span data-stu-id="7d1a9-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="7d1a9-131">元件</span><span class="sxs-lookup"><span data-stu-id="7d1a9-131">Component</span></span>  | <span data-ttu-id="7d1a9-132">Name</span><span class="sxs-lookup"><span data-stu-id="7d1a9-132">Name</span></span>           | <span data-ttu-id="7d1a9-133">值</span><span class="sxs-lookup"><span data-stu-id="7d1a9-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="7d1a9-134">ComponentA</span><span class="sxs-lookup"><span data-stu-id="7d1a9-134">ComponentA</span></span> | <span data-ttu-id="7d1a9-135">Name</span><span class="sxs-lookup"><span data-stu-id="7d1a9-135">Name</span></span>           | <span data-ttu-id="7d1a9-136">simple</span><span class="sxs-lookup"><span data-stu-id="7d1a9-136">simple</span></span>           |
| <span data-ttu-id="7d1a9-137">ComponentA</span><span class="sxs-lookup"><span data-stu-id="7d1a9-137">ComponentA</span></span> | <span data-ttu-id="7d1a9-138">version</span><span class="sxs-lookup"><span data-stu-id="7d1a9-138">version</span></span>        | <span data-ttu-id="7d1a9-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="7d1a9-139">1.0.0.0</span></span>          |
| <span data-ttu-id="7d1a9-140">ComponentA</span><span class="sxs-lookup"><span data-stu-id="7d1a9-140">ComponentA</span></span> | <span data-ttu-id="7d1a9-141">文化特性</span><span class="sxs-lookup"><span data-stu-id="7d1a9-141">Culture</span></span>        | <span data-ttu-id="7d1a9-142">neutral</span><span class="sxs-lookup"><span data-stu-id="7d1a9-142">neutral</span></span>          |
| <span data-ttu-id="7d1a9-143">ComponentA</span><span class="sxs-lookup"><span data-stu-id="7d1a9-143">ComponentA</span></span> | <span data-ttu-id="7d1a9-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="7d1a9-144">publicKeyToken</span></span> | <span data-ttu-id="7d1a9-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="7d1a9-145">9d1ec8380f483f5a</span></span> |



 

 

 



