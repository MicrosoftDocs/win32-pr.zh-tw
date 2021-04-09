---
title: 屬性範圍抓取
description: 多重值屬性幾乎可以有任意數目的值。 在許多情況下，它可能很有利，甚至是必要的，以限制查詢所抓取的值範圍。
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- 屬性範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931857"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="58a3d-105">屬性範圍抓取</span><span class="sxs-lookup"><span data-stu-id="58a3d-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="58a3d-106">多重值屬性幾乎可以有任意數目的值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="58a3d-107">在許多情況下，它可能很有利，甚至是必要的，以限制查詢所抓取的值範圍。</span><span class="sxs-lookup"><span data-stu-id="58a3d-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="58a3d-108">範圍抓取需要在單一查詢中要求有限數目的屬性值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="58a3d-109">要求的值數目必須小於或等於伺服器支援的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="58a3d-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="58a3d-110">為了減少查詢必須與伺服器聯繫的次數，要求的值數目應盡可能接近此最大值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="58a3d-111">若要讓應用程式能夠與所有 Windows 伺服器正確搭配運作，應使用最大的1000數目。</span><span class="sxs-lookup"><span data-stu-id="58a3d-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="58a3d-112">屬性查詢的範圍規範需要下列格式：</span><span class="sxs-lookup"><span data-stu-id="58a3d-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="58a3d-113">其中「 &lt; 下限」 &gt; 是要抓取之第一個屬性值的以零為起始的索引，而「 &lt; 高範圍」 &gt; 是要抓取之最後一個屬性值的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="58a3d-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="58a3d-114">「範圍下限」會使用零 &lt; &gt; 來指定第一個專案。</span><span class="sxs-lookup"><span data-stu-id="58a3d-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="58a3d-115">萬用字元 (\*) 可用於「 &lt; 高範圍」 &gt; 以指定所有剩餘的專案。</span><span class="sxs-lookup"><span data-stu-id="58a3d-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="58a3d-116">下表列出範圍規範的範例。</span><span class="sxs-lookup"><span data-stu-id="58a3d-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="58a3d-117">範例</span><span class="sxs-lookup"><span data-stu-id="58a3d-117">Example</span></span>      | <span data-ttu-id="58a3d-118">描述</span><span class="sxs-lookup"><span data-stu-id="58a3d-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a3d-119">範圍 = 0-\*</span><span class="sxs-lookup"><span data-stu-id="58a3d-119">range=0-\*</span></span>   | <span data-ttu-id="58a3d-120">取出所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-120">Retrieve all property values.</span></span> <span data-ttu-id="58a3d-121">這會受限於伺服器所加諸的限制。</span><span class="sxs-lookup"><span data-stu-id="58a3d-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="58a3d-122">範圍 = 0-500</span><span class="sxs-lookup"><span data-stu-id="58a3d-122">range=0-500</span></span>  | <span data-ttu-id="58a3d-123">從1取出至501st 值（含）。</span><span class="sxs-lookup"><span data-stu-id="58a3d-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="58a3d-124">範圍 = 2-3</span><span class="sxs-lookup"><span data-stu-id="58a3d-124">range=2-3</span></span>    | <span data-ttu-id="58a3d-125">取出第三和第四個值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="58a3d-126">範圍 = 501-\*</span><span class="sxs-lookup"><span data-stu-id="58a3d-126">range=501-\*</span></span> | <span data-ttu-id="58a3d-127">取出502nd 和所有剩餘的值。</span><span class="sxs-lookup"><span data-stu-id="58a3d-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="58a3d-128">這會受限於伺服器所加諸的限制。</span><span class="sxs-lookup"><span data-stu-id="58a3d-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="58a3d-129">有幾種不同的方式可捕獲屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="58a3d-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="58a3d-130">[**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法可以在自動化語言或 c + + 中使用。</span><span class="sxs-lookup"><span data-stu-id="58a3d-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="58a3d-131">**IADs. GetInfoEx** 方法是執行範圍抓取的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="58a3d-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="58a3d-132">如需有關使用 **IADs GetInfoEx** 進行範圍抓取的詳細資訊，請參閱 [使用 IADs：： GetInfoEx 來取得範圍的提取](using-iads--getinfoex-for-range-retrieval.md)。</span><span class="sxs-lookup"><span data-stu-id="58a3d-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="58a3d-133">如果使用自動化語言， (ADO) 的 ActiveX 目錄物件就可以用來抓取屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="58a3d-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="58a3d-134">如需使用 ADO 進行範圍抓取的詳細資訊，請參閱 [使用 ado 進行範圍](using-ado-for-range-retrieval.md)抓取。</span><span class="sxs-lookup"><span data-stu-id="58a3d-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="58a3d-135">如果使用 c + +， [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 和 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面可以用來取得屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="58a3d-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="58a3d-136">如需使用 **>idirectorysearch** 和 **IDirectoryObject** 進行範圍抓取的詳細資訊，請參閱 [使用 >idirectorysearch 和 IDirectoryObject 進行範圍](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md)抓取。</span><span class="sxs-lookup"><span data-stu-id="58a3d-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




