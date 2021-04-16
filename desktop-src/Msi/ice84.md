---
description: ICE84 會檢查 AdvtExecuteSequence 資料表、AdminExecuteSequence 資料表和 InstallExecuteSequence 資料表，以確認未在條件欄位中設定條件的下列標準動作。
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320087"
---
# <a name="ice84"></a><span data-ttu-id="8f6b2-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="8f6b2-103">ICE84</span></span>

<span data-ttu-id="8f6b2-104">ICE84 會檢查 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)、 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)和 [InstallExecuteSequence 資料表](installexecutesequence-table.md) ，以確認未在條件欄位中設定條件的下列 [標準動作](standard-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="8f6b2-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="8f6b2-105">CostInitialize 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="8f6b2-106">CostFinalize 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="8f6b2-107">FileCost 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="8f6b2-108">InstallValidate 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="8f6b2-109">InstallInitialize 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="8f6b2-110">InstallFinalize 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="8f6b2-111">ProcessComponents 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="8f6b2-112">PublishFeatures 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="8f6b2-113">PublishProduct 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="8f6b2-114">RegisterProduct 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="8f6b2-115">UnpublishFeatures 動作</span><span class="sxs-lookup"><span data-stu-id="8f6b2-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="8f6b2-116">如果找到條件，ICE84 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="8f6b2-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="8f6b2-117">結果</span><span class="sxs-lookup"><span data-stu-id="8f6b2-117">Result</span></span>

<span data-ttu-id="8f6b2-118">ICE84 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="8f6b2-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="8f6b2-119">ICE84 錯誤</span><span class="sxs-lookup"><span data-stu-id="8f6b2-119">ICE84 error</span></span>                                                             | <span data-ttu-id="8f6b2-120">Description</span><span class="sxs-lookup"><span data-stu-id="8f6b2-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8f6b2-121">\[ \] 在% s 資料表中找到的動作 ' 1 ' 是具有條件的必要動作。</span><span class="sxs-lookup"><span data-stu-id="8f6b2-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="8f6b2-122">已使用條件撰寫必要的動作。</span><span class="sxs-lookup"><span data-stu-id="8f6b2-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8f6b2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f6b2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6b2-124">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="8f6b2-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



