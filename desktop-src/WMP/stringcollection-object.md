---
title: StringCollection 物件
description: StringCollection 物件提供操作字串集合的方法。
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- StringCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313250"
---
# <a name="stringcollection-object"></a><span data-ttu-id="f29ed-104">StringCollection 物件</span><span class="sxs-lookup"><span data-stu-id="f29ed-104">StringCollection Object</span></span>

<span data-ttu-id="f29ed-105">**StringCollection** 物件提供操作字串集合的方法。</span><span class="sxs-lookup"><span data-stu-id="f29ed-105">The **StringCollection** object provides a way to manipulate a collection of strings.</span></span>

<span data-ttu-id="f29ed-106">**StringCollection** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f29ed-106">The **StringCollection** object supports the following property.</span></span>



| <span data-ttu-id="f29ed-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f29ed-107">Property</span></span>                            | <span data-ttu-id="f29ed-108">描述</span><span class="sxs-lookup"><span data-stu-id="f29ed-108">Description</span></span>                                             |
|-------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="f29ed-109">計數</span><span class="sxs-lookup"><span data-stu-id="f29ed-109">count</span></span>](stringcollection-count.md) | <span data-ttu-id="f29ed-110">抓取字串集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f29ed-110">Retrieves the number of items in the string collection.</span></span> |



 

<span data-ttu-id="f29ed-111">**StringCollection** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="f29ed-111">The **StringCollection** object supports the following methods.</span></span>



| <span data-ttu-id="f29ed-112">方法</span><span class="sxs-lookup"><span data-stu-id="f29ed-112">Method</span></span>                                                                  | <span data-ttu-id="f29ed-113">描述</span><span class="sxs-lookup"><span data-stu-id="f29ed-113">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f29ed-114">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="f29ed-114">getAttributeCountByType</span></span>](stringcollection-getattributecountbytype.md) | <span data-ttu-id="f29ed-115">抓取與指定的 **StringCollection** 專案索引、屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="f29ed-115">Retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span> |
| [<span data-ttu-id="f29ed-116">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="f29ed-116">getItemInfo</span></span>](stringcollection-getiteminfo.md)                         | <span data-ttu-id="f29ed-117">抓取對應于指定之 **StringCollection** 專案索引和名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="f29ed-117">Retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>                                   |
| [<span data-ttu-id="f29ed-118">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="f29ed-118">getItemInfoByType</span></span>](stringcollection-getiteminfobytype.md)             | <span data-ttu-id="f29ed-119">抓取與指定的 **StringCollection** 專案索引、名稱、語言和屬性索引對應的字串。</span><span class="sxs-lookup"><span data-stu-id="f29ed-119">Retrieves the string corresponding to the specified **StringCollection** item index, name, language, and attribute index.</span></span>       |
| [<span data-ttu-id="f29ed-120">isIdentical</span><span class="sxs-lookup"><span data-stu-id="f29ed-120">isIdentical</span></span>](stringcollection-isidentical.md)                         | <span data-ttu-id="f29ed-121">抓取值，指出提供的物件是否與目前的物件相同。</span><span class="sxs-lookup"><span data-stu-id="f29ed-121">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                                        |
| [<span data-ttu-id="f29ed-122">item</span><span class="sxs-lookup"><span data-stu-id="f29ed-122">item</span></span>](stringcollection-item.md)                                       | <span data-ttu-id="f29ed-123">抓取位於指定索引位置的字串。</span><span class="sxs-lookup"><span data-stu-id="f29ed-123">Retrieves the string at the specified index.</span></span>                                                                                    |



 

<span data-ttu-id="f29ed-124">**StringCollection** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="f29ed-124">The **StringCollection** object is accessed through the following method.</span></span>



| <span data-ttu-id="f29ed-125">Object</span><span class="sxs-lookup"><span data-stu-id="f29ed-125">Object</span></span>                                        | <span data-ttu-id="f29ed-126">方法</span><span class="sxs-lookup"><span data-stu-id="f29ed-126">Method</span></span>                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="f29ed-127">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="f29ed-127">MediaCollection</span></span>](mediacollection-object.md) | [<span data-ttu-id="f29ed-128">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="f29ed-128">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) |



 

<span data-ttu-id="f29ed-129">例如， *播放* 程式的用途。*mediaCollection*。**getAttributeStringCollection** (*屬性*， *媒體媒體*) 用於參考語法區段。</span><span class="sxs-lookup"><span data-stu-id="f29ed-129">For purposes of illustration, *player*.*mediaCollection*.**getAttributeStringCollection**(*attribute*, *mediaType*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="f29ed-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f29ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29ed-131">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="f29ed-131">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




