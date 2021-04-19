---
title: LibraryID 屬性
description: LibraryID 屬性是專案所屬程式庫的識別碼。
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- LibraryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989802"
---
# <a name="libraryid-attribute"></a><span data-ttu-id="030bd-104">LibraryID 屬性</span><span class="sxs-lookup"><span data-stu-id="030bd-104">LibraryID Attribute</span></span>

<span data-ttu-id="030bd-105">**LibraryID** 屬性是專案所屬程式庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="030bd-105">The **LibraryID** attribute is the identifier of the library that the item belongs to.</span></span>

## <a name="applies-to"></a><span data-ttu-id="030bd-106">套用至</span><span class="sxs-lookup"><span data-stu-id="030bd-106">Applies To</span></span>

-   [<span data-ttu-id="030bd-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="030bd-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="030bd-108">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="030bd-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="030bd-109">**播放清單專案**</span><span class="sxs-lookup"><span data-stu-id="030bd-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="030bd-110">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="030bd-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="030bd-111">備註</span><span class="sxs-lookup"><span data-stu-id="030bd-111">Remarks</span></span>

<span data-ttu-id="030bd-112">媒體專案可能屬於目前使用者的本機文件庫，或可能屬於家用網路或網際網路上的另一位使用者所提供的程式庫。</span><span class="sxs-lookup"><span data-stu-id="030bd-112">A media item might belong to the current user's local library or it might belong to a library that has been made available by another user on the home network or the Internet.</span></span>

<span data-ttu-id="030bd-113">這個屬性的值與 [**IWMPLibrary2：： getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) 方法所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="030bd-113">The value of this attribute is the same as the value returned by the [**IWMPLibrary2::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="030bd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="030bd-114">Requirements</span></span>



| <span data-ttu-id="030bd-115">需求</span><span class="sxs-lookup"><span data-stu-id="030bd-115">Requirement</span></span> | <span data-ttu-id="030bd-116">值</span><span class="sxs-lookup"><span data-stu-id="030bd-116">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="030bd-117">版本</span><span class="sxs-lookup"><span data-stu-id="030bd-117">Version</span></span><br/> | <span data-ttu-id="030bd-118">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="030bd-118">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="030bd-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="030bd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="030bd-120">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="030bd-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





