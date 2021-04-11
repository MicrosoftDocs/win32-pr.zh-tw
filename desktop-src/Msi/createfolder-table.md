---
description: CreateFolder 資料表包含需要針對特定元件明確建立之資料夾的參考。
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193921"
---
# <a name="createfolder-table"></a><span data-ttu-id="87417-103">CreateFolder 資料表</span><span class="sxs-lookup"><span data-stu-id="87417-103">CreateFolder Table</span></span>

<span data-ttu-id="87417-104">CreateFolder 資料表包含需要針對特定元件明確建立之資料夾的參考。</span><span class="sxs-lookup"><span data-stu-id="87417-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="87417-105">CreateFolder 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="87417-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="87417-106">Column</span><span class="sxs-lookup"><span data-stu-id="87417-106">Column</span></span>      | <span data-ttu-id="87417-107">類型</span><span class="sxs-lookup"><span data-stu-id="87417-107">Type</span></span>                         | <span data-ttu-id="87417-108">答案</span><span class="sxs-lookup"><span data-stu-id="87417-108">Key</span></span> | <span data-ttu-id="87417-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="87417-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="87417-110">目錄\_</span><span class="sxs-lookup"><span data-stu-id="87417-110">Directory\_</span></span> | [<span data-ttu-id="87417-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="87417-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="87417-112">Y</span><span class="sxs-lookup"><span data-stu-id="87417-112">Y</span></span>   | <span data-ttu-id="87417-113">N</span><span class="sxs-lookup"><span data-stu-id="87417-113">N</span></span>        |
| <span data-ttu-id="87417-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="87417-114">Component\_</span></span> | [<span data-ttu-id="87417-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="87417-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="87417-116">Y</span><span class="sxs-lookup"><span data-stu-id="87417-116">Y</span></span>   | <span data-ttu-id="87417-117">N</span><span class="sxs-lookup"><span data-stu-id="87417-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="87417-118">資料行</span><span class="sxs-lookup"><span data-stu-id="87417-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="87417-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_</span><span class="sxs-lookup"><span data-stu-id="87417-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="87417-120">在 [目錄資料表](directory-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="87417-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="87417-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="87417-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="87417-122">在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="87417-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87417-123">備註</span><span class="sxs-lookup"><span data-stu-id="87417-123">Remarks</span></span>

<span data-ttu-id="87417-124">安裝元件時，會建立此資料表中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="87417-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="87417-125">只有在元件已卸載或移至從來源執行時，才會嘗試移除這些資料夾。</span><span class="sxs-lookup"><span data-stu-id="87417-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="87417-126">如果資料夾變成空白，則不會觸發自動移除。</span><span class="sxs-lookup"><span data-stu-id="87417-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="87417-127">相反地，安裝程式所建立但未列在此資料表中的資料夾，會在它們變成空白時移除。</span><span class="sxs-lookup"><span data-stu-id="87417-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="87417-128">因為安裝程式所建立的資料夾是空的，所以您必須在 CreateFolder 資料表中撰寫一個專案，才能安裝包含空資料夾的元件。</span><span class="sxs-lookup"><span data-stu-id="87417-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="87417-129">當呼叫 [CreateFolders](createfolders-action.md) 動作或 [RemoveFolders](removefolders-action.md) 動作時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="87417-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="87417-130">如需如何保護資料夾的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) 和 [LockPermissions 資料表](lockpermissions-table.md)。</span><span class="sxs-lookup"><span data-stu-id="87417-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="87417-131">驗證</span><span class="sxs-lookup"><span data-stu-id="87417-131">Validation</span></span>

<dl>

[<span data-ttu-id="87417-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="87417-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="87417-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="87417-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="87417-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="87417-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="87417-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="87417-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="87417-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="87417-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



