---
title: WM/Language 屬性
description: WM/Language 屬性是專案的語言。
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/Language 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000390"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="d7fcb-104">WM/Language 屬性</span><span class="sxs-lookup"><span data-stu-id="d7fcb-104">WM/Language Attribute</span></span>

<span data-ttu-id="d7fcb-105">**WM/language** 屬性是專案的語言。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d7fcb-106">套用至</span><span class="sxs-lookup"><span data-stu-id="d7fcb-106">Applies To</span></span>

-   [<span data-ttu-id="d7fcb-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="d7fcb-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="d7fcb-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="d7fcb-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="d7fcb-109">單選項目</span><span class="sxs-lookup"><span data-stu-id="d7fcb-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="d7fcb-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="d7fcb-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="d7fcb-111">備註</span><span class="sxs-lookup"><span data-stu-id="d7fcb-111">Remarks</span></span>

<span data-ttu-id="d7fcb-112">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="d7fcb-113">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-113">This attribute may have multiple values.</span></span> <span data-ttu-id="d7fcb-114">若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="d7fcb-115">**Language** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="d7fcb-116">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMLanguage。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="d7fcb-117">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d7fcb-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fcb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7fcb-118">Requirements</span></span>



| <span data-ttu-id="d7fcb-119">需求</span><span class="sxs-lookup"><span data-stu-id="d7fcb-119">Requirement</span></span> | <span data-ttu-id="d7fcb-120">值</span><span class="sxs-lookup"><span data-stu-id="d7fcb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fcb-121">版本</span><span class="sxs-lookup"><span data-stu-id="d7fcb-121">Version</span></span><br/> | <span data-ttu-id="d7fcb-122">Windows Media Player 9 系列或更新版本 (單選項目只在 Windows Media Player 9 系列中支援) </span><span class="sxs-lookup"><span data-stu-id="d7fcb-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7fcb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7fcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fcb-124">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="d7fcb-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="d7fcb-125">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="d7fcb-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





