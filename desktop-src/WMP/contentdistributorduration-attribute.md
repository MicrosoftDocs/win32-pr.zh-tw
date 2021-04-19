---
title: ContentDistributorDuration 屬性
description: ContentDistributorDuration 屬性是專案的播放持續時間（以秒為單位）。
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- ContentDistributorDuration 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997725"
---
# <a name="contentdistributorduration-attribute"></a><span data-ttu-id="3252a-104">ContentDistributorDuration 屬性</span><span class="sxs-lookup"><span data-stu-id="3252a-104">ContentDistributorDuration Attribute</span></span>

<span data-ttu-id="3252a-105">**ContentDistributorDuration** 屬性是專案的播放持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3252a-105">The **ContentDistributorDuration** attribute is the playing duration of the item, in seconds.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3252a-106">套用至</span><span class="sxs-lookup"><span data-stu-id="3252a-106">Applies To</span></span>

-   [<span data-ttu-id="3252a-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="3252a-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3252a-108">其他專案</span><span class="sxs-lookup"><span data-stu-id="3252a-108">Other Items</span></span>](other-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3252a-109">備註</span><span class="sxs-lookup"><span data-stu-id="3252a-109">Remarks</span></span>

<span data-ttu-id="3252a-110">如果 [一般 **持續時間** ] 屬性未設定 (Null) 或0，則會改為傳回這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3252a-110">If the regular **Duration** attribute is either not set (Null) or 0, then the value of this attribute will be returned instead.</span></span>

<span data-ttu-id="3252a-111">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3252a-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3252a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3252a-112">Requirements</span></span>



| <span data-ttu-id="3252a-113">需求</span><span class="sxs-lookup"><span data-stu-id="3252a-113">Requirement</span></span> | <span data-ttu-id="3252a-114">值</span><span class="sxs-lookup"><span data-stu-id="3252a-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="3252a-115">版本</span><span class="sxs-lookup"><span data-stu-id="3252a-115">Version</span></span><br/> | <span data-ttu-id="3252a-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3252a-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3252a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3252a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3252a-118">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="3252a-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="3252a-119">**Duration 屬性**</span><span class="sxs-lookup"><span data-stu-id="3252a-119">**Duration Attribute**</span></span>](duration-attribute.md)
</dt> </dl>

 

 





