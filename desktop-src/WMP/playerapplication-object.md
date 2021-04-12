---
title: PlayerApplication 物件
description: PlayerApplication 物件提供一種方式，可協調遠端 Windows Media Player 控制項與 Windows Media Player 的完整模式之間的切換。
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- PlayerApplication 物件 Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313244"
---
# <a name="playerapplication-object"></a><span data-ttu-id="68c42-104">PlayerApplication 物件</span><span class="sxs-lookup"><span data-stu-id="68c42-104">PlayerApplication Object</span></span>

<span data-ttu-id="68c42-105">**PlayerApplication** 物件提供一種方式，可協調遠端 Windows Media Player 控制項與 Windows Media Player 的完整模式之間的切換。</span><span class="sxs-lookup"><span data-stu-id="68c42-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="68c42-106">此物件僅適用于執行 **IWMPRemoteMediaServices** 介面的 c + + 程式，並在遠端模式中內嵌播放機控制項。</span><span class="sxs-lookup"><span data-stu-id="68c42-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="68c42-107">用來作為遠端 Windows Media Player 控制項自訂介面的面板檔案會透過 **playerApplication** 全域屬性，在腳本中存取這個物件。</span><span class="sxs-lookup"><span data-stu-id="68c42-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="68c42-108">**PlayerApplication** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="68c42-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="68c42-109">屬性</span><span class="sxs-lookup"><span data-stu-id="68c42-109">Property</span></span>                                           | <span data-ttu-id="68c42-110">描述</span><span class="sxs-lookup"><span data-stu-id="68c42-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68c42-111">hasDisplay</span><span class="sxs-lookup"><span data-stu-id="68c42-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="68c42-112">抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項顯示。</span><span class="sxs-lookup"><span data-stu-id="68c42-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="68c42-113">playerDocked</span><span class="sxs-lookup"><span data-stu-id="68c42-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="68c42-114">抓取值，指出 Windows Media Player 是否處於停駐狀態。</span><span class="sxs-lookup"><span data-stu-id="68c42-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="68c42-115">**PlayerApplication** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="68c42-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="68c42-116">方法</span><span class="sxs-lookup"><span data-stu-id="68c42-116">Method</span></span>                                                                       | <span data-ttu-id="68c42-117">描述</span><span class="sxs-lookup"><span data-stu-id="68c42-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="68c42-118">switchToControl</span><span class="sxs-lookup"><span data-stu-id="68c42-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="68c42-119">將遠端 Windows Media Player 控制項切換至停駐的狀態。</span><span class="sxs-lookup"><span data-stu-id="68c42-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="68c42-120">switchToPlayerApplication</span><span class="sxs-lookup"><span data-stu-id="68c42-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="68c42-121">將遠端 Windows Media Player 控制項切換至播放程式的完整模式。</span><span class="sxs-lookup"><span data-stu-id="68c42-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="68c42-122">**PlayerApplication** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="68c42-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="68c42-123">Object</span><span class="sxs-lookup"><span data-stu-id="68c42-123">Object</span></span>                      | <span data-ttu-id="68c42-124">屬性</span><span class="sxs-lookup"><span data-stu-id="68c42-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="68c42-125">球員</span><span class="sxs-lookup"><span data-stu-id="68c42-125">Player</span></span>](player-object.md) | [<span data-ttu-id="68c42-126">playerApplication</span><span class="sxs-lookup"><span data-stu-id="68c42-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="68c42-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c42-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c42-128">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="68c42-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="68c42-129">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="68c42-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




