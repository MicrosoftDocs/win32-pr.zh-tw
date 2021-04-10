---
description: ICE58 會檢查您的媒體資料表是否沒有超過80個數據列。
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944843"
---
# <a name="ice58"></a><span data-ttu-id="16c50-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="16c50-103">ICE58</span></span>

<span data-ttu-id="16c50-104">ICE58 會檢查您的 [媒體資料表](media-table.md) 是否沒有超過80個數據列。</span><span class="sxs-lookup"><span data-stu-id="16c50-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="16c50-105">結果</span><span class="sxs-lookup"><span data-stu-id="16c50-105">Result</span></span>

<span data-ttu-id="16c50-106">ICE58 回報的警告會導致安裝失敗，除非封裝是使用 Windows Installer 2.0 或更新版本安裝。</span><span class="sxs-lookup"><span data-stu-id="16c50-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="16c50-107">從 Windows Installer 2.0 開始，會移除超過80個媒體資料表專案的限制。</span><span class="sxs-lookup"><span data-stu-id="16c50-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="16c50-108">如果封裝的 [**頁面計數摘要**](page-count-summary.md) 屬性大於或等於150，則不會發出任何警告。</span><span class="sxs-lookup"><span data-stu-id="16c50-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="16c50-109">架構200或更高版本的套件只能由 Windows Installer 2.0 或更新版本安裝。</span><span class="sxs-lookup"><span data-stu-id="16c50-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="16c50-110">範例</span><span class="sxs-lookup"><span data-stu-id="16c50-110">Example</span></span>

<span data-ttu-id="16c50-111">ICE58 會針對所顯示的範例報告下列錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="16c50-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="16c50-112">若要修正這個錯誤，請排除任何未使用的媒體資料表專案、合併參考相同媒體的媒體資料表專案，以及重新封裝您的應用程式以減少所需的媒體。</span><span class="sxs-lookup"><span data-stu-id="16c50-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="16c50-113">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="16c50-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="16c50-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="16c50-114">DiskId</span></span> | <span data-ttu-id="16c50-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="16c50-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="16c50-116">1</span><span class="sxs-lookup"><span data-stu-id="16c50-116">1</span></span>      | <span data-ttu-id="16c50-117">10</span><span class="sxs-lookup"><span data-stu-id="16c50-117">10</span></span>             |
| <span data-ttu-id="16c50-118">2</span><span class="sxs-lookup"><span data-stu-id="16c50-118">2</span></span>      | <span data-ttu-id="16c50-119">20</span><span class="sxs-lookup"><span data-stu-id="16c50-119">20</span></span>             |
| <span data-ttu-id="16c50-120">...</span><span class="sxs-lookup"><span data-stu-id="16c50-120">...</span></span>    | <span data-ttu-id="16c50-121">...</span><span class="sxs-lookup"><span data-stu-id="16c50-121">...</span></span>            |
| <span data-ttu-id="16c50-122">81</span><span class="sxs-lookup"><span data-stu-id="16c50-122">81</span></span>     | <span data-ttu-id="16c50-123">810</span><span class="sxs-lookup"><span data-stu-id="16c50-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="16c50-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="16c50-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16c50-125">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="16c50-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



