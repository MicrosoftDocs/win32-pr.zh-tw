---
description: RemoveRegistry 資料表包含應用程式需要從系統登錄刪除的登錄資訊。
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: RemoveRegistry 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944480"
---
# <a name="removeregistry-table"></a><span data-ttu-id="c2d4f-103">RemoveRegistry 資料表</span><span class="sxs-lookup"><span data-stu-id="c2d4f-103">RemoveRegistry Table</span></span>

<span data-ttu-id="c2d4f-104">RemoveRegistry 資料表包含應用程式需要從系統登錄刪除的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="c2d4f-105">RemoveRegistry 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="c2d4f-106">Column</span><span class="sxs-lookup"><span data-stu-id="c2d4f-106">Column</span></span>         | <span data-ttu-id="c2d4f-107">類型</span><span class="sxs-lookup"><span data-stu-id="c2d4f-107">Type</span></span>                         | <span data-ttu-id="c2d4f-108">答案</span><span class="sxs-lookup"><span data-stu-id="c2d4f-108">Key</span></span> | <span data-ttu-id="c2d4f-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="c2d4f-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="c2d4f-110">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="c2d4f-110">RemoveRegistry</span></span> | [<span data-ttu-id="c2d4f-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="c2d4f-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c2d4f-112">Y</span><span class="sxs-lookup"><span data-stu-id="c2d4f-112">Y</span></span>   | <span data-ttu-id="c2d4f-113">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-113">N</span></span>        |
| <span data-ttu-id="c2d4f-114">Root</span><span class="sxs-lookup"><span data-stu-id="c2d4f-114">Root</span></span>           | [<span data-ttu-id="c2d4f-115">整數</span><span class="sxs-lookup"><span data-stu-id="c2d4f-115">Integer</span></span>](integer.md)       | <span data-ttu-id="c2d4f-116">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-116">N</span></span>   | <span data-ttu-id="c2d4f-117">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-117">N</span></span>        |
| <span data-ttu-id="c2d4f-118">答案</span><span class="sxs-lookup"><span data-stu-id="c2d4f-118">Key</span></span>            | [<span data-ttu-id="c2d4f-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="c2d4f-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="c2d4f-120">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-120">N</span></span>   | <span data-ttu-id="c2d4f-121">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-121">N</span></span>        |
| <span data-ttu-id="c2d4f-122">Name</span><span class="sxs-lookup"><span data-stu-id="c2d4f-122">Name</span></span>           | [<span data-ttu-id="c2d4f-123">格式 化</span><span class="sxs-lookup"><span data-stu-id="c2d4f-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c2d4f-124">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-124">N</span></span>   | <span data-ttu-id="c2d4f-125">Y</span><span class="sxs-lookup"><span data-stu-id="c2d4f-125">Y</span></span>        |
| <span data-ttu-id="c2d4f-126">元件\_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-126">Component\_</span></span>    | [<span data-ttu-id="c2d4f-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="c2d4f-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="c2d4f-128">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-128">N</span></span>   | <span data-ttu-id="c2d4f-129">N</span><span class="sxs-lookup"><span data-stu-id="c2d4f-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c2d4f-130">資料行</span><span class="sxs-lookup"><span data-stu-id="c2d4f-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c2d4f-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="c2d4f-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="c2d4f-132">此資料表的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="c2d4f-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>根</span><span class="sxs-lookup"><span data-stu-id="c2d4f-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="c2d4f-134">登錄值的預先定義根金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="c2d4f-135">常數</span><span class="sxs-lookup"><span data-stu-id="c2d4f-135">Constant</span></span>                          | <span data-ttu-id="c2d4f-136">十六進位</span><span class="sxs-lookup"><span data-stu-id="c2d4f-136">Hexadecimal</span></span> | <span data-ttu-id="c2d4f-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="c2d4f-137">Decimal</span></span> | <span data-ttu-id="c2d4f-138">根金鑰</span><span class="sxs-lookup"><span data-stu-id="c2d4f-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-139">(無)</span><span class="sxs-lookup"><span data-stu-id="c2d4f-139">(none)</span></span>                            | <span data-ttu-id="c2d4f-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="c2d4f-140">\- 0x001</span></span>    | <span data-ttu-id="c2d4f-141">-1</span><span class="sxs-lookup"><span data-stu-id="c2d4f-141">-1</span></span>      | <span data-ttu-id="c2d4f-142">**HKEY \_目前的 \_ 使用者** 安裝程式會在執行每個使用者安裝時設定此機碼。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="c2d4f-143">(無)</span><span class="sxs-lookup"><span data-stu-id="c2d4f-143">(none)</span></span>                            | <span data-ttu-id="c2d4f-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="c2d4f-144">-0x001</span></span>      | <span data-ttu-id="c2d4f-145">-1</span><span class="sxs-lookup"><span data-stu-id="c2d4f-145">-1</span></span>      | <span data-ttu-id="c2d4f-146">**HKEY \_本機 \_ 電腦** 安裝程式會在執行所有使用者安裝時設定此機碼，並將 [**ALLUSERS**](allusers.md) 設定為1。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="c2d4f-147">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="c2d4f-148">0x000</span><span class="sxs-lookup"><span data-stu-id="c2d4f-148">0x000</span></span>       | <span data-ttu-id="c2d4f-149">0</span><span class="sxs-lookup"><span data-stu-id="c2d4f-149">0</span></span>       | <span data-ttu-id="c2d4f-150">**HKEY \_類別 \_ 根目錄** 安裝程式會在每位使用者和每部電腦的 [安裝內容](installation-context.md)中，從 **HKCU \\ Software \\** class hive 移除值。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="c2d4f-151">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="c2d4f-152">0x001</span><span class="sxs-lookup"><span data-stu-id="c2d4f-152">0x001</span></span>       | <span data-ttu-id="c2d4f-153">1</span><span class="sxs-lookup"><span data-stu-id="c2d4f-153">1</span></span>       | <span data-ttu-id="c2d4f-154">**HKEY \_ 目前的 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="c2d4f-155">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="c2d4f-156">0x002</span><span class="sxs-lookup"><span data-stu-id="c2d4f-156">0x002</span></span>       | <span data-ttu-id="c2d4f-157">2</span><span class="sxs-lookup"><span data-stu-id="c2d4f-157">2</span></span>       | <span data-ttu-id="c2d4f-158">**HKEY \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="c2d4f-159">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="c2d4f-160">0x003</span><span class="sxs-lookup"><span data-stu-id="c2d4f-160">0x003</span></span>       | <span data-ttu-id="c2d4f-161">3</span><span class="sxs-lookup"><span data-stu-id="c2d4f-161">3</span></span>       | <span data-ttu-id="c2d4f-162">**HKEY \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="c2d4f-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="c2d4f-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="c2d4f-164">登錄值的可當地語系化金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="c2d4f-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="c2d4f-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="c2d4f-166">可當地語系化的登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-166">The localizable registry value name.</span></span>

<span data-ttu-id="c2d4f-167">[名稱] 資料行中的下列字串具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="c2d4f-168">String</span><span class="sxs-lookup"><span data-stu-id="c2d4f-168">String</span></span> | <span data-ttu-id="c2d4f-169">意義</span><span class="sxs-lookup"><span data-stu-id="c2d4f-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-170">"-"</span><span class="sxs-lookup"><span data-stu-id="c2d4f-170">"-"</span></span>    | <span data-ttu-id="c2d4f-171">安裝元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="c2d4f-172">請注意，移除元件時，應該使用登錄 [資料表](registry-table.md) 來建立或移除登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="c2d4f-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c2d4f-174">在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵參考控制登錄值刪除的元件。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2d4f-175">備註</span><span class="sxs-lookup"><span data-stu-id="c2d4f-175">Remarks</span></span>

<span data-ttu-id="c2d4f-176">當已選取要在本機安裝或從來源執行的對應元件時，系統會從系統登錄刪除登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="c2d4f-177">當 [RemoveRegistryValues 動作](removeregistryvalues-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="c2d4f-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="c2d4f-178">驗證</span><span class="sxs-lookup"><span data-stu-id="c2d4f-178">Validation</span></span>

<dl>

[<span data-ttu-id="c2d4f-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="c2d4f-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c2d4f-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="c2d4f-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c2d4f-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="c2d4f-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c2d4f-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="c2d4f-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c2d4f-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="c2d4f-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




