---
description: LaunchConditions 動作會使用 LaunchCondition 資料表。 它包含一份條件清單，必須滿足這些條件才能開始安裝。
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: LaunchCondition 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991824"
---
# <a name="launchcondition-table"></a><span data-ttu-id="55505-104">LaunchCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="55505-104">LaunchCondition Table</span></span>

<span data-ttu-id="55505-105">[LaunchConditions 動作](launchconditions-action.md)會使用 LaunchCondition 資料表。</span><span class="sxs-lookup"><span data-stu-id="55505-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="55505-106">它包含一份條件清單，必須滿足這些條件才能開始安裝。</span><span class="sxs-lookup"><span data-stu-id="55505-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="55505-107">LaunchCondition 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="55505-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="55505-108">Column</span><span class="sxs-lookup"><span data-stu-id="55505-108">Column</span></span>      | <span data-ttu-id="55505-109">類型</span><span class="sxs-lookup"><span data-stu-id="55505-109">Type</span></span>                       | <span data-ttu-id="55505-110">答案</span><span class="sxs-lookup"><span data-stu-id="55505-110">Key</span></span> | <span data-ttu-id="55505-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="55505-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="55505-112">條件</span><span class="sxs-lookup"><span data-stu-id="55505-112">Condition</span></span>   | [<span data-ttu-id="55505-113">Condition</span><span class="sxs-lookup"><span data-stu-id="55505-113">Condition</span></span>](condition.md) | <span data-ttu-id="55505-114">Y</span><span class="sxs-lookup"><span data-stu-id="55505-114">Y</span></span>   | <span data-ttu-id="55505-115">N</span><span class="sxs-lookup"><span data-stu-id="55505-115">N</span></span>        |
| <span data-ttu-id="55505-116">Description</span><span class="sxs-lookup"><span data-stu-id="55505-116">Description</span></span> | [<span data-ttu-id="55505-117">格式 化</span><span class="sxs-lookup"><span data-stu-id="55505-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="55505-118">N</span><span class="sxs-lookup"><span data-stu-id="55505-118">N</span></span>   | <span data-ttu-id="55505-119">N</span><span class="sxs-lookup"><span data-stu-id="55505-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="55505-120">資料行</span><span class="sxs-lookup"><span data-stu-id="55505-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="55505-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="55505-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="55505-122">必須評估為 True 的運算式，才能開始安裝。</span><span class="sxs-lookup"><span data-stu-id="55505-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="55505-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="55505-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="55505-124">當條件失敗且必須終止安裝時，可顯示的可當地語系化文字。</span><span class="sxs-lookup"><span data-stu-id="55505-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55505-125">備註</span><span class="sxs-lookup"><span data-stu-id="55505-125">Remarks</span></span>

<span data-ttu-id="55505-126">您無法保證藉由撰寫此資料表來評估啟動條件的順序。</span><span class="sxs-lookup"><span data-stu-id="55505-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="55505-127">如果需要控制評估條件的順序，您應該在安裝中使用自訂動作類型19自訂動作來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="55505-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="55505-128">驗證</span><span class="sxs-lookup"><span data-stu-id="55505-128">Validation</span></span>

<dl>

[<span data-ttu-id="55505-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="55505-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="55505-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="55505-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="55505-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="55505-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="55505-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="55505-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="55505-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="55505-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



