---
title: PLAYERAPPLICATION. playerDocked 屬性
description: PlayerDocked 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。
ms.assetid: 8b95da72-037b-4179-a564-fc9bc63368ac
keywords:
- PLAYERAPPLICATION. playerDocked Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.playerDocked
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21abe3dd5cb14906db39e8eb50a1d18302a92ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994086"
---
# <a name="playerapplicationplayerdocked"></a><span data-ttu-id="3c32e-104">PLAYERAPPLICATION.playerDocked</span><span class="sxs-lookup"><span data-stu-id="3c32e-104">PLAYERAPPLICATION.playerDocked</span></span>

<span data-ttu-id="3c32e-105">**PlayerDocked** 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。</span><span class="sxs-lookup"><span data-stu-id="3c32e-105">The **playerDocked** attribute retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>

``` syntax
        elementID.playerDocked
```

## <a name="possible-values"></a><span data-ttu-id="3c32e-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="3c32e-106">Possible Values</span></span>

<span data-ttu-id="3c32e-107">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="3c32e-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="3c32e-108">值</span><span class="sxs-lookup"><span data-stu-id="3c32e-108">Value</span></span> | <span data-ttu-id="3c32e-109">描述</span><span class="sxs-lookup"><span data-stu-id="3c32e-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="3c32e-110">True</span><span class="sxs-lookup"><span data-stu-id="3c32e-110">True</span></span>  | <span data-ttu-id="3c32e-111">Windows Media Player 固定。</span><span class="sxs-lookup"><span data-stu-id="3c32e-111">Windows Media Player is docked.</span></span>   |
| <span data-ttu-id="3c32e-112">否</span><span class="sxs-lookup"><span data-stu-id="3c32e-112">False</span></span> | <span data-ttu-id="3c32e-113">Windows Media Player 未移除。</span><span class="sxs-lookup"><span data-stu-id="3c32e-113">Windows Media Player is undocked.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3c32e-114">備註</span><span class="sxs-lookup"><span data-stu-id="3c32e-114">Remarks</span></span>

<span data-ttu-id="3c32e-115">只有在遠端 Windows Media Player 控制項時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3c32e-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c32e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c32e-116">Requirements</span></span>



| <span data-ttu-id="3c32e-117">需求</span><span class="sxs-lookup"><span data-stu-id="3c32e-117">Requirement</span></span> | <span data-ttu-id="3c32e-118">值</span><span class="sxs-lookup"><span data-stu-id="3c32e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3c32e-119">版本</span><span class="sxs-lookup"><span data-stu-id="3c32e-119">Version</span></span><br/> | <span data-ttu-id="3c32e-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3c32e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c32e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c32e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c32e-122">**PLAYERAPPLICATION 元素**</span><span class="sxs-lookup"><span data-stu-id="3c32e-122">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="3c32e-123">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="3c32e-123">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





