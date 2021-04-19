---
title: DisplayArtist 屬性
description: DisplayArtist 屬性是針對專案顯示之演出者的名稱。
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978695"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="de60e-104">DisplayArtist 屬性</span><span class="sxs-lookup"><span data-stu-id="de60e-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="de60e-105">**DisplayArtist** 屬性是針對專案顯示之演出者的名稱。</span><span class="sxs-lookup"><span data-stu-id="de60e-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="de60e-106">套用至</span><span class="sxs-lookup"><span data-stu-id="de60e-106">Applies To</span></span>

-   [<span data-ttu-id="de60e-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="de60e-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="de60e-108">備註</span><span class="sxs-lookup"><span data-stu-id="de60e-108">Remarks</span></span>

<span data-ttu-id="de60e-109">一般來說，當設定屬性時， **DisplayArtist** 會具有與 **WM/AlbumArtist** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="de60e-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="de60e-110">否則，此值會是與專輯上第一個曲目相關聯之演出者的名稱。</span><span class="sxs-lookup"><span data-stu-id="de60e-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="de60e-111">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="de60e-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="de60e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="de60e-112">Requirements</span></span>



| <span data-ttu-id="de60e-113">需求</span><span class="sxs-lookup"><span data-stu-id="de60e-113">Requirement</span></span> | <span data-ttu-id="de60e-114">值</span><span class="sxs-lookup"><span data-stu-id="de60e-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="de60e-115">版本</span><span class="sxs-lookup"><span data-stu-id="de60e-115">Version</span></span><br/> | <span data-ttu-id="de60e-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="de60e-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de60e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de60e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de60e-118">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="de60e-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="de60e-119">**WM/AlbumArtist 屬性**</span><span class="sxs-lookup"><span data-stu-id="de60e-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 





