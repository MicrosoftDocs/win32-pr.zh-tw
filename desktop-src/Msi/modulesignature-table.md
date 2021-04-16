---
description: ModuleSignature 資料表是必要的資料表。
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513489"
---
# <a name="modulesignature-table"></a><span data-ttu-id="3bfa3-103">ModuleSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="3bfa3-103">ModuleSignature Table</span></span>

<span data-ttu-id="3bfa3-104">ModuleSignature 資料表是必要的資料表。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="3bfa3-105">它包含識別合併模組所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="3bfa3-106">合併工具會將此資料表加入至 .msi 檔案（如果尚未存在的話）。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="3bfa3-107">Merge 模組中的 ModuleSignature 資料表只有一個資料列包含 ModuleID、Language 和 Version。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="3bfa3-108">不過，.msi 檔案中的 ModuleSignature 資料表具有一個資料列，其中包含每個已合併至其中的 .msm 檔案的這項資訊。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="3bfa3-109">合併和驗證工具會檢查 .msi 檔案中的 ModuleSignature 資料表，以判斷它是否具有目前合併模組所需的所有相依合併模組 (請參閱 [ModuleDependency 資料表](moduledependency-table.md)) 以及安裝封裝是否先前與任何衝突的合併模組合併 (請參閱 [ModuleExclusion 資料表](moduleexclusion-table.md)) 。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="3bfa3-110">ModuleSignature 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="3bfa3-111">Column</span><span class="sxs-lookup"><span data-stu-id="3bfa3-111">Column</span></span>   | <span data-ttu-id="3bfa3-112">類型</span><span class="sxs-lookup"><span data-stu-id="3bfa3-112">Type</span></span>                         | <span data-ttu-id="3bfa3-113">答案</span><span class="sxs-lookup"><span data-stu-id="3bfa3-113">Key</span></span> | <span data-ttu-id="3bfa3-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="3bfa3-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="3bfa3-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3bfa3-115">ModuleID</span></span> | [<span data-ttu-id="3bfa3-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="3bfa3-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="3bfa3-117">Y</span><span class="sxs-lookup"><span data-stu-id="3bfa3-117">Y</span></span>   | <span data-ttu-id="3bfa3-118">N</span><span class="sxs-lookup"><span data-stu-id="3bfa3-118">N</span></span>        |
| <span data-ttu-id="3bfa3-119">語言</span><span class="sxs-lookup"><span data-stu-id="3bfa3-119">Language</span></span> | [<span data-ttu-id="3bfa3-120">整數</span><span class="sxs-lookup"><span data-stu-id="3bfa3-120">Integer</span></span>](integer.md)       | <span data-ttu-id="3bfa3-121">Y</span><span class="sxs-lookup"><span data-stu-id="3bfa3-121">Y</span></span>   | <span data-ttu-id="3bfa3-122">N</span><span class="sxs-lookup"><span data-stu-id="3bfa3-122">N</span></span>        |
| <span data-ttu-id="3bfa3-123">版本</span><span class="sxs-lookup"><span data-stu-id="3bfa3-123">Version</span></span>  | [<span data-ttu-id="3bfa3-124">版本</span><span class="sxs-lookup"><span data-stu-id="3bfa3-124">Version</span></span>](version.md)       |     | <span data-ttu-id="3bfa3-125">N</span><span class="sxs-lookup"><span data-stu-id="3bfa3-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3bfa3-126">資料行</span><span class="sxs-lookup"><span data-stu-id="3bfa3-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3bfa3-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="3bfa3-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-128">可唯一識別合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="3bfa3-129">除非合併模組與其前身完全相容，否則兩個合併模組不能具有相同的 ModuleID。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="3bfa3-130">您可以使用 GUIDGEN 之類的公用程式來建立此欄位的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="3bfa3-131">ModuleID 資料行是資料表的主鍵，因此必須遵循命名慣例來 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="3bfa3-132">例如，如果合併模組的可讀取名稱是 MyLibrary，而 GUID 是 {880DE2F0-CDD8-11D1-A849-006097ABDE17}，則 ModuleID 資料行中的專案會變成 MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 A849 006097ABDE17 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言</span><span class="sxs-lookup"><span data-stu-id="3bfa3-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-134">語言識別項會指定合併模組的預設語言。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="3bfa3-135">語言識別項採用十進位格式，例如，美國英文為1033。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="3bfa3-136">合併模組所使用的語言可以藉由在合併之前套用轉換至合併模組來變更。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>版本</span><span class="sxs-lookup"><span data-stu-id="3bfa3-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-138">[版本] 欄位包含描述合併模組之主要和次要版本的字串。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="3bfa3-139">驗證</span><span class="sxs-lookup"><span data-stu-id="3bfa3-139">Validation</span></span>

<dl>

[<span data-ttu-id="3bfa3-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="3bfa3-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3bfa3-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="3bfa3-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3bfa3-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="3bfa3-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="3bfa3-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bfa3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bfa3-144">多個語言合併模組</span><span class="sxs-lookup"><span data-stu-id="3bfa3-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



