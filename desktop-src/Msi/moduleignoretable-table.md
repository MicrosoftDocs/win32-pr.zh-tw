---
description: 如果 merge 模組中的資料表列在 ModuleIgnoreTable 資料表中，它就不會合並到 .msi 檔案中。
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: ModuleIgnoreTable 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194748"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="17eef-103">ModuleIgnoreTable 資料表</span><span class="sxs-lookup"><span data-stu-id="17eef-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="17eef-104">如果 merge 模組中的資料表列在 ModuleIgnoreTable 資料表中，它就不會合並到 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="17eef-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="17eef-105">如果資料表已經存在於 .msi 檔案中，則合併不會修改它。</span><span class="sxs-lookup"><span data-stu-id="17eef-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="17eef-106">因此，ModuleIgnoreTable 中的資料表可能包含合併後不需要的資料。</span><span class="sxs-lookup"><span data-stu-id="17eef-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="17eef-107">ModuleIgnoreTable 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="17eef-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="17eef-108">Column</span><span class="sxs-lookup"><span data-stu-id="17eef-108">Column</span></span> | <span data-ttu-id="17eef-109">類型</span><span class="sxs-lookup"><span data-stu-id="17eef-109">Type</span></span>                         | <span data-ttu-id="17eef-110">答案</span><span class="sxs-lookup"><span data-stu-id="17eef-110">Key</span></span> | <span data-ttu-id="17eef-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="17eef-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="17eef-112">資料表</span><span class="sxs-lookup"><span data-stu-id="17eef-112">Table</span></span>  | [<span data-ttu-id="17eef-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="17eef-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="17eef-114">Y</span><span class="sxs-lookup"><span data-stu-id="17eef-114">Y</span></span>   | <span data-ttu-id="17eef-115">否</span><span class="sxs-lookup"><span data-stu-id="17eef-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="17eef-116">資料行</span><span class="sxs-lookup"><span data-stu-id="17eef-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="17eef-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="17eef-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="17eef-118">合併模組中不會合並到 .msi 檔案中的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="17eef-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17eef-119">備註</span><span class="sxs-lookup"><span data-stu-id="17eef-119">Remarks</span></span>

<span data-ttu-id="17eef-120">若要將 .msm 檔案的大小降到最低，建議開發人員從用於轉散發的模組中移除未使用的資料表，而不是在 ModuleIgnoreTable 資料表中列出這些資料表。</span><span class="sxs-lookup"><span data-stu-id="17eef-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



