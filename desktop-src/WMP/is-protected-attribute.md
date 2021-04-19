---
title: Is_Protected 屬性
description: '\_受保護的屬性會指出內容是否使用數位版權管理 (DRM) 來保護。'
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980242"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="853a7-104">\_受保護的屬性</span><span class="sxs-lookup"><span data-stu-id="853a7-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="853a7-105">**\_ 受保護** 的屬性會指出內容是否使用數位版權管理 (DRM) 來保護。</span><span class="sxs-lookup"><span data-stu-id="853a7-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="853a7-106">套用至</span><span class="sxs-lookup"><span data-stu-id="853a7-106">Applies To</span></span>

-   [<span data-ttu-id="853a7-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="853a7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="853a7-108">常用的 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="853a7-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="853a7-109">影片專案</span><span class="sxs-lookup"><span data-stu-id="853a7-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="853a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="853a7-110">Remarks</span></span>

<span data-ttu-id="853a7-111">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="853a7-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="853a7-112">**DigitallySecure** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="853a7-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="853a7-113">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMProtected。</span><span class="sxs-lookup"><span data-stu-id="853a7-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="853a7-114">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="853a7-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="853a7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="853a7-115">Requirements</span></span>



| <span data-ttu-id="853a7-116">需求</span><span class="sxs-lookup"><span data-stu-id="853a7-116">Requirement</span></span> | <span data-ttu-id="853a7-117">值</span><span class="sxs-lookup"><span data-stu-id="853a7-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="853a7-118">版本</span><span class="sxs-lookup"><span data-stu-id="853a7-118">Version</span></span><br/> | <span data-ttu-id="853a7-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="853a7-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="853a7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="853a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853a7-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="853a7-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





