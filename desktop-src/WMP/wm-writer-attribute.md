---
title: WM/Writer 屬性
description: WM/Writer 屬性是寫入內容文字之寫入器的名稱。
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- WM/寫入器屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989871"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="90634-104">WM/Writer 屬性</span><span class="sxs-lookup"><span data-stu-id="90634-104">WM/Writer Attribute</span></span>

<span data-ttu-id="90634-105">**WM/Writer** 屬性是寫入內容文字之寫入器的名稱。</span><span class="sxs-lookup"><span data-stu-id="90634-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="90634-106">套用至</span><span class="sxs-lookup"><span data-stu-id="90634-106">Applies To</span></span>

-   [<span data-ttu-id="90634-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="90634-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="90634-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="90634-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="90634-109">影片專案</span><span class="sxs-lookup"><span data-stu-id="90634-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="90634-110">備註</span><span class="sxs-lookup"><span data-stu-id="90634-110">Remarks</span></span>

<span data-ttu-id="90634-111">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="90634-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="90634-112">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="90634-112">This attribute may have multiple values.</span></span> <span data-ttu-id="90634-113">若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="90634-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="90634-114">**寫入器** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="90634-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="90634-115">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMWriter。</span><span class="sxs-lookup"><span data-stu-id="90634-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="90634-116">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="90634-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="90634-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="90634-117">Requirements</span></span>



| <span data-ttu-id="90634-118">需求</span><span class="sxs-lookup"><span data-stu-id="90634-118">Requirement</span></span> | <span data-ttu-id="90634-119">值</span><span class="sxs-lookup"><span data-stu-id="90634-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="90634-120">版本</span><span class="sxs-lookup"><span data-stu-id="90634-120">Version</span></span><br/> | <span data-ttu-id="90634-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="90634-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90634-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90634-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90634-123">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="90634-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="90634-124">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="90634-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





