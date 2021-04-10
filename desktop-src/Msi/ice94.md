---
description: ICE94 會檢查快速鍵資料表、功能資料表和 MsiAssembly 資料表，如果有任何 unadvertised 快速鍵指向全域組件快取中的元件檔案，則會張貼警告。
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194395"
---
# <a name="ice94"></a><span data-ttu-id="ff408-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="ff408-103">ICE94</span></span>

<span data-ttu-id="ff408-104">ICE94 會檢查 [快速鍵資料表](shortcut-table.md)、 [功能資料表](feature-table.md)和 [MsiAssembly 資料表](msiassembly-table.md) ，如果有任何 unadvertised 快速鍵指向全域組件快取中的元件檔案，則會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="ff408-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="ff408-105">如果快速鍵資料表的 [目標] 欄位中的專案不是功能資料表中的一項功能，則會 unadvertised 快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ff408-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="ff408-106">如果快速鍵資料表之 [元件] 欄位中的專案 \_ 也列在 [MsiAssembly] 資料表中，快捷方式會指向元件檔案。</span><span class="sxs-lookup"><span data-stu-id="ff408-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="ff408-107">如果 MsiAssembly 資料表的 [檔案 \_ 應用程式] 欄位中的專案是空的，則元件檔會在全域組件快取中。</span><span class="sxs-lookup"><span data-stu-id="ff408-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="ff408-108">結果</span><span class="sxs-lookup"><span data-stu-id="ff408-108">Result</span></span>

<span data-ttu-id="ff408-109">ICE94 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="ff408-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="ff408-110">ICE94 警告</span><span class="sxs-lookup"><span data-stu-id="ff408-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="ff408-111">Description</span><span class="sxs-lookup"><span data-stu-id="ff408-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff408-112">未公告的快捷方式 ' \[ 2 \] ' 會指向全域組件快取中的元件檔案。</span><span class="sxs-lookup"><span data-stu-id="ff408-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="ff408-113">Unadvertised 快捷方式指向全域組件快取中的元件檔案。</span><span class="sxs-lookup"><span data-stu-id="ff408-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="ff408-114">範例</span><span class="sxs-lookup"><span data-stu-id="ff408-114">Example</span></span>

<span data-ttu-id="ff408-115">ICE94 會報告此範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="ff408-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="ff408-116"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="ff408-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="ff408-117">快速鍵</span><span class="sxs-lookup"><span data-stu-id="ff408-117">Shortcut</span></span>  | <span data-ttu-id="ff408-118">元件\_</span><span class="sxs-lookup"><span data-stu-id="ff408-118">Component\_</span></span> | <span data-ttu-id="ff408-119">目標</span><span class="sxs-lookup"><span data-stu-id="ff408-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="ff408-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="ff408-120">shortcut1</span></span> | <span data-ttu-id="ff408-121">c1</span><span class="sxs-lookup"><span data-stu-id="ff408-121">c1</span></span>          | <span data-ttu-id="ff408-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ff408-122">\[file1\]</span></span> |
| <span data-ttu-id="ff408-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="ff408-123">shortcut2</span></span> | <span data-ttu-id="ff408-124">c2</span><span class="sxs-lookup"><span data-stu-id="ff408-124">c2</span></span>          | <span data-ttu-id="ff408-125">feature1</span><span class="sxs-lookup"><span data-stu-id="ff408-125">feature1</span></span>  |
| <span data-ttu-id="ff408-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="ff408-126">shortcut3</span></span> | <span data-ttu-id="ff408-127">c3</span><span class="sxs-lookup"><span data-stu-id="ff408-127">c3</span></span>          | <span data-ttu-id="ff408-128">\[file2\]</span><span class="sxs-lookup"><span data-stu-id="ff408-128">\[file2\]</span></span> |



 

<span data-ttu-id="ff408-129">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="ff408-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="ff408-130">功能</span><span class="sxs-lookup"><span data-stu-id="ff408-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="ff408-131">feature1</span><span class="sxs-lookup"><span data-stu-id="ff408-131">feature1</span></span> |



 

<span data-ttu-id="ff408-132">[MsiAssembly 資料表](msiassembly-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="ff408-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="ff408-133">元件\_</span><span class="sxs-lookup"><span data-stu-id="ff408-133">Component\_</span></span> | <span data-ttu-id="ff408-134">檔 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="ff408-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="ff408-135">c1</span><span class="sxs-lookup"><span data-stu-id="ff408-135">c1</span></span>          |                   |
| <span data-ttu-id="ff408-136">c2</span><span class="sxs-lookup"><span data-stu-id="ff408-136">c2</span></span>          |                   |
| <span data-ttu-id="ff408-137">c3</span><span class="sxs-lookup"><span data-stu-id="ff408-137">c3</span></span>          | <span data-ttu-id="ff408-138">fa1</span><span class="sxs-lookup"><span data-stu-id="ff408-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="ff408-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff408-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff408-140">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="ff408-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



