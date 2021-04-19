---
title: WM/AlbumCoverURL 屬性
description: WM/AlbumCoverURL 屬性是適用于專輯封面或縮圖影像 (URL) 的統一資源定位器。
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- WM/AlbumCoverURL 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978672"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="769f7-104">WM/AlbumCoverURL 屬性</span><span class="sxs-lookup"><span data-stu-id="769f7-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="769f7-105">**WM/AlbumCoverURL** 屬性是適用于專輯封面或縮圖影像 (URL) 的統一資源定位器。</span><span class="sxs-lookup"><span data-stu-id="769f7-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="769f7-106">套用至</span><span class="sxs-lookup"><span data-stu-id="769f7-106">Applies To</span></span>

-   [<span data-ttu-id="769f7-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="769f7-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="769f7-108">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="769f7-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="769f7-109">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="769f7-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="769f7-110">備註</span><span class="sxs-lookup"><span data-stu-id="769f7-110">Remarks</span></span>

<span data-ttu-id="769f7-111">若是音訊專案，這個屬性就是專輯封面的 URL。</span><span class="sxs-lookup"><span data-stu-id="769f7-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="769f7-112">如果是相片或影片專案，這個屬性就是縮圖影像的 URL。</span><span class="sxs-lookup"><span data-stu-id="769f7-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="769f7-113">目前使用者的本機文件庫中的媒體專案無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="769f7-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="769f7-114">它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。</span><span class="sxs-lookup"><span data-stu-id="769f7-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="769f7-115">若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。</span><span class="sxs-lookup"><span data-stu-id="769f7-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="769f7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="769f7-116">Requirements</span></span>



| <span data-ttu-id="769f7-117">需求</span><span class="sxs-lookup"><span data-stu-id="769f7-117">Requirement</span></span> | <span data-ttu-id="769f7-118">值</span><span class="sxs-lookup"><span data-stu-id="769f7-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="769f7-119">版本</span><span class="sxs-lookup"><span data-stu-id="769f7-119">Version</span></span><br/> | <span data-ttu-id="769f7-120">Windows Media Player 12 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="769f7-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="769f7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="769f7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769f7-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="769f7-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





