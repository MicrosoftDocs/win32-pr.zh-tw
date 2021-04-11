---
description: ICE77 會確認 msidbCustomActionTypeInScript 位集的自訂動作是否會在 InstallInitialize 動作之後，以及 InstallFinalize 動作之前排序。
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113856"
---
# <a name="ice77"></a><span data-ttu-id="b150f-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="b150f-103">ICE77</span></span>

<span data-ttu-id="b150f-104">ICE77 會確認 **msidbCustomActionTypeInScript** 位集的自訂動作是否會在 [InstallInitialize 動作](installinitialize-action.md) 之後，以及 [InstallFinalize 動作](installfinalize-action.md)之前排序。</span><span class="sxs-lookup"><span data-stu-id="b150f-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="b150f-105">ICE77 會檢查 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)中的順序。</span><span class="sxs-lookup"><span data-stu-id="b150f-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="b150f-106">結果</span><span class="sxs-lookup"><span data-stu-id="b150f-106">Result</span></span>

<span data-ttu-id="b150f-107">如果腳本內自訂動作是在 InstallInitialize 動作之前或 InstallFinalize 動作之後排序，ICE77 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="b150f-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="b150f-108">ICE77 會在 InstallInitialize 動作或 InstallFinalize 動作遺失時張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="b150f-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="b150f-109">範例</span><span class="sxs-lookup"><span data-stu-id="b150f-109">Example</span></span>

<span data-ttu-id="b150f-110">ICE77 會報告範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="b150f-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="b150f-111">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b150f-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="b150f-112">動作</span><span class="sxs-lookup"><span data-stu-id="b150f-112">Action</span></span>              | <span data-ttu-id="b150f-113">類型</span><span class="sxs-lookup"><span data-stu-id="b150f-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="b150f-114">CA \_ InScriptInstall</span><span class="sxs-lookup"><span data-stu-id="b150f-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="b150f-115">1025</span><span class="sxs-lookup"><span data-stu-id="b150f-115">1025</span></span> |
| <span data-ttu-id="b150f-116">CA \_ InScriptAdmin</span><span class="sxs-lookup"><span data-stu-id="b150f-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="b150f-117">1026</span><span class="sxs-lookup"><span data-stu-id="b150f-117">1026</span></span> |



 

<span data-ttu-id="b150f-118">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b150f-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="b150f-119">動作</span><span class="sxs-lookup"><span data-stu-id="b150f-119">Action</span></span>              | <span data-ttu-id="b150f-120">順序</span><span class="sxs-lookup"><span data-stu-id="b150f-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="b150f-121">CA \_ InScriptInstall</span><span class="sxs-lookup"><span data-stu-id="b150f-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="b150f-122">2000</span><span class="sxs-lookup"><span data-stu-id="b150f-122">2000</span></span>     |
| <span data-ttu-id="b150f-123">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="b150f-123">InstallInitialize</span></span>   | <span data-ttu-id="b150f-124">1500</span><span class="sxs-lookup"><span data-stu-id="b150f-124">1500</span></span>     |



 

<span data-ttu-id="b150f-125">[AdminExecuteSequence 資料表](adminexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b150f-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="b150f-126">動作</span><span class="sxs-lookup"><span data-stu-id="b150f-126">Action</span></span>            | <span data-ttu-id="b150f-127">順序</span><span class="sxs-lookup"><span data-stu-id="b150f-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="b150f-128">CA \_ InScriptAdmin</span><span class="sxs-lookup"><span data-stu-id="b150f-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="b150f-129">1400</span><span class="sxs-lookup"><span data-stu-id="b150f-129">1400</span></span>     |
| <span data-ttu-id="b150f-130">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="b150f-130">InstallInitialize</span></span> | <span data-ttu-id="b150f-131">1500</span><span class="sxs-lookup"><span data-stu-id="b150f-131">1500</span></span>     |
| <span data-ttu-id="b150f-132">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="b150f-132">InstallFinalize</span></span>   | <span data-ttu-id="b150f-133">6600</span><span class="sxs-lookup"><span data-stu-id="b150f-133">6600</span></span>     |



 

<span data-ttu-id="b150f-134">若要修正錯誤，請在 InstallInitialize 動作之後以及 InstallFinalize 動作之前，將腳本內自訂動作排序。</span><span class="sxs-lookup"><span data-stu-id="b150f-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="b150f-135">InstallInitialize 和 InstallFinalize 動作必須存在於 InstallExecuteSequence 資料表和 AdminExecuteSequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="b150f-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b150f-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="b150f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b150f-137">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b150f-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



