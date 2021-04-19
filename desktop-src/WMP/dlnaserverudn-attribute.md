---
title: DLNAServerUDN 屬性
description: DLNAServerUDN 屬性是裝載媒體專案之伺服器的唯一裝置名稱。
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- DLNAServerUDN 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001906"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="f9e7b-104">DLNAServerUDN 屬性</span><span class="sxs-lookup"><span data-stu-id="f9e7b-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="f9e7b-105">**DLNAServerUDN** 屬性是裝載媒體專案之伺服器的唯一裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="f9e7b-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f9e7b-106">套用至</span><span class="sxs-lookup"><span data-stu-id="f9e7b-106">Applies To</span></span>

-   [<span data-ttu-id="f9e7b-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f9e7b-108">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="f9e7b-109">**播放清單專案**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="f9e7b-110">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f9e7b-111">備註</span><span class="sxs-lookup"><span data-stu-id="f9e7b-111">Remarks</span></span>

<span data-ttu-id="f9e7b-112">目前使用者的本機文件庫中的媒體專案無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f9e7b-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="f9e7b-113">它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。</span><span class="sxs-lookup"><span data-stu-id="f9e7b-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="f9e7b-114">若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。</span><span class="sxs-lookup"><span data-stu-id="f9e7b-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e7b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9e7b-115">Requirements</span></span>



| <span data-ttu-id="f9e7b-116">需求</span><span class="sxs-lookup"><span data-stu-id="f9e7b-116">Requirement</span></span> | <span data-ttu-id="f9e7b-117">值</span><span class="sxs-lookup"><span data-stu-id="f9e7b-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f9e7b-118">版本</span><span class="sxs-lookup"><span data-stu-id="f9e7b-118">Version</span></span><br/> | <span data-ttu-id="f9e7b-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="f9e7b-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9e7b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9e7b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e7b-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





