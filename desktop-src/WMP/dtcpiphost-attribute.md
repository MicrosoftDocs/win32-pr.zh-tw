---
title: DTCPIPHost 屬性
description: DTCPIPHost 屬性是電腦或裝置的名稱或 IP 位址，必須透過網際網路通訊協定連線到數位傳輸內容保護， (DTCP-IP) 針對媒體專案進行驗證的金鑰交換 (確定) 。
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- DTCPIPHost 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990751"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="27387-104">DTCPIPHost 屬性</span><span class="sxs-lookup"><span data-stu-id="27387-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="27387-105">**DTCPIPHost** 屬性是電腦或裝置的名稱或 IP 位址，必須透過網際網路通訊協定連線到數位傳輸內容保護， (DTCP-ip) 針對媒體專案進行驗證的金鑰交換 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="27387-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="27387-106">套用至</span><span class="sxs-lookup"><span data-stu-id="27387-106">Applies To</span></span>

-   [<span data-ttu-id="27387-107">**音訊專案**</span><span class="sxs-lookup"><span data-stu-id="27387-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="27387-108">**相片專案**</span><span class="sxs-lookup"><span data-stu-id="27387-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="27387-109">**播放清單專案**</span><span class="sxs-lookup"><span data-stu-id="27387-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="27387-110">**影片專案**</span><span class="sxs-lookup"><span data-stu-id="27387-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="27387-111">備註</span><span class="sxs-lookup"><span data-stu-id="27387-111">Remarks</span></span>

<span data-ttu-id="27387-112">如果這個屬性可用，則會使用 DTCP-IP 來保護媒體專案。</span><span class="sxs-lookup"><span data-stu-id="27387-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="27387-113">目前使用者的本機文件庫中的媒體專案無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="27387-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="27387-114">它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。</span><span class="sxs-lookup"><span data-stu-id="27387-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="27387-115">若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。</span><span class="sxs-lookup"><span data-stu-id="27387-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="27387-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="27387-116">Requirements</span></span>



| <span data-ttu-id="27387-117">需求</span><span class="sxs-lookup"><span data-stu-id="27387-117">Requirement</span></span> | <span data-ttu-id="27387-118">值</span><span class="sxs-lookup"><span data-stu-id="27387-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="27387-119">版本</span><span class="sxs-lookup"><span data-stu-id="27387-119">Version</span></span><br/> | <span data-ttu-id="27387-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="27387-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27387-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27387-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27387-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="27387-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





