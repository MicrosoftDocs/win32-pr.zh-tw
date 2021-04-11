---
description: ICE54 會檢查使用隨附檔案作為其金鑰路徑的元件。
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849470"
---
# <a name="ice54"></a><span data-ttu-id="5fd19-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="5fd19-103">ICE54</span></span>

<span data-ttu-id="5fd19-104">ICE54 會檢查使用隨附檔案作為其金鑰路徑的元件。</span><span class="sxs-lookup"><span data-stu-id="5fd19-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="5fd19-105">元件的金鑰路徑檔案不能從不同的檔案衍生其版本。</span><span class="sxs-lookup"><span data-stu-id="5fd19-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="5fd19-106">這可能會導致某些檔案無法安裝。</span><span class="sxs-lookup"><span data-stu-id="5fd19-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="5fd19-107">如需隨附檔案的詳細資訊，請參閱檔案 [表格](file-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="5fd19-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="5fd19-108">結果</span><span class="sxs-lookup"><span data-stu-id="5fd19-108">Result</span></span>

<span data-ttu-id="5fd19-109">如果有任何元件的金鑰路徑檔案衍生自另一個檔案的版本，ICE54 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="5fd19-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="5fd19-110">範例</span><span class="sxs-lookup"><span data-stu-id="5fd19-110">Example</span></span>

<span data-ttu-id="5fd19-111">ICE54 會針對所顯示的範例傳回下列警告。</span><span class="sxs-lookup"><span data-stu-id="5fd19-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="5fd19-112">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="5fd19-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5fd19-113">元件</span><span class="sxs-lookup"><span data-stu-id="5fd19-113">Component</span></span>  | <span data-ttu-id="5fd19-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5fd19-114">Attribute</span></span> | <span data-ttu-id="5fd19-115">KeyPath</span><span class="sxs-lookup"><span data-stu-id="5fd19-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="5fd19-116">Component1</span><span class="sxs-lookup"><span data-stu-id="5fd19-116">Component1</span></span> | <span data-ttu-id="5fd19-117">0</span><span class="sxs-lookup"><span data-stu-id="5fd19-117">0</span></span>         | <span data-ttu-id="5fd19-118">File1</span><span class="sxs-lookup"><span data-stu-id="5fd19-118">File1</span></span>   |



 

<span data-ttu-id="5fd19-119">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="5fd19-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5fd19-120">檔案</span><span class="sxs-lookup"><span data-stu-id="5fd19-120">File</span></span>  | <span data-ttu-id="5fd19-121">版本</span><span class="sxs-lookup"><span data-stu-id="5fd19-121">Version</span></span> | <span data-ttu-id="5fd19-122">語言</span><span class="sxs-lookup"><span data-stu-id="5fd19-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="5fd19-123">File1</span><span class="sxs-lookup"><span data-stu-id="5fd19-123">File1</span></span> | <span data-ttu-id="5fd19-124">File2</span><span class="sxs-lookup"><span data-stu-id="5fd19-124">File2</span></span>   |          |
| <span data-ttu-id="5fd19-125">File2</span><span class="sxs-lookup"><span data-stu-id="5fd19-125">File2</span></span> | <span data-ttu-id="5fd19-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="5fd19-126">1.0.0.0</span></span> | <span data-ttu-id="5fd19-127">1033</span><span class="sxs-lookup"><span data-stu-id="5fd19-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5fd19-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="5fd19-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fd19-129">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="5fd19-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



