---
title: 暫存屬性
description: 暫存屬性指定播放清單是否為暫時性。
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- 暫存屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984294"
---
# <a name="temporary-attribute"></a><span data-ttu-id="a00ca-104">暫存屬性</span><span class="sxs-lookup"><span data-stu-id="a00ca-104">Temporary Attribute</span></span>

<span data-ttu-id="a00ca-105">**暫存** 屬性指定播放清單是否為暫時性。</span><span class="sxs-lookup"><span data-stu-id="a00ca-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="a00ca-106">**備註**</span><span class="sxs-lookup"><span data-stu-id="a00ca-106">**Remarks**</span></span>

<span data-ttu-id="a00ca-107">如果您從程式庫中取出播放清單，則對播放清單所做的變更會反映在使用者的程式庫中。</span><span class="sxs-lookup"><span data-stu-id="a00ca-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="a00ca-108">若要避免這種情況，請呼叫 [IWMPPlaylist：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) 傳遞屬性名稱 "暫時性" 和值 "true"。</span><span class="sxs-lookup"><span data-stu-id="a00ca-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="a00ca-109">這會將您的播放清單實例轉換成暫時的播放清單，在不變更原始播放清單的情況下，可以安全地進行編輯。</span><span class="sxs-lookup"><span data-stu-id="a00ca-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="a00ca-110">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a00ca-110">**Applies To**</span></span>

-   [<span data-ttu-id="a00ca-111">播放清單</span><span class="sxs-lookup"><span data-stu-id="a00ca-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="a00ca-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a00ca-112">Requirements</span></span>



| <span data-ttu-id="a00ca-113">需求</span><span class="sxs-lookup"><span data-stu-id="a00ca-113">Requirement</span></span> | <span data-ttu-id="a00ca-114">值</span><span class="sxs-lookup"><span data-stu-id="a00ca-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="a00ca-115">版本</span><span class="sxs-lookup"><span data-stu-id="a00ca-115">Version</span></span><br/> | <span data-ttu-id="a00ca-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="a00ca-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a00ca-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a00ca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00ca-118">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="a00ca-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





