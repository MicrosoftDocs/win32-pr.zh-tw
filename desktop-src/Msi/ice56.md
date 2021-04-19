---
description: ICE56 會驗證 .msi 檔案的目錄結構是否具有單一根目錄、根目錄是 TARGETDIR 屬性，以及 SourceDir 屬性值是否在目錄資料表的 DefaultDir 資料行中。
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988918"
---
# <a name="ice56"></a><span data-ttu-id="42cde-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="42cde-103">ICE56</span></span>

<span data-ttu-id="42cde-104">ICE56 會驗證 .msi 檔案的目錄結構是否具有單一根目錄、根目錄是 [**TARGETDIR**](targetdir.md) 屬性，以及 [**SourceDir**](sourcedir.md) 屬性值是否在 [目錄資料表](directory-table.md)的 DefaultDir 資料行中。</span><span class="sxs-lookup"><span data-stu-id="42cde-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="42cde-105">如果 .msi 檔案有多個根目錄或指定 [**TARGETDIR**](targetdir.md)以外的根目錄， [系統管理安裝](administrative-installation.md) 不會建立正確的系統管理映射。</span><span class="sxs-lookup"><span data-stu-id="42cde-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="42cde-106">請注意，ICE56 不會檢查空的目錄。</span><span class="sxs-lookup"><span data-stu-id="42cde-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="42cde-107">如果額外的目錄是空的，則目錄結構會以多個根目錄傳遞驗證。</span><span class="sxs-lookup"><span data-stu-id="42cde-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="42cde-108">結果</span><span class="sxs-lookup"><span data-stu-id="42cde-108">Result</span></span>

<span data-ttu-id="42cde-109">如果 .msi 沒有單一根、 [**TARGETDIR**](targetdir.md)，或 [目錄資料表](directory-table.md)的 DefaultDir 資料行中未指定 [**SourceDir**](sourcedir.md) ，ICE56 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="42cde-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="42cde-110">範例</span><span class="sxs-lookup"><span data-stu-id="42cde-110">Example</span></span>

<span data-ttu-id="42cde-111">ICE56 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="42cde-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="42cde-112">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="42cde-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="42cde-113">目錄</span><span class="sxs-lookup"><span data-stu-id="42cde-113">Directory</span></span> | <span data-ttu-id="42cde-114">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="42cde-114">Directory\_Parent</span></span> | <span data-ttu-id="42cde-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="42cde-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="42cde-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="42cde-116">TARGETDIR</span></span> |                   | <span data-ttu-id="42cde-117">Temp</span><span class="sxs-lookup"><span data-stu-id="42cde-117">Temp</span></span>       |
| <span data-ttu-id="42cde-118">Root2</span><span class="sxs-lookup"><span data-stu-id="42cde-118">Root2</span></span>     | <span data-ttu-id="42cde-119">Root2</span><span class="sxs-lookup"><span data-stu-id="42cde-119">Root2</span></span>             | <span data-ttu-id="42cde-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="42cde-120">SourceDir</span></span>  |



 

<span data-ttu-id="42cde-121">若要修正第一個錯誤， [**TARGETDIR**](targetdir.md) 根目錄應具有 [**SourceDir**](sourcedir.md)的 DefaultDir 值。</span><span class="sxs-lookup"><span data-stu-id="42cde-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="42cde-122">也接受 SOURCEDIR。</span><span class="sxs-lookup"><span data-stu-id="42cde-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="42cde-123">您可以將 **TARGETDIR** 設為第二個根節點的父系，並使用 DefaultDir 資料行中的 '. ' 值。</span><span class="sxs-lookup"><span data-stu-id="42cde-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="42cde-124">如需詳細資訊，請參閱 [目錄表格](directory-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="42cde-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="42cde-125">為了修正第二個錯誤，目錄結構只能有一個稱為 [**TARGETDIR**](targetdir.md)的根目錄。</span><span class="sxs-lookup"><span data-stu-id="42cde-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="42cde-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="42cde-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42cde-127">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="42cde-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



