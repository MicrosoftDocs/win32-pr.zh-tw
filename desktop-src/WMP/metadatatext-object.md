---
title: MetadataText 物件
description: MetadataText 物件提供一種方式，來取得複雜文字中繼資料屬性的中繼資料。
ms.assetid: cf8e4524-6fc5-4534-9542-6bdc7d34bca4
keywords:
- MetadataText 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MetadataText Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b043a9050d03ca562159aa5be0c113084ac152fb
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373455"
---
# <a name="metadatatext-object"></a><span data-ttu-id="ce3b7-104">MetadataText 物件</span><span class="sxs-lookup"><span data-stu-id="ce3b7-104">MetadataText Object</span></span>

<span data-ttu-id="ce3b7-105">**MetadataText** 物件提供一種方式，來取得複雜文字中繼資料屬性的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-105">The **MetadataText** object provides a way to retrieve metadata for complex textual metadata attributes.</span></span>

<span data-ttu-id="ce3b7-106">**MetadataText** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-106">The **MetadataText** object supports the following properties.</span></span>



| <span data-ttu-id="ce3b7-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ce3b7-107">Property</span></span>                                    | <span data-ttu-id="ce3b7-108">描述</span><span class="sxs-lookup"><span data-stu-id="ce3b7-108">Description</span></span>                                   |
|---------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ce3b7-109">description</span><span class="sxs-lookup"><span data-stu-id="ce3b7-109">description</span></span>](metadatatext-description.md) | <span data-ttu-id="ce3b7-110">捕獲中繼資料文字的描述。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-110">Retrieves a description of the metadata text.</span></span> |
| [<span data-ttu-id="ce3b7-111">text</span><span class="sxs-lookup"><span data-stu-id="ce3b7-111">text</span></span>](metadatatext-text.md)               | <span data-ttu-id="ce3b7-112">捕獲中繼資料文字。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-112">Retrieves the metadata text.</span></span>                  |



 

<span data-ttu-id="ce3b7-113">**MetadataText** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-113">The **MetadataText** object is accessed through the following method.</span></span>



| <span data-ttu-id="ce3b7-114">Object</span><span class="sxs-lookup"><span data-stu-id="ce3b7-114">Object</span></span>                    | <span data-ttu-id="ce3b7-115">方法</span><span class="sxs-lookup"><span data-stu-id="ce3b7-115">Method</span></span>                                           |
|---------------------------|--------------------------------------------------|
| [<span data-ttu-id="ce3b7-116">媒體</span><span class="sxs-lookup"><span data-stu-id="ce3b7-116">Media</span></span>](media-object.md) | [<span data-ttu-id="ce3b7-117">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="ce3b7-117">getItemInfoByType</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="ce3b7-118">例如， *播放* 程式的用途。*currentMedia*。**getItemInfoByType** (*name*、 *language*、 *index*) 用於參考語法區段中。</span><span class="sxs-lookup"><span data-stu-id="ce3b7-118">For purposes of illustration, *player*.*currentMedia*.**getItemInfoByType**(*name*, *language*, *index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce3b7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce3b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3b7-120">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="ce3b7-120">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




