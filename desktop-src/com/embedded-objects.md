---
title: COM)  (的内嵌物件
description: 内嵌物件
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093643"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="b60cb-103">COM)  (的内嵌物件</span><span class="sxs-lookup"><span data-stu-id="b60cb-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="b60cb-104">内嵌物件實際上會儲存在複合檔案中，以及管理物件所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="b60cb-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="b60cb-105">換句話說，嵌入的物件實際上是它所在的複合檔案的一部分。</span><span class="sxs-lookup"><span data-stu-id="b60cb-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="b60cb-106">這種安排有幾個缺點。</span><span class="sxs-lookup"><span data-stu-id="b60cb-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="b60cb-107">首先，包含内嵌物件的複合檔案將會大於一個，其中包含與連結相同的物件。</span><span class="sxs-lookup"><span data-stu-id="b60cb-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="b60cb-108">其次，對内嵌物件來源所做的變更將不會自動複寫到內嵌的複本中，而且內嵌複本中的變更不會反映在來源中，因為它們是使用連結。</span><span class="sxs-lookup"><span data-stu-id="b60cb-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="b60cb-109">但基於特定目的，內嵌提供數個優於連結的優點。</span><span class="sxs-lookup"><span data-stu-id="b60cb-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="b60cb-110">首先，使用者可以將包含内嵌物件的複合檔案傳輸到其他電腦，或同一部電腦上的其他位置，而不會中斷連結。</span><span class="sxs-lookup"><span data-stu-id="b60cb-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="b60cb-111">其次，使用者可以編輯内嵌物件，而不需要變更原始內容。</span><span class="sxs-lookup"><span data-stu-id="b60cb-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="b60cb-112">有時候，這項分隔正是必要的。</span><span class="sxs-lookup"><span data-stu-id="b60cb-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="b60cb-113">第三，内嵌物件可以就地啟用，這表示使用者可以編輯或操作物件，而不需要在與物件容器不同的視窗中工作。</span><span class="sxs-lookup"><span data-stu-id="b60cb-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="b60cb-114">相反地，當物件啟用時，容器應用程式的使用者介面會變更，以公開管理或修改物件時所需的工具。</span><span class="sxs-lookup"><span data-stu-id="b60cb-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b60cb-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b60cb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b60cb-116">從現有資料建立連結和內嵌物件</span><span class="sxs-lookup"><span data-stu-id="b60cb-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




