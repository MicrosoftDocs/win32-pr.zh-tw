---
title: WM/ContentDistributor 屬性
description: WM/ContentDistributor 屬性是專案的散發者名稱。
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- WM/ContentDistributor 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995270"
---
# <a name="wmcontentdistributor-attribute"></a><span data-ttu-id="9e066-104">WM/ContentDistributor 屬性</span><span class="sxs-lookup"><span data-stu-id="9e066-104">WM/ContentDistributor Attribute</span></span>

<span data-ttu-id="9e066-105">**WM/ContentDistributor** 屬性是專案的散發者名稱。</span><span class="sxs-lookup"><span data-stu-id="9e066-105">The **WM/ContentDistributor** attribute is the name of the distributor of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e066-106">套用至</span><span class="sxs-lookup"><span data-stu-id="9e066-106">Applies To</span></span>

-   [<span data-ttu-id="9e066-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="9e066-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="9e066-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9e066-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="9e066-109">播放清單</span><span class="sxs-lookup"><span data-stu-id="9e066-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="9e066-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="9e066-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9e066-111">備註</span><span class="sxs-lookup"><span data-stu-id="9e066-111">Remarks</span></span>

<span data-ttu-id="9e066-112">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="9e066-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="9e066-113">**ContentDistributor** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="9e066-113">**ContentDistributor** is an alias for this attribute.</span></span>

<span data-ttu-id="9e066-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMContentDistributor。</span><span class="sxs-lookup"><span data-stu-id="9e066-114">The Windows Media Format SDK constant for this attribute is g\_wszWMContentDistributor.</span></span>

<span data-ttu-id="9e066-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9e066-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e066-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e066-116">Requirements</span></span>



| <span data-ttu-id="9e066-117">需求</span><span class="sxs-lookup"><span data-stu-id="9e066-117">Requirement</span></span> | <span data-ttu-id="9e066-118">值</span><span class="sxs-lookup"><span data-stu-id="9e066-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9e066-119">版本</span><span class="sxs-lookup"><span data-stu-id="9e066-119">Version</span></span><br/> | <span data-ttu-id="9e066-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="9e066-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e066-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e066-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e066-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="9e066-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





