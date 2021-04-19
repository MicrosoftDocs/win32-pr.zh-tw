---
title: WM/EncodingTime 屬性
description: WM/EncodingTime 屬性是編碼內容的日期和時間。
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- WM/EncodingTime 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659a1ec5b192782370804745da3f232db6e439dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987077"
---
# <a name="wmencodingtime-attribute"></a><span data-ttu-id="b50ca-104">WM/EncodingTime 屬性</span><span class="sxs-lookup"><span data-stu-id="b50ca-104">WM/EncodingTime Attribute</span></span>

<span data-ttu-id="b50ca-105">**WM/EncodingTime** 屬性是編碼內容的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b50ca-105">The **WM/EncodingTime** attribute is the date and time at which the content was encoded.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b50ca-106">套用至</span><span class="sxs-lookup"><span data-stu-id="b50ca-106">Applies To</span></span>

-   [<span data-ttu-id="b50ca-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="b50ca-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b50ca-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="b50ca-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="b50ca-109">播放清單</span><span class="sxs-lookup"><span data-stu-id="b50ca-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b50ca-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="b50ca-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b50ca-111">備註</span><span class="sxs-lookup"><span data-stu-id="b50ca-111">Remarks</span></span>

<span data-ttu-id="b50ca-112">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="b50ca-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="b50ca-113">**CreationDate** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="b50ca-113">**CreationDate** is an alias for this attribute.</span></span>

<span data-ttu-id="b50ca-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMEncodingTime。</span><span class="sxs-lookup"><span data-stu-id="b50ca-114">The Windows Media Format SDK constant for this attribute is g\_wszWMEncodingTime.</span></span>

<span data-ttu-id="b50ca-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b50ca-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b50ca-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b50ca-116">Requirements</span></span>



| <span data-ttu-id="b50ca-117">需求</span><span class="sxs-lookup"><span data-stu-id="b50ca-117">Requirement</span></span> | <span data-ttu-id="b50ca-118">值</span><span class="sxs-lookup"><span data-stu-id="b50ca-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b50ca-119">版本</span><span class="sxs-lookup"><span data-stu-id="b50ca-119">Version</span></span><br/> | <span data-ttu-id="b50ca-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b50ca-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b50ca-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b50ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50ca-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="b50ca-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





