---
description: ICE48 會檢查是否已硬式編碼至屬性工作表中的本機路徑的目錄。
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975157"
---
# <a name="ice48"></a><span data-ttu-id="2eb9a-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="2eb9a-103">ICE48</span></span>

<span data-ttu-id="2eb9a-104">ICE48 會檢查是否已硬式編碼至 [屬性工作表](property-table.md)中的本機路徑的目錄。</span><span class="sxs-lookup"><span data-stu-id="2eb9a-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="2eb9a-105">請勿將目錄路徑硬式編碼到本機磁片磁碟機，因為電腦上的本機磁片磁碟機設定不同。</span><span class="sxs-lookup"><span data-stu-id="2eb9a-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="2eb9a-106">如果將應用程式部署到大量的電腦上，而這些電腦的相關部分全都相同，則這種作法可能是可接受的。</span><span class="sxs-lookup"><span data-stu-id="2eb9a-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="2eb9a-107">結果</span><span class="sxs-lookup"><span data-stu-id="2eb9a-107">Result</span></span>

<span data-ttu-id="2eb9a-108">ICE48 會在屬性工作表中有硬式編碼至本機路徑的目錄時張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2eb9a-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="2eb9a-109">範例</span><span class="sxs-lookup"><span data-stu-id="2eb9a-109">Example</span></span>

<span data-ttu-id="2eb9a-110">ICE48 會針對所顯示的範例報告下列警告。</span><span class="sxs-lookup"><span data-stu-id="2eb9a-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="2eb9a-111">[目錄資料表](directory-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2eb9a-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="2eb9a-112">目錄</span><span class="sxs-lookup"><span data-stu-id="2eb9a-112">Directory</span></span> | <span data-ttu-id="2eb9a-113">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="2eb9a-113">Directory\_Parent</span></span> | <span data-ttu-id="2eb9a-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="2eb9a-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="2eb9a-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="2eb9a-115">Dir1</span></span>      |                   | <span data-ttu-id="2eb9a-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="2eb9a-116">SourceDir</span></span>  |



 

<span data-ttu-id="2eb9a-117">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2eb9a-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="2eb9a-118">屬性</span><span class="sxs-lookup"><span data-stu-id="2eb9a-118">Property</span></span> | <span data-ttu-id="2eb9a-119">值</span><span class="sxs-lookup"><span data-stu-id="2eb9a-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="2eb9a-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="2eb9a-120">Dir1</span></span>     | <span data-ttu-id="2eb9a-121">d： \\ 來源</span><span class="sxs-lookup"><span data-stu-id="2eb9a-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2eb9a-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="2eb9a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb9a-123">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="2eb9a-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



