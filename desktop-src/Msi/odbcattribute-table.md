---
description: ODBCAttribute 資料表包含 (ODBC) 驅動程式和轉譯程式之開放式資料庫連接的屬性相關資訊。
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: ODBCAttribute 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114169"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="d7b01-103">ODBCAttribute 資料表</span><span class="sxs-lookup"><span data-stu-id="d7b01-103">ODBCAttribute Table</span></span>

<span data-ttu-id="d7b01-104">ODBCAttribute 資料表包含 (ODBC) 驅動程式和轉譯程式之開放式資料庫連接的屬性相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d7b01-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="d7b01-105">ODBCAttribute 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="d7b01-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="d7b01-106">Column</span><span class="sxs-lookup"><span data-stu-id="d7b01-106">Column</span></span>    | <span data-ttu-id="d7b01-107">類型</span><span class="sxs-lookup"><span data-stu-id="d7b01-107">Type</span></span>                         | <span data-ttu-id="d7b01-108">答案</span><span class="sxs-lookup"><span data-stu-id="d7b01-108">Key</span></span> | <span data-ttu-id="d7b01-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d7b01-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="d7b01-110">驅動程式\_</span><span class="sxs-lookup"><span data-stu-id="d7b01-110">Driver\_</span></span>  | [<span data-ttu-id="d7b01-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="d7b01-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d7b01-112">Y</span><span class="sxs-lookup"><span data-stu-id="d7b01-112">Y</span></span>   | <span data-ttu-id="d7b01-113">N</span><span class="sxs-lookup"><span data-stu-id="d7b01-113">N</span></span>        |
| <span data-ttu-id="d7b01-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d7b01-114">Attribute</span></span> | [<span data-ttu-id="d7b01-115">Text</span><span class="sxs-lookup"><span data-stu-id="d7b01-115">Text</span></span>](text.md)             | <span data-ttu-id="d7b01-116">Y</span><span class="sxs-lookup"><span data-stu-id="d7b01-116">Y</span></span>   | <span data-ttu-id="d7b01-117">N</span><span class="sxs-lookup"><span data-stu-id="d7b01-117">N</span></span>        |
| <span data-ttu-id="d7b01-118">值</span><span class="sxs-lookup"><span data-stu-id="d7b01-118">Value</span></span>     | [<span data-ttu-id="d7b01-119">格式 化</span><span class="sxs-lookup"><span data-stu-id="d7b01-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d7b01-120">N</span><span class="sxs-lookup"><span data-stu-id="d7b01-120">N</span></span>   | <span data-ttu-id="d7b01-121">Y</span><span class="sxs-lookup"><span data-stu-id="d7b01-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d7b01-122">資料行</span><span class="sxs-lookup"><span data-stu-id="d7b01-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d7b01-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>司機\_</span><span class="sxs-lookup"><span data-stu-id="d7b01-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="d7b01-124">驅動程式的內部權杖名稱。</span><span class="sxs-lookup"><span data-stu-id="d7b01-124">Internal token name for a driver.</span></span> <span data-ttu-id="d7b01-125">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="d7b01-125">A primary key for the table.</span></span> <span data-ttu-id="d7b01-126">[ODBCDriver 資料表](odbcdriver-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="d7b01-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7b01-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="d7b01-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="d7b01-128">驅動程式屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7b01-128">Name of the driver attribute.</span></span> <span data-ttu-id="d7b01-129">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="d7b01-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="d7b01-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="d7b01-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d7b01-131">屬性的可當地語系化字串值。</span><span class="sxs-lookup"><span data-stu-id="d7b01-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7b01-132">備註</span><span class="sxs-lookup"><span data-stu-id="d7b01-132">Remarks</span></span>

<span data-ttu-id="d7b01-133">[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="d7b01-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="d7b01-134">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d7b01-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d7b01-135">驗證</span><span class="sxs-lookup"><span data-stu-id="d7b01-135">Validation</span></span>

<dl>

[<span data-ttu-id="d7b01-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="d7b01-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d7b01-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="d7b01-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d7b01-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="d7b01-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d7b01-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="d7b01-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



