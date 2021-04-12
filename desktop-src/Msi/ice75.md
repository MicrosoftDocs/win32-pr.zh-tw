---
description: ICE75 會確認所有自訂動作類型 17 (DLL) 、自訂動作類型 18 (EXE) 、自訂動作類型 21 (JScript) 和自訂動作類型 22 (VBScript) 自訂動作會在 CostFinalize 動作之後排序。
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319919"
---
# <a name="ice75"></a><span data-ttu-id="0a865-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="0a865-103">ICE75</span></span>

<span data-ttu-id="0a865-104">ICE75 會確認所有 [自訂動作類型 17](custom-action-type-17.md) (DLL) 、 [自訂動作類型 18](custom-action-type-18.md) (EXE) 、 [自訂動作類型 21](custom-action-type-21.md) (JScript) 和 [自訂動作類型 22](custom-action-type-22.md) (VBScript) 自訂動作會在 [CostFinalize 動作](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="0a865-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0a865-105">這些類型的自訂動作會使用已安裝的檔案作為其來源。</span><span class="sxs-lookup"><span data-stu-id="0a865-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="0a865-106">ICE75 會檢查 [InstallUISequence 資料表](installuisequence-table.md)、 [InstallExecuteSequence 資料表](installexecutesequence-table.md)、 [AdminUISequence 資料表](adminuisequence-table.md)和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="0a865-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="0a865-107">請注意，這些順序資料表中必須要有 CostFinalize 動作。</span><span class="sxs-lookup"><span data-stu-id="0a865-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="0a865-108">結果</span><span class="sxs-lookup"><span data-stu-id="0a865-108">Result</span></span>

<span data-ttu-id="0a865-109">ICE75 會在使用已安裝的檔案做為原始程式檔（未在 CostFinalize 動作之後排序）找到自訂動作時張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="0a865-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="0a865-110">範例</span><span class="sxs-lookup"><span data-stu-id="0a865-110">Example</span></span>

<span data-ttu-id="0a865-111">ICE75 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="0a865-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="0a865-112">[CustomAction 資料表](customaction-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0a865-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="0a865-113">動作</span><span class="sxs-lookup"><span data-stu-id="0a865-113">Action</span></span>      | <span data-ttu-id="0a865-114">類型</span><span class="sxs-lookup"><span data-stu-id="0a865-114">Type</span></span> | <span data-ttu-id="0a865-115">來源</span><span class="sxs-lookup"><span data-stu-id="0a865-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="0a865-116">CA \_ FileExe</span><span class="sxs-lookup"><span data-stu-id="0a865-116">CA\_FileExe</span></span> | <span data-ttu-id="0a865-117">18</span><span class="sxs-lookup"><span data-stu-id="0a865-117">18</span></span>   | <span data-ttu-id="0a865-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="0a865-118">FileExe</span></span> |
| <span data-ttu-id="0a865-119">CA \_ FileDLL</span><span class="sxs-lookup"><span data-stu-id="0a865-119">CA\_FileDLL</span></span> | <span data-ttu-id="0a865-120">17</span><span class="sxs-lookup"><span data-stu-id="0a865-120">17</span></span>   | <span data-ttu-id="0a865-121">FileDLL</span><span class="sxs-lookup"><span data-stu-id="0a865-121">FileDLL</span></span> |



 

<span data-ttu-id="0a865-122">[AdminUISequence 資料表](adminuisequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0a865-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="0a865-123">動作</span><span class="sxs-lookup"><span data-stu-id="0a865-123">Action</span></span>      | <span data-ttu-id="0a865-124">順序</span><span class="sxs-lookup"><span data-stu-id="0a865-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="0a865-125">CA \_ FileExe</span><span class="sxs-lookup"><span data-stu-id="0a865-125">CA\_FileExe</span></span> | <span data-ttu-id="0a865-126">1100</span><span class="sxs-lookup"><span data-stu-id="0a865-126">1100</span></span>     |



 

<span data-ttu-id="0a865-127">[AdminExecuteSequence 資料表](adminexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0a865-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0a865-128">動作</span><span class="sxs-lookup"><span data-stu-id="0a865-128">Action</span></span>       | <span data-ttu-id="0a865-129">順序</span><span class="sxs-lookup"><span data-stu-id="0a865-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="0a865-130">CA \_ FileDLL</span><span class="sxs-lookup"><span data-stu-id="0a865-130">CA\_FileDLL</span></span>  | <span data-ttu-id="0a865-131">800</span><span class="sxs-lookup"><span data-stu-id="0a865-131">800</span></span>      |
| <span data-ttu-id="0a865-132">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="0a865-132">CostFinalize</span></span> | <span data-ttu-id="0a865-133">1000</span><span class="sxs-lookup"><span data-stu-id="0a865-133">1000</span></span>     |



 

<span data-ttu-id="0a865-134">若要修正錯誤，請在 CostFinalize 動作之後排列自訂動作的順序。</span><span class="sxs-lookup"><span data-stu-id="0a865-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a865-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a865-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a865-136">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="0a865-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



