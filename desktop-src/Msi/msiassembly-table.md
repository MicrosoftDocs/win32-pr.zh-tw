---
description: MsiAssembly 資料表會指定 Microsoft .NET Framework 元件和 Win32 元件的 Windows Installer 設定。 如需詳細資訊，請參閱將元件安裝到全域組件快取和 Win32 元件的安裝。
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: MsiAssembly 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945331"
---
# <a name="msiassembly-table"></a><span data-ttu-id="a08d8-104">MsiAssembly 資料表</span><span class="sxs-lookup"><span data-stu-id="a08d8-104">MsiAssembly Table</span></span>

<span data-ttu-id="a08d8-105">MsiAssembly 資料表會指定 Microsoft .NET Framework 元件和 Win32 元件的 Windows Installer 設定。</span><span class="sxs-lookup"><span data-stu-id="a08d8-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="a08d8-106">如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="a08d8-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="a08d8-107">在 Windows XP 上，Windows Installer 可以安裝 Win32 元件作為 [並存元件](side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="a08d8-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="a08d8-108">如需詳細資訊，請參閱 [並存元件 API](../sbscs/side-by-side-assembly-api.md)。</span><span class="sxs-lookup"><span data-stu-id="a08d8-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="a08d8-109">**Windows 2000：** 這項功能不受支援。</span><span class="sxs-lookup"><span data-stu-id="a08d8-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="a08d8-110">MsiAssembly 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a08d8-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="a08d8-111">Column</span><span class="sxs-lookup"><span data-stu-id="a08d8-111">Column</span></span>            | <span data-ttu-id="a08d8-112">類型</span><span class="sxs-lookup"><span data-stu-id="a08d8-112">Type</span></span>                         | <span data-ttu-id="a08d8-113">答案</span><span class="sxs-lookup"><span data-stu-id="a08d8-113">Key</span></span> | <span data-ttu-id="a08d8-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="a08d8-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="a08d8-115">元件\_</span><span class="sxs-lookup"><span data-stu-id="a08d8-115">Component\_</span></span>       | [<span data-ttu-id="a08d8-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="a08d8-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="a08d8-117">Y</span><span class="sxs-lookup"><span data-stu-id="a08d8-117">Y</span></span>   | <span data-ttu-id="a08d8-118">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-118">N</span></span>        |
| <span data-ttu-id="a08d8-119">功能\_</span><span class="sxs-lookup"><span data-stu-id="a08d8-119">Feature\_</span></span>         | [<span data-ttu-id="a08d8-120">識別碼</span><span class="sxs-lookup"><span data-stu-id="a08d8-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="a08d8-121">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-121">N</span></span>   | <span data-ttu-id="a08d8-122">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-122">N</span></span>        |
| <span data-ttu-id="a08d8-123">檔案 \_ 資訊清單</span><span class="sxs-lookup"><span data-stu-id="a08d8-123">File\_Manifest</span></span>    | [<span data-ttu-id="a08d8-124">識別碼</span><span class="sxs-lookup"><span data-stu-id="a08d8-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="a08d8-125">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-125">N</span></span>   | <span data-ttu-id="a08d8-126">Y</span><span class="sxs-lookup"><span data-stu-id="a08d8-126">Y</span></span>        |
| <span data-ttu-id="a08d8-127">檔 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="a08d8-127">File\_Application</span></span> | [<span data-ttu-id="a08d8-128">識別碼</span><span class="sxs-lookup"><span data-stu-id="a08d8-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="a08d8-129">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-129">N</span></span>   | <span data-ttu-id="a08d8-130">Y</span><span class="sxs-lookup"><span data-stu-id="a08d8-130">Y</span></span>        |
| <span data-ttu-id="a08d8-131">屬性</span><span class="sxs-lookup"><span data-stu-id="a08d8-131">Attributes</span></span>        | [<span data-ttu-id="a08d8-132">整數</span><span class="sxs-lookup"><span data-stu-id="a08d8-132">Integer</span></span>](integer.md)       | <span data-ttu-id="a08d8-133">N</span><span class="sxs-lookup"><span data-stu-id="a08d8-133">N</span></span>   | <span data-ttu-id="a08d8-134">Y</span><span class="sxs-lookup"><span data-stu-id="a08d8-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a08d8-135">資料行</span><span class="sxs-lookup"><span data-stu-id="a08d8-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a08d8-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="a08d8-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a08d8-137">[元件資料表](component-table.md)中的索引鍵，指定包含此元件的 Windows Installer 元件。</span><span class="sxs-lookup"><span data-stu-id="a08d8-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="a08d8-138">此欄位中的值不得設定為 null。</span><span class="sxs-lookup"><span data-stu-id="a08d8-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="a08d8-139">[元件資料表](component-table.md)中的元件 KeyPath 欄位不得為 null。</span><span class="sxs-lookup"><span data-stu-id="a08d8-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="a08d8-140">針對 Win32 元件，元件 KeyPath 不能是檔案資訊清單中指定的資訊清單檔 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a08d8-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="a08d8-141">資訊清單可以是 .NET Framework 或原則元件的 keypath。</span><span class="sxs-lookup"><span data-stu-id="a08d8-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="a08d8-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="a08d8-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="a08d8-143">[功能資料表](feature-table.md)中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a08d8-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="a08d8-144">當功能安裝必須安裝元件時，Windows Installer 會安裝這個欄位所指向的功能。</span><span class="sxs-lookup"><span data-stu-id="a08d8-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="a08d8-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>檔案 \_ 資訊清單</span><span class="sxs-lookup"><span data-stu-id="a08d8-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="a08d8-146">檔案 [資料表](file-table.md) 中的外部索引鍵，指定包含 .NET Framework 元件或 Win32 元件之資訊清單的檔案。</span><span class="sxs-lookup"><span data-stu-id="a08d8-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="a08d8-147">若為 Win32 元件，請勿在 [元件資料表](component-table.md)的 [KeyPath] 欄位中，將此檔案指定為元件金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="a08d8-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="a08d8-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>檔 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="a08d8-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="a08d8-149">若要在私用位置安裝元件，請在此欄位中輸入元件元件的金鑰路徑檔案。</span><span class="sxs-lookup"><span data-stu-id="a08d8-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="a08d8-150">這是出現在 [元件資料表](component-table.md)的 KeyPath 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="a08d8-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="a08d8-151">然後，安裝程式可以將元件安裝到 [目錄資料表](directory-table.md)中所指定之元件的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="a08d8-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="a08d8-152">如果要將元件安裝到全域組件快取中，這個欄位必須是 null。</span><span class="sxs-lookup"><span data-stu-id="a08d8-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="a08d8-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="a08d8-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="a08d8-154">輸入 1 (一個 Win32 元件的) 值。</span><span class="sxs-lookup"><span data-stu-id="a08d8-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="a08d8-155">輸入 .NET Framework 元件的值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="a08d8-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="a08d8-156">如果 [屬性] 資料行是 Null，則安裝程式會將元件視為 .NET Framework 元件。</span><span class="sxs-lookup"><span data-stu-id="a08d8-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a08d8-157">備註</span><span class="sxs-lookup"><span data-stu-id="a08d8-157">Remarks</span></span>

<span data-ttu-id="a08d8-158">如果 MsiAssembly 資料表中至少有一個專案，則 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 必須包含 [MsiPublishAssemblies 動作](msipublishassemblies-action.md)和 [MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md)。</span><span class="sxs-lookup"><span data-stu-id="a08d8-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="a08d8-159">因為元件無法在認可之後復原，Windows Installer 會使用兩步驟的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="a08d8-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="a08d8-160">元件的介面是在 [MsiPublishAssemblies 動作](msipublishassemblies-action.md)所產生的安裝作業期間建立。</span><span class="sxs-lookup"><span data-stu-id="a08d8-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="a08d8-161">在成功執行 [InstallFinalize 動作](installfinalize-action.md)之前，不會認可這些元件。</span><span class="sxs-lookup"><span data-stu-id="a08d8-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="a08d8-162">這表示，如果您撰寫相依元件的自訂動作或資源，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="a08d8-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="a08d8-163">例如，如果您需要啟動相依于全域組件快取中元件 (GAC) 的服務，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排程該服務的啟動。</span><span class="sxs-lookup"><span data-stu-id="a08d8-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="a08d8-164">這表示您無法使用 [ServiceControl 資料表](servicecontrol-table.md) 來啟動服務，而是必須使用在 InstallFinalize 之後排序的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a08d8-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="a08d8-165">驗證</span><span class="sxs-lookup"><span data-stu-id="a08d8-165">Validation</span></span>

<dl>

[<span data-ttu-id="a08d8-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="a08d8-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a08d8-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="a08d8-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a08d8-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="a08d8-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a08d8-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="a08d8-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="a08d8-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="a08d8-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="a08d8-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="a08d8-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
