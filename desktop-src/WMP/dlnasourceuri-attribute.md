---
title: DLNASourceURI 屬性
description: DLNASourceURI 屬性是專案 (URI) 的通用資源識別碼。
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- DLNASourceURI 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982580"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="e16e9-104">DLNASourceURI 屬性</span><span class="sxs-lookup"><span data-stu-id="e16e9-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="e16e9-105">**DLNASourceURI** 屬性是專案 (URI) 的通用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e16e9-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e16e9-106">套用至</span><span class="sxs-lookup"><span data-stu-id="e16e9-106">Applies To</span></span>

-   [<span data-ttu-id="e16e9-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="e16e9-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e16e9-108">**其他專案**</span><span class="sxs-lookup"><span data-stu-id="e16e9-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="e16e9-109">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="e16e9-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="e16e9-110">**播放清單專案**</span><span class="sxs-lookup"><span data-stu-id="e16e9-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="e16e9-111">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="e16e9-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e16e9-112">備註</span><span class="sxs-lookup"><span data-stu-id="e16e9-112">Remarks</span></span>

<span data-ttu-id="e16e9-113">如果專案是在目前使用者的本機文件庫中，則這個屬性、 [**SourceURL**](sourceurl-attribute.md) 屬性以及 [**IWMPMedia：： get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) 所傳回的值全都相同。</span><span class="sxs-lookup"><span data-stu-id="e16e9-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="e16e9-114">如果專案不在目前使用者的本機文件庫中，但屬於遠端程式庫，此屬性就是 playsingle：//*xxx* 格式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e16e9-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="e16e9-115">您可以將 playsingle URI 傳遞至 [**IWMPCore3：： newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) 方法，以取得可讓您查看媒體專案中繼資料的 [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) 介面，並可能會編輯媒體專案的星級評等。</span><span class="sxs-lookup"><span data-stu-id="e16e9-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="e16e9-116">不過請注意，playsingle URI 必須是 Windows Media Player 已經探索到的內容目錄服務 (CD) 。</span><span class="sxs-lookup"><span data-stu-id="e16e9-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="e16e9-117">**NewMedia** 方法不會起始 UPnP 探索並搜尋 cd。</span><span class="sxs-lookup"><span data-stu-id="e16e9-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="e16e9-118">只有在遠端程式庫支援編輯作業時，您才可以編輯遠端媒體櫃中媒體專案的星星評等。</span><span class="sxs-lookup"><span data-stu-id="e16e9-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="e16e9-119">在執行 Windows 7 的電腦上主控的遠端程式庫支援編輯作業。</span><span class="sxs-lookup"><span data-stu-id="e16e9-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="e16e9-120">在執行 windows 7 之前 Windows 作業系統的電腦上裝載的遠端程式庫不支援編輯作業。</span><span class="sxs-lookup"><span data-stu-id="e16e9-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e16e9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e16e9-121">Requirements</span></span>



| <span data-ttu-id="e16e9-122">需求</span><span class="sxs-lookup"><span data-stu-id="e16e9-122">Requirement</span></span> | <span data-ttu-id="e16e9-123">值</span><span class="sxs-lookup"><span data-stu-id="e16e9-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="e16e9-124">版本</span><span class="sxs-lookup"><span data-stu-id="e16e9-124">Version</span></span><br/> | <span data-ttu-id="e16e9-125">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="e16e9-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e16e9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e16e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16e9-127">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="e16e9-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





