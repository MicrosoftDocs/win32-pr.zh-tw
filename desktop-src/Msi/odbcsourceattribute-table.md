---
description: ODBCSourceAttribute 資料表包含資料來源屬性的相關資訊。
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: ODBCSourceAttribute 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511186"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="19fd0-103">ODBCSourceAttribute 資料表</span><span class="sxs-lookup"><span data-stu-id="19fd0-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="19fd0-104">ODBCSourceAttribute 資料表包含資料來源屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="19fd0-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="19fd0-105">ODBCSourceAttribute 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="19fd0-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="19fd0-106">Column</span><span class="sxs-lookup"><span data-stu-id="19fd0-106">Column</span></span>       | <span data-ttu-id="19fd0-107">類型</span><span class="sxs-lookup"><span data-stu-id="19fd0-107">Type</span></span>                         | <span data-ttu-id="19fd0-108">答案</span><span class="sxs-lookup"><span data-stu-id="19fd0-108">Key</span></span> | <span data-ttu-id="19fd0-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="19fd0-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="19fd0-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="19fd0-110">DataSource\_</span></span> | [<span data-ttu-id="19fd0-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="19fd0-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="19fd0-112">Y</span><span class="sxs-lookup"><span data-stu-id="19fd0-112">Y</span></span>   | <span data-ttu-id="19fd0-113">N</span><span class="sxs-lookup"><span data-stu-id="19fd0-113">N</span></span>        |
| <span data-ttu-id="19fd0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="19fd0-114">Attribute</span></span>    | [<span data-ttu-id="19fd0-115">Text</span><span class="sxs-lookup"><span data-stu-id="19fd0-115">Text</span></span>](text.md)             | <span data-ttu-id="19fd0-116">Y</span><span class="sxs-lookup"><span data-stu-id="19fd0-116">Y</span></span>   | <span data-ttu-id="19fd0-117">N</span><span class="sxs-lookup"><span data-stu-id="19fd0-117">N</span></span>        |
| <span data-ttu-id="19fd0-118">值</span><span class="sxs-lookup"><span data-stu-id="19fd0-118">Value</span></span>        | [<span data-ttu-id="19fd0-119">格式 化</span><span class="sxs-lookup"><span data-stu-id="19fd0-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="19fd0-120">N</span><span class="sxs-lookup"><span data-stu-id="19fd0-120">N</span></span>   | <span data-ttu-id="19fd0-121">Y</span><span class="sxs-lookup"><span data-stu-id="19fd0-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="19fd0-122">資料行</span><span class="sxs-lookup"><span data-stu-id="19fd0-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="19fd0-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>資料來源\_</span><span class="sxs-lookup"><span data-stu-id="19fd0-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="19fd0-124">資料來源的內部 token 名稱。</span><span class="sxs-lookup"><span data-stu-id="19fd0-124">Internal token name for data source.</span></span> <span data-ttu-id="19fd0-125">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="19fd0-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="19fd0-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="19fd0-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="19fd0-127">資料來源屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="19fd0-127">Name of data source attribute.</span></span> <span data-ttu-id="19fd0-128">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="19fd0-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="19fd0-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="19fd0-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="19fd0-130">屬性的可當地語系化字串值。</span><span class="sxs-lookup"><span data-stu-id="19fd0-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19fd0-131">備註</span><span class="sxs-lookup"><span data-stu-id="19fd0-131">Remarks</span></span>

<span data-ttu-id="19fd0-132">[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="19fd0-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="19fd0-133">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="19fd0-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="19fd0-134">驗證</span><span class="sxs-lookup"><span data-stu-id="19fd0-134">Validation</span></span>

<dl>

[<span data-ttu-id="19fd0-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="19fd0-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="19fd0-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="19fd0-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="19fd0-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="19fd0-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="19fd0-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="19fd0-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



