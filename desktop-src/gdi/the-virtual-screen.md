---
description: 所有監視器的周框都是虛擬螢幕。 桌面涵蓋了虛擬畫面，而不是單一監視器。 下圖顯示三個監視器的可能相片順序。
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: 虛擬畫面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991786"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="3c157-105">虛擬畫面</span><span class="sxs-lookup"><span data-stu-id="3c157-105">The Virtual Screen</span></span>

<span data-ttu-id="3c157-106">所有監視器的周框都是 *虛擬螢幕*。</span><span class="sxs-lookup"><span data-stu-id="3c157-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="3c157-107">桌面涵蓋了虛擬畫面，而不是單一監視器。</span><span class="sxs-lookup"><span data-stu-id="3c157-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="3c157-108">下圖顯示三個監視器的可能相片順序。</span><span class="sxs-lookup"><span data-stu-id="3c157-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![顯示三個方塊的圖例，代表在代表虛擬畫面的方塊中排列的監視器](images/multimon-1.png)

<span data-ttu-id="3c157-110">*主要監視器* 包含來源 (0、0) 。</span><span class="sxs-lookup"><span data-stu-id="3c157-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="3c157-111">這是為了與預期監視器具有來源的現有應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="3c157-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="3c157-112">不過，主要監視器不一定要位於虛擬螢幕的左上方。</span><span class="sxs-lookup"><span data-stu-id="3c157-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="3c157-113">在 [圖 1] 中，它位於中央附近。</span><span class="sxs-lookup"><span data-stu-id="3c157-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="3c157-114">當主要監視器不在虛擬畫面的左上方時，虛擬畫面的元件會有負面的座標。</span><span class="sxs-lookup"><span data-stu-id="3c157-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="3c157-115">因為監視的排列是由使用者設定，所以所有應用程式都應該設計為使用負座標。</span><span class="sxs-lookup"><span data-stu-id="3c157-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="3c157-116">如需詳細資訊，請參閱 [舊版程式的多個監視器考慮](multiple-monitor-considerations-for-older-programs.md)。</span><span class="sxs-lookup"><span data-stu-id="3c157-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="3c157-117">虛擬螢幕的座標會以帶正負號的16位值表示，因為許多現有的訊息中包含16位值。</span><span class="sxs-lookup"><span data-stu-id="3c157-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="3c157-118">因此，虛擬畫面的界限如下：</span><span class="sxs-lookup"><span data-stu-id="3c157-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



