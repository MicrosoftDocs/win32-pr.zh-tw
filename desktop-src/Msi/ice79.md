---
description: ICE79 會使用 Condition 資料類型來驗證資料庫欄位中所輸入之元件和功能的參考。
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113849"
---
# <a name="ice79"></a><span data-ttu-id="06f07-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="06f07-103">ICE79</span></span>

<span data-ttu-id="06f07-104">ICE79 會使用 [Condition](condition.md) 資料類型來驗證資料庫欄位中所輸入之元件和功能的參考。</span><span class="sxs-lookup"><span data-stu-id="06f07-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="06f07-105">結果</span><span class="sxs-lookup"><span data-stu-id="06f07-105">Result</span></span>

<span data-ttu-id="06f07-106">ICE79 會發佈兩個警告。</span><span class="sxs-lookup"><span data-stu-id="06f07-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="06f07-107">ICE79 警告</span><span class="sxs-lookup"><span data-stu-id="06f07-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="06f07-108">Description</span><span class="sxs-lookup"><span data-stu-id="06f07-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="06f07-109">資料庫缺少 \_ 驗證資料表。</span><span class="sxs-lookup"><span data-stu-id="06f07-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="06f07-110">無法完全檢查屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="06f07-110">Could not completely check property names.</span></span> | <span data-ttu-id="06f07-111">資料庫缺少[ \_ 驗證資料表](-validation-table.md)。</span><span class="sxs-lookup"><span data-stu-id="06f07-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="06f07-112">從 \[ \] 表1中的資料行2取出值時發生錯誤 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="06f07-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="06f07-113">略過資料行。</span><span class="sxs-lookup"><span data-stu-id="06f07-113">Skipping Column.</span></span>         | <span data-ttu-id="06f07-114">抓取值時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06f07-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="06f07-115">ICE79 會張貼兩個錯誤。</span><span class="sxs-lookup"><span data-stu-id="06f07-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="06f07-116">ICE79 錯誤</span><span class="sxs-lookup"><span data-stu-id="06f07-116">ICE79 error</span></span>                                                          | <span data-ttu-id="06f07-117">Description</span><span class="sxs-lookup"><span data-stu-id="06f07-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="06f07-118">在資料行 '% s ' 中參考的元件 '% ls '。% s ' 的資料列% s 無效。</span><span class="sxs-lookup"><span data-stu-id="06f07-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="06f07-119">找到不正確元件參考。</span><span class="sxs-lookup"><span data-stu-id="06f07-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="06f07-120">在資料行 '% s ' 中參考的功能 '% ls '。% s ' 的資料列% s 無效。</span><span class="sxs-lookup"><span data-stu-id="06f07-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="06f07-121">找到不正確功能參考</span><span class="sxs-lookup"><span data-stu-id="06f07-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="06f07-122">範例</span><span class="sxs-lookup"><span data-stu-id="06f07-122">Example</span></span>

<span data-ttu-id="06f07-123">ICE79 會報告範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="06f07-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="06f07-124">在此範例中， [元件資料表](component-table.md) 中的 NoSuchComponent 不存在，而且 [功能資料表](feature-table.md)中沒有 NoSuchFeature。</span><span class="sxs-lookup"><span data-stu-id="06f07-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="06f07-125">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="06f07-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="06f07-126">動作</span><span class="sxs-lookup"><span data-stu-id="06f07-126">Action</span></span>  | <span data-ttu-id="06f07-127">條件</span><span class="sxs-lookup"><span data-stu-id="06f07-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="06f07-128">Custom1</span><span class="sxs-lookup"><span data-stu-id="06f07-128">Custom1</span></span> | <span data-ttu-id="06f07-129">TESTACTION = 1046 和 &NoSuchFeature>2</span><span class="sxs-lookup"><span data-stu-id="06f07-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="06f07-130">Custom2</span><span class="sxs-lookup"><span data-stu-id="06f07-130">Custom2</span></span> | <span data-ttu-id="06f07-131">TESTACTION = 146 和 $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="06f07-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="06f07-132">若要修正這些錯誤，請在功能和元件資料表中輸入 NoSuchFeature 和 NoSuchComponent 的有效記錄。</span><span class="sxs-lookup"><span data-stu-id="06f07-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f07-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="06f07-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06f07-134">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="06f07-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



