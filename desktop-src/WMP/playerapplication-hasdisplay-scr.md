---
title: PLAYERAPPLICATION. hasDisplay 屬性
description: HasDisplay 屬性會抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項來顯示。
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976034"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="b4e87-104">PLAYERAPPLICATION.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="b4e87-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="b4e87-105">**HasDisplay** 屬性會抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項來顯示。</span><span class="sxs-lookup"><span data-stu-id="b4e87-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="b4e87-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="b4e87-106">Possible Values</span></span>

<span data-ttu-id="b4e87-107">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b4e87-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="b4e87-108">值</span><span class="sxs-lookup"><span data-stu-id="b4e87-108">Value</span></span> | <span data-ttu-id="b4e87-109">描述</span><span class="sxs-lookup"><span data-stu-id="b4e87-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="b4e87-110">True</span><span class="sxs-lookup"><span data-stu-id="b4e87-110">True</span></span>  | <span data-ttu-id="b4e87-111">影片可以顯示。</span><span class="sxs-lookup"><span data-stu-id="b4e87-111">The video can display.</span></span>    |
| <span data-ttu-id="b4e87-112">否</span><span class="sxs-lookup"><span data-stu-id="b4e87-112">False</span></span> | <span data-ttu-id="b4e87-113">影片無法顯示。</span><span class="sxs-lookup"><span data-stu-id="b4e87-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4e87-114">備註</span><span class="sxs-lookup"><span data-stu-id="b4e87-114">Remarks</span></span>

<span data-ttu-id="b4e87-115">只有在遠端 Windows Media Player 控制項時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b4e87-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="b4e87-116">您可以同時在遠端執行數個 Windows Media Player 控制項，但影片在播放程式的完整模式或其中一個遠端控制項中，一次只能顯示在一個位置。</span><span class="sxs-lookup"><span data-stu-id="b4e87-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="b4e87-117">您可以使用這個屬性來判斷目前的控制項是否為可顯示影片的控制項。</span><span class="sxs-lookup"><span data-stu-id="b4e87-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e87-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4e87-118">Requirements</span></span>



| <span data-ttu-id="b4e87-119">需求</span><span class="sxs-lookup"><span data-stu-id="b4e87-119">Requirement</span></span> | <span data-ttu-id="b4e87-120">值</span><span class="sxs-lookup"><span data-stu-id="b4e87-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b4e87-121">版本</span><span class="sxs-lookup"><span data-stu-id="b4e87-121">Version</span></span><br/> | <span data-ttu-id="b4e87-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b4e87-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4e87-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4e87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e87-124">**PLAYERAPPLICATION 元素**</span><span class="sxs-lookup"><span data-stu-id="b4e87-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="b4e87-125">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="b4e87-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





