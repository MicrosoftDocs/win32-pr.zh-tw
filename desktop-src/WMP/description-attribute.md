---
title: 'Description 屬性 (WMP SDK) '
description: Description 屬性是內容的描述。
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994214"
---
# <a name="description-attribute"></a><span data-ttu-id="f8004-104">Description 屬性</span><span class="sxs-lookup"><span data-stu-id="f8004-104">Description Attribute</span></span>

<span data-ttu-id="f8004-105">**Description** 屬性是內容的描述。</span><span class="sxs-lookup"><span data-stu-id="f8004-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f8004-106">套用至</span><span class="sxs-lookup"><span data-stu-id="f8004-106">Applies To</span></span>

-   [<span data-ttu-id="f8004-107">音樂檔案</span><span class="sxs-lookup"><span data-stu-id="f8004-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f8004-108">備註</span><span class="sxs-lookup"><span data-stu-id="f8004-108">Remarks</span></span>

<span data-ttu-id="f8004-109">這個屬性會儲存在音樂檔案中，而不是儲存在文件庫中。</span><span class="sxs-lookup"><span data-stu-id="f8004-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="f8004-110">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="f8004-110">This attribute may have multiple values.</span></span> <span data-ttu-id="f8004-111">若要取得多重值屬性的所有值，您必須使用 *媒體*。**getItemInfoByType** 方法，而不 *是 getItemInfo* 方法。</span><span class="sxs-lookup"><span data-stu-id="f8004-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="f8004-112">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMDescription。</span><span class="sxs-lookup"><span data-stu-id="f8004-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="f8004-113">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f8004-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8004-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8004-114">Requirements</span></span>



| <span data-ttu-id="f8004-115">需求</span><span class="sxs-lookup"><span data-stu-id="f8004-115">Requirement</span></span> | <span data-ttu-id="f8004-116">值</span><span class="sxs-lookup"><span data-stu-id="f8004-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f8004-117">版本</span><span class="sxs-lookup"><span data-stu-id="f8004-117">Version</span></span><br/> | <span data-ttu-id="f8004-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f8004-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8004-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8004-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8004-120">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="f8004-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





