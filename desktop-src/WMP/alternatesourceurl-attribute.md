---
title: AlternateSourceURL 屬性
description: AlternateSourceURL 屬性是媒體專案的統一資源定位器，可做為 DLNASourceURI 和 SourceURL 屬性的替代專案。
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- AlternateSourceURL 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000806"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="316c2-104">AlternateSourceURL 屬性</span><span class="sxs-lookup"><span data-stu-id="316c2-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="316c2-105">**AlternateSourceURL** 屬性是媒體專案的統一資源定位器，可做為 [**DLNASourceURI**](dlnasourceuri-attribute.md)和 [**SourceURL**](sourceurl-attribute.md)屬性的替代專案。</span><span class="sxs-lookup"><span data-stu-id="316c2-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="316c2-106">套用至</span><span class="sxs-lookup"><span data-stu-id="316c2-106">Applies To</span></span>

-   [<span data-ttu-id="316c2-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="316c2-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="316c2-108">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="316c2-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="316c2-109">**播放清單專案**</span><span class="sxs-lookup"><span data-stu-id="316c2-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="316c2-110">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="316c2-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="316c2-111">備註</span><span class="sxs-lookup"><span data-stu-id="316c2-111">Remarks</span></span>

<span data-ttu-id="316c2-112">目前使用者的本機文件庫中的媒體專案無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="316c2-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="316c2-113">它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。</span><span class="sxs-lookup"><span data-stu-id="316c2-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="316c2-114">若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。</span><span class="sxs-lookup"><span data-stu-id="316c2-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="316c2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="316c2-115">Requirements</span></span>



| <span data-ttu-id="316c2-116">需求</span><span class="sxs-lookup"><span data-stu-id="316c2-116">Requirement</span></span> | <span data-ttu-id="316c2-117">值</span><span class="sxs-lookup"><span data-stu-id="316c2-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="316c2-118">版本</span><span class="sxs-lookup"><span data-stu-id="316c2-118">Version</span></span><br/> | <span data-ttu-id="316c2-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="316c2-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="316c2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="316c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316c2-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="316c2-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





