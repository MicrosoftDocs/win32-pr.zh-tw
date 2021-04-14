---
description: 請注意，您無法使用 SelfRegModules 和 SelfUnRegModules 動作來指定安裝程式註冊或取消註冊自行註冊 Dll 的順序。
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: 指定自我註冊的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469276"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="d2b1c-103">指定自我註冊的順序</span><span class="sxs-lookup"><span data-stu-id="d2b1c-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="d2b1c-104">請注意，您無法使用 [SelfRegModules](selfregmodules-action.md) 和 [SelfUnRegModules](selfunregmodules-action.md) 動作來指定安裝程式註冊或取消註冊自行註冊 dll 的順序。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="d2b1c-105">這些動作會註冊 [SelfReg 資料表](selfreg-table.md)中列出的所有模組。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="d2b1c-106">安裝程式不會自行註冊 .exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="d2b1c-107">若要指定安裝程式註冊或取消註冊模組的順序，您必須針對每個模組使用兩個 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="d2b1c-108">一個用於 DllRegisterServer 的自訂動作，另一個用於 DllUnregisterServer。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="d2b1c-109">然後，這些自訂動作必須在 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中，于要註冊或取消註冊 DLL 的位置，于順序中撰寫。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="d2b1c-110">下列範例說明如何撰寫資料庫，以排程在動作順序的特定點自行註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="d2b1c-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="d2b1c-111">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d2b1c-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="d2b1c-112">檔案</span><span class="sxs-lookup"><span data-stu-id="d2b1c-112">File</span></span>  | <span data-ttu-id="d2b1c-113">元件\_</span><span class="sxs-lookup"><span data-stu-id="d2b1c-113">Component\_</span></span> | <span data-ttu-id="d2b1c-114">FileName</span><span class="sxs-lookup"><span data-stu-id="d2b1c-114">FileName</span></span>  | <span data-ttu-id="d2b1c-115">順序</span><span class="sxs-lookup"><span data-stu-id="d2b1c-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="d2b1c-116">mydll.dll</span><span class="sxs-lookup"><span data-stu-id="d2b1c-116">mydll</span></span> | <span data-ttu-id="d2b1c-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="d2b1c-117">myComponent</span></span> | <span data-ttu-id="d2b1c-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="d2b1c-118">Mydll.dll</span></span> | <span data-ttu-id="d2b1c-119">13</span><span class="sxs-lookup"><span data-stu-id="d2b1c-119">13</span></span>       |



 

<span data-ttu-id="d2b1c-120">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d2b1c-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d2b1c-121">元件</span><span class="sxs-lookup"><span data-stu-id="d2b1c-121">Component</span></span>   | <span data-ttu-id="d2b1c-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="d2b1c-122">ComponentId</span></span> | <span data-ttu-id="d2b1c-123">目錄\_</span><span class="sxs-lookup"><span data-stu-id="d2b1c-123">Directory\_</span></span> | <span data-ttu-id="d2b1c-124">KeyPath</span><span class="sxs-lookup"><span data-stu-id="d2b1c-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="d2b1c-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="d2b1c-125">myComponent</span></span> | <span data-ttu-id="d2b1c-126">{*GUID*}</span><span class="sxs-lookup"><span data-stu-id="d2b1c-126">{*a GUID*}</span></span>  | <span data-ttu-id="d2b1c-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="d2b1c-127">myFolder</span></span>    | <span data-ttu-id="d2b1c-128">mydll.dll</span><span class="sxs-lookup"><span data-stu-id="d2b1c-128">mydll</span></span>   |



 

[<span data-ttu-id="d2b1c-129">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="d2b1c-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="d2b1c-130">目錄</span><span class="sxs-lookup"><span data-stu-id="d2b1c-130">Directory</span></span> | <span data-ttu-id="d2b1c-131">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="d2b1c-131">Directory\_Parent</span></span> | <span data-ttu-id="d2b1c-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="d2b1c-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="d2b1c-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="d2b1c-133">TARGETDIR</span></span> |                   | <span data-ttu-id="d2b1c-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="d2b1c-134">SourceDir</span></span>           |
| <span data-ttu-id="d2b1c-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="d2b1c-135">myFolder</span></span>  | <span data-ttu-id="d2b1c-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="d2b1c-136">TARGETDIR</span></span>         | <span data-ttu-id="d2b1c-137">myFolder \| 我的資料夾</span><span class="sxs-lookup"><span data-stu-id="d2b1c-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="d2b1c-138">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="d2b1c-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="d2b1c-139">動作</span><span class="sxs-lookup"><span data-stu-id="d2b1c-139">Action</span></span>     | <span data-ttu-id="d2b1c-140">類型</span><span class="sxs-lookup"><span data-stu-id="d2b1c-140">Type</span></span> | <span data-ttu-id="d2b1c-141">來源</span><span class="sxs-lookup"><span data-stu-id="d2b1c-141">Source</span></span>   | <span data-ttu-id="d2b1c-142">目標</span><span class="sxs-lookup"><span data-stu-id="d2b1c-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="d2b1c-143">mydllREG</span><span class="sxs-lookup"><span data-stu-id="d2b1c-143">mydllREG</span></span>   | <span data-ttu-id="d2b1c-144">3170</span><span class="sxs-lookup"><span data-stu-id="d2b1c-144">3170</span></span> | <span data-ttu-id="d2b1c-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="d2b1c-145">myFolder</span></span> | <span data-ttu-id="d2b1c-146">" \[ SystemFolder \] msiexec"/y " \[ \# mydll.dll \] "</span><span class="sxs-lookup"><span data-stu-id="d2b1c-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="d2b1c-147">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="d2b1c-147">mydllUNREG</span></span> | <span data-ttu-id="d2b1c-148">3170</span><span class="sxs-lookup"><span data-stu-id="d2b1c-148">3170</span></span> | <span data-ttu-id="d2b1c-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="d2b1c-149">myFolder</span></span> | <span data-ttu-id="d2b1c-150">" \[ SystemFolder \] msiexec"/z " \[ \# mydll.dll \] "</span><span class="sxs-lookup"><span data-stu-id="d2b1c-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="d2b1c-151">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d2b1c-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="d2b1c-152">動作</span><span class="sxs-lookup"><span data-stu-id="d2b1c-152">Action</span></span>           | <span data-ttu-id="d2b1c-153">條件</span><span class="sxs-lookup"><span data-stu-id="d2b1c-153">Condition</span></span>         | <span data-ttu-id="d2b1c-154">順序</span><span class="sxs-lookup"><span data-stu-id="d2b1c-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="d2b1c-155">SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="d2b1c-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="d2b1c-156">2200</span><span class="sxs-lookup"><span data-stu-id="d2b1c-156">2200</span></span>     |
| <span data-ttu-id="d2b1c-157">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="d2b1c-157">mydllUNREG</span></span>       | <span data-ttu-id="d2b1c-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="d2b1c-158">$myComponent=2</span></span>    | <span data-ttu-id="d2b1c-159">2201</span><span class="sxs-lookup"><span data-stu-id="d2b1c-159">2201</span></span>     |
| <span data-ttu-id="d2b1c-160">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="d2b1c-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="d2b1c-161">3500</span><span class="sxs-lookup"><span data-stu-id="d2b1c-161">3500</span></span>     |
| <span data-ttu-id="d2b1c-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="d2b1c-162">InstallFiles</span></span>     |                   | <span data-ttu-id="d2b1c-163">4000</span><span class="sxs-lookup"><span data-stu-id="d2b1c-163">4000</span></span>     |
| <span data-ttu-id="d2b1c-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="d2b1c-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="d2b1c-165">6500</span><span class="sxs-lookup"><span data-stu-id="d2b1c-165">6500</span></span>     |
| <span data-ttu-id="d2b1c-166">mydllREG</span><span class="sxs-lookup"><span data-stu-id="d2b1c-166">mydllREG</span></span>         | <span data-ttu-id="d2b1c-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="d2b1c-167">$myComponent>2</span></span> | <span data-ttu-id="d2b1c-168">6501</span><span class="sxs-lookup"><span data-stu-id="d2b1c-168">6501</span></span>     |



 

 

 



