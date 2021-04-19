---
title: WM/ContentDistributorType 屬性
description: WM/ContentDistributorType 屬性是專案散發者的型別。
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- WM/ContentDistributorType 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977486"
---
# <a name="wmcontentdistributortype-attribute"></a><span data-ttu-id="9bbbd-104">WM/ContentDistributorType 屬性</span><span class="sxs-lookup"><span data-stu-id="9bbbd-104">WM/ContentDistributorType Attribute</span></span>

<span data-ttu-id="9bbbd-105">**WM/ContentDistributorType** 屬性是專案散發者的型別。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-105">The **WM/ContentDistributorType** attribute is the type of the distributor of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9bbbd-106">套用至</span><span class="sxs-lookup"><span data-stu-id="9bbbd-106">Applies To</span></span>

-   [<span data-ttu-id="9bbbd-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="9bbbd-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="9bbbd-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9bbbd-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="9bbbd-109">播放清單</span><span class="sxs-lookup"><span data-stu-id="9bbbd-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="9bbbd-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="9bbbd-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9bbbd-111">備註</span><span class="sxs-lookup"><span data-stu-id="9bbbd-111">Remarks</span></span>

<span data-ttu-id="9bbbd-112">這個屬性的值將會設定為 "List" 或 "單選"。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-112">The value of this attribute will be set to either "List" or "Radio".</span></span> <span data-ttu-id="9bbbd-113">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-113">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="9bbbd-114">**ContentDistributorType** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-114">**ContentDistributorType** is an alias for this attribute.</span></span>

<span data-ttu-id="9bbbd-115">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMContentDistributorType。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-115">The Windows Media Format SDK constant for this attribute is g\_wszWMContentDistributorType.</span></span>

<span data-ttu-id="9bbbd-116">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9bbbd-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbbd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bbbd-117">Requirements</span></span>



| <span data-ttu-id="9bbbd-118">需求</span><span class="sxs-lookup"><span data-stu-id="9bbbd-118">Requirement</span></span> | <span data-ttu-id="9bbbd-119">值</span><span class="sxs-lookup"><span data-stu-id="9bbbd-119">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="9bbbd-120">版本</span><span class="sxs-lookup"><span data-stu-id="9bbbd-120">Version</span></span><br/> | <span data-ttu-id="9bbbd-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="9bbbd-121">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bbbd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bbbd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bbbd-123">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="9bbbd-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





