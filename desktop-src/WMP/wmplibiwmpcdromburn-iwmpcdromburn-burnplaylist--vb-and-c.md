---
title: IWMPCdromBurn burnPlaylist 屬性
description: BurnPlaylist 屬性會取得要燒錄到 CD 的目前播放清單。
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- burnPlaylist 屬性 Windows Media Player
- burnPlaylist 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，burnPlaylist 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983095"
---
# <a name="iwmpcdromburnburnplaylist-property"></a><span data-ttu-id="fe4b9-106">IWMPCdromBurn：： burnPlaylist 屬性</span><span class="sxs-lookup"><span data-stu-id="fe4b9-106">IWMPCdromBurn::burnPlaylist property</span></span>

<span data-ttu-id="fe4b9-107">**BurnPlaylist** 屬性會取得要燒錄到 CD 的目前播放清單。</span><span class="sxs-lookup"><span data-stu-id="fe4b9-107">The **burnPlaylist** property gets the current playlist to burn to the CD.</span></span>

<span data-ttu-id="fe4b9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fe4b9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4b9-109">語法</span><span class="sxs-lookup"><span data-stu-id="fe4b9-109">Syntax</span></span>


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="fe4b9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fe4b9-110">Property value</span></span>

<span data-ttu-id="fe4b9-111">要燒錄之播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="fe4b9-111">The **WMPLib.IWMPPlaylist** interface of the playlist to burn.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4b9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe4b9-112">Requirements</span></span>



| <span data-ttu-id="fe4b9-113">需求</span><span class="sxs-lookup"><span data-stu-id="fe4b9-113">Requirement</span></span> | <span data-ttu-id="fe4b9-114">值</span><span class="sxs-lookup"><span data-stu-id="fe4b9-114">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4b9-115">版本</span><span class="sxs-lookup"><span data-stu-id="fe4b9-115">Version</span></span><br/>   | <span data-ttu-id="fe4b9-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fe4b9-116">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="fe4b9-117">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe4b9-117">Namespace</span></span><br/> | <span data-ttu-id="fe4b9-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fe4b9-118">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fe4b9-119">組件</span><span class="sxs-lookup"><span data-stu-id="fe4b9-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fe4b9-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="fe4b9-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4b9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe4b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4b9-122">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fe4b9-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fe4b9-123">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fe4b9-123">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





