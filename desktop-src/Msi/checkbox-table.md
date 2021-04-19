---
description: 核取方塊表格會列出核取方塊的值。
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: 核取方塊表格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986886"
---
# <a name="checkbox-table"></a><span data-ttu-id="31cfd-103">核取方塊表格</span><span class="sxs-lookup"><span data-stu-id="31cfd-103">CheckBox Table</span></span>

<span data-ttu-id="31cfd-104">核取方塊表格會列出核取方塊的值。</span><span class="sxs-lookup"><span data-stu-id="31cfd-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="31cfd-105">CheckBox 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="31cfd-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="31cfd-106">Column</span><span class="sxs-lookup"><span data-stu-id="31cfd-106">Column</span></span>   | <span data-ttu-id="31cfd-107">類型</span><span class="sxs-lookup"><span data-stu-id="31cfd-107">Type</span></span>                         | <span data-ttu-id="31cfd-108">答案</span><span class="sxs-lookup"><span data-stu-id="31cfd-108">Key</span></span> | <span data-ttu-id="31cfd-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="31cfd-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="31cfd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="31cfd-110">Property</span></span> | [<span data-ttu-id="31cfd-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="31cfd-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="31cfd-112">Y</span><span class="sxs-lookup"><span data-stu-id="31cfd-112">Y</span></span>   | <span data-ttu-id="31cfd-113">N</span><span class="sxs-lookup"><span data-stu-id="31cfd-113">N</span></span>        |
| <span data-ttu-id="31cfd-114">值</span><span class="sxs-lookup"><span data-stu-id="31cfd-114">Value</span></span>    | [<span data-ttu-id="31cfd-115">格式 化</span><span class="sxs-lookup"><span data-stu-id="31cfd-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="31cfd-116">N</span><span class="sxs-lookup"><span data-stu-id="31cfd-116">N</span></span>   | <span data-ttu-id="31cfd-117">Y</span><span class="sxs-lookup"><span data-stu-id="31cfd-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="31cfd-118">資料行</span><span class="sxs-lookup"><span data-stu-id="31cfd-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="31cfd-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="31cfd-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="31cfd-120">要系結至這個專案的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="31cfd-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="31cfd-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="31cfd-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="31cfd-122">與這個專案相關聯的值字串。</span><span class="sxs-lookup"><span data-stu-id="31cfd-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31cfd-123">備註</span><span class="sxs-lookup"><span data-stu-id="31cfd-123">Remarks</span></span>

<span data-ttu-id="31cfd-124">如果選取此核取方塊，則對應的屬性會設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="31cfd-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="31cfd-125">如果未指定任何值，或此資料表不存在，則在選取核取方塊時，屬性會設定為其原始值。</span><span class="sxs-lookup"><span data-stu-id="31cfd-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="31cfd-126">如果原始值為 null，則屬性會設定為 "1"。</span><span class="sxs-lookup"><span data-stu-id="31cfd-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="31cfd-127">當建立控制項時， [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 函式會格式化 Value 資料行的內容。</span><span class="sxs-lookup"><span data-stu-id="31cfd-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="31cfd-128">因此，它可以包含 **MsiFormatRecord** 函數可解讀的任何運算式。</span><span class="sxs-lookup"><span data-stu-id="31cfd-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="31cfd-129">只有在建立控制項時，才會格式化 Value 資料行，而且如果在控制項的存留期內修改了包含在運算式中的屬性，則不會更新此資料行。</span><span class="sxs-lookup"><span data-stu-id="31cfd-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="31cfd-130">驗證</span><span class="sxs-lookup"><span data-stu-id="31cfd-130">Validation</span></span>

<dl>

[<span data-ttu-id="31cfd-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="31cfd-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="31cfd-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="31cfd-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="31cfd-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="31cfd-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



