---
description: ModuleComponents 資料表包含在合併模組中找到的元件清單。
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: ModuleComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981199"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="ae357-103">ModuleComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="ae357-103">ModuleComponents Table</span></span>

<span data-ttu-id="ae357-104">ModuleComponents 資料表包含在合併模組中找到的元件清單。</span><span class="sxs-lookup"><span data-stu-id="ae357-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="ae357-105">ModuleComponents 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="ae357-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="ae357-106">Column</span><span class="sxs-lookup"><span data-stu-id="ae357-106">Column</span></span>    | <span data-ttu-id="ae357-107">類型</span><span class="sxs-lookup"><span data-stu-id="ae357-107">Type</span></span>                         | <span data-ttu-id="ae357-108">答案</span><span class="sxs-lookup"><span data-stu-id="ae357-108">Key</span></span> | <span data-ttu-id="ae357-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ae357-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ae357-110">元件</span><span class="sxs-lookup"><span data-stu-id="ae357-110">Component</span></span> | [<span data-ttu-id="ae357-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="ae357-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ae357-112">Y</span><span class="sxs-lookup"><span data-stu-id="ae357-112">Y</span></span>   | <span data-ttu-id="ae357-113">N</span><span class="sxs-lookup"><span data-stu-id="ae357-113">N</span></span>        |
| <span data-ttu-id="ae357-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="ae357-114">ModuleID</span></span>  | [<span data-ttu-id="ae357-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="ae357-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ae357-116">Y</span><span class="sxs-lookup"><span data-stu-id="ae357-116">Y</span></span>   | <span data-ttu-id="ae357-117">N</span><span class="sxs-lookup"><span data-stu-id="ae357-117">N</span></span>        |
| <span data-ttu-id="ae357-118">語言</span><span class="sxs-lookup"><span data-stu-id="ae357-118">Language</span></span>  | [<span data-ttu-id="ae357-119">整數</span><span class="sxs-lookup"><span data-stu-id="ae357-119">Integer</span></span>](integer.md)       | <span data-ttu-id="ae357-120">Y</span><span class="sxs-lookup"><span data-stu-id="ae357-120">Y</span></span>   | <span data-ttu-id="ae357-121">N</span><span class="sxs-lookup"><span data-stu-id="ae357-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ae357-122">資料行</span><span class="sxs-lookup"><span data-stu-id="ae357-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ae357-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>元件</span><span class="sxs-lookup"><span data-stu-id="ae357-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="ae357-124">參考合併模組中元件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae357-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="ae357-125">元件資料行是 [元件資料表](component-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="ae357-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="ae357-126">元件資料行中的專案必須遵循命名慣例，以 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="ae357-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae357-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="ae357-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="ae357-128">合併模組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae357-128">The identifier for the merge module.</span></span> <span data-ttu-id="ae357-129">這是 [ModuleSignature 資料表](modulesignature-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="ae357-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae357-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言</span><span class="sxs-lookup"><span data-stu-id="ae357-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="ae357-131">語言識別項描述合併模組的預設語言。</span><span class="sxs-lookup"><span data-stu-id="ae357-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="ae357-132">語言識別項採用十進位格式，例如，美國英文為1033。</span><span class="sxs-lookup"><span data-stu-id="ae357-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="ae357-133">[ModuleSignature 資料表](modulesignature-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="ae357-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae357-134">備註</span><span class="sxs-lookup"><span data-stu-id="ae357-134">Remarks</span></span>

<span data-ttu-id="ae357-135">如果合併模組支援多種語言，則語言轉換必須能夠更新此資料表。</span><span class="sxs-lookup"><span data-stu-id="ae357-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



