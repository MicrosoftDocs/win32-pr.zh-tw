---
title: 標準 DISPID
description: 已針對控制項規格定義一些標準 dispid。
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965165"
---
# <a name="standard-dispids"></a><span data-ttu-id="9036b-103">標準 DISPID</span><span class="sxs-lookup"><span data-stu-id="9036b-103">Standard DISPIDS</span></span>

<span data-ttu-id="9036b-104">已針對控制項規格定義一些標準 dispid。</span><span class="sxs-lookup"><span data-stu-id="9036b-104">A number of standard dispids have been defined for the controls specification.</span></span>

## <a name="dispid_mousepointer"></a><span data-ttu-id="9036b-105">DISPID \_ MOUSEPOINTER</span><span class="sxs-lookup"><span data-stu-id="9036b-105">DISPID\_MOUSEPOINTER</span></span>

<span data-ttu-id="9036b-106">整數類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9036b-106">Property of type integer.</span></span>

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

<span data-ttu-id="9036b-107">Mousepointer 屬性可識別標準的滑鼠圖示。</span><span class="sxs-lookup"><span data-stu-id="9036b-107">The Mousepointer property identifies standard mouse icons.</span></span>



| <span data-ttu-id="9036b-108">值</span><span class="sxs-lookup"><span data-stu-id="9036b-108">Value</span></span>         | <span data-ttu-id="9036b-109">描述</span><span class="sxs-lookup"><span data-stu-id="9036b-109">Description</span></span>                                                                |
|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="9036b-110">0</span><span class="sxs-lookup"><span data-stu-id="9036b-110">0</span></span><br/>  | <span data-ttu-id="9036b-111"> (由物件決定的預設) 圖形。</span><span class="sxs-lookup"><span data-stu-id="9036b-111">(Default) Shape determined by the object.</span></span><br/>                       |
| <span data-ttu-id="9036b-112">1</span><span class="sxs-lookup"><span data-stu-id="9036b-112">1</span></span><br/>  | <span data-ttu-id="9036b-113">箭號</span><span class="sxs-lookup"><span data-stu-id="9036b-113">Arrow</span></span><br/>                                                           |
| <span data-ttu-id="9036b-114">2</span><span class="sxs-lookup"><span data-stu-id="9036b-114">2</span></span><br/>  | <span data-ttu-id="9036b-115">交叉 (交叉線指標) </span><span class="sxs-lookup"><span data-stu-id="9036b-115">Cross (cross-hair pointer)</span></span><br/>                                      |
| <span data-ttu-id="9036b-116">3</span><span class="sxs-lookup"><span data-stu-id="9036b-116">3</span></span><br/>  | <span data-ttu-id="9036b-117">I 無線</span><span class="sxs-lookup"><span data-stu-id="9036b-117">I Beam</span></span><br/>                                                          |
| <span data-ttu-id="9036b-118">4</span><span class="sxs-lookup"><span data-stu-id="9036b-118">4</span></span><br/>  | <span data-ttu-id="9036b-119">方塊內 (小方塊的圖示) </span><span class="sxs-lookup"><span data-stu-id="9036b-119">Icon (small square within a square)</span></span><br/>                             |
| <span data-ttu-id="9036b-120">5</span><span class="sxs-lookup"><span data-stu-id="9036b-120">5</span></span><br/>  | <span data-ttu-id="9036b-121">大小 (四個指向北、南、東和西的箭號) </span><span class="sxs-lookup"><span data-stu-id="9036b-121">Size (four-pointed arrow pointing north, south, east, and west)</span></span><br/> |
| <span data-ttu-id="9036b-122">6</span><span class="sxs-lookup"><span data-stu-id="9036b-122">6</span></span><br/>  | <span data-ttu-id="9036b-123">大小 NE 的 SW (雙箭號指向東北和西南) </span><span class="sxs-lookup"><span data-stu-id="9036b-123">Size NE SW (double arrow pointing northeast and southwest)</span></span><br/>      |
| <span data-ttu-id="9036b-124">7</span><span class="sxs-lookup"><span data-stu-id="9036b-124">7</span></span><br/>  | <span data-ttu-id="9036b-125">大小 N S (雙向箭號指向北和南) </span><span class="sxs-lookup"><span data-stu-id="9036b-125">Size N S (double arrow pointing north and south)</span></span><br/>                |
| <span data-ttu-id="9036b-126">8</span><span class="sxs-lookup"><span data-stu-id="9036b-126">8</span></span><br/>  | <span data-ttu-id="9036b-127">大小 NW、SE</span><span class="sxs-lookup"><span data-stu-id="9036b-127">Size NW, SE</span></span><br/>                                                     |
| <span data-ttu-id="9036b-128">9</span><span class="sxs-lookup"><span data-stu-id="9036b-128">9</span></span><br/>  | <span data-ttu-id="9036b-129">大小 E W (雙向箭號指向東部和西部) </span><span class="sxs-lookup"><span data-stu-id="9036b-129">Size E W (double arrow pointing east and west)</span></span><br/>                  |
| <span data-ttu-id="9036b-130">10</span><span class="sxs-lookup"><span data-stu-id="9036b-130">10</span></span><br/> | <span data-ttu-id="9036b-131">向上箭號</span><span class="sxs-lookup"><span data-stu-id="9036b-131">Up Arrow</span></span><br/>                                                        |
| <span data-ttu-id="9036b-132">11</span><span class="sxs-lookup"><span data-stu-id="9036b-132">11</span></span><br/> | <span data-ttu-id="9036b-133">沙漏 (等候) </span><span class="sxs-lookup"><span data-stu-id="9036b-133">Hourglass (wait)</span></span><br/>                                                |
| <span data-ttu-id="9036b-134">12</span><span class="sxs-lookup"><span data-stu-id="9036b-134">12</span></span><br/> | <span data-ttu-id="9036b-135">不捨棄</span><span class="sxs-lookup"><span data-stu-id="9036b-135">No Drop</span></span><br/>                                                         |
| <span data-ttu-id="9036b-136">13</span><span class="sxs-lookup"><span data-stu-id="9036b-136">13</span></span><br/> | <span data-ttu-id="9036b-137">箭號和沙漏</span><span class="sxs-lookup"><span data-stu-id="9036b-137">Arrow and hourglass</span></span><br/>                                             |
| <span data-ttu-id="9036b-138">14</span><span class="sxs-lookup"><span data-stu-id="9036b-138">14</span></span><br/> | <span data-ttu-id="9036b-139">箭號和問號</span><span class="sxs-lookup"><span data-stu-id="9036b-139">Arrow and question mark</span></span><br/>                                         |
| <span data-ttu-id="9036b-140">15</span><span class="sxs-lookup"><span data-stu-id="9036b-140">15</span></span><br/> | <span data-ttu-id="9036b-141">全部大小</span><span class="sxs-lookup"><span data-stu-id="9036b-141">Size all</span></span><br/>                                                        |
| <span data-ttu-id="9036b-142">99</span><span class="sxs-lookup"><span data-stu-id="9036b-142">99</span></span><br/> | <span data-ttu-id="9036b-143">MouseIcon 屬性指定的自訂圖示</span><span class="sxs-lookup"><span data-stu-id="9036b-143">Custom icon specified by the MouseIcon property</span></span><br/>                 |



 

## <a name="dispid_mouseicon"></a><span data-ttu-id="9036b-144">DISPID \_ MOUSEICON</span><span class="sxs-lookup"><span data-stu-id="9036b-144">DISPID\_MOUSEICON</span></span>

<span data-ttu-id="9036b-145">圖片類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9036b-145">Property of type picture.</span></span>

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a><span data-ttu-id="9036b-146">DISPID \_ 圖</span><span class="sxs-lookup"><span data-stu-id="9036b-146">DISPID\_PICTURE</span></span>

<span data-ttu-id="9036b-147">圖片類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9036b-147">Property of type picture.</span></span>

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a><span data-ttu-id="9036b-148">DISPID \_ 有效</span><span class="sxs-lookup"><span data-stu-id="9036b-148">DISPID\_VALID</span></span>

<span data-ttu-id="9036b-149">用來判斷控制項是否有有效的資料。</span><span class="sxs-lookup"><span data-stu-id="9036b-149">Used to determine if the control has valid data or not.</span></span>

<span data-ttu-id="9036b-150">BOOL 類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="9036b-150">Property of type BOOL.</span></span>

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a><span data-ttu-id="9036b-151">DISPID 的 \_ 環境 \_ 調色板</span><span class="sxs-lookup"><span data-stu-id="9036b-151">DISPID\_ AMBIENT\_PALETTE</span></span>

<span data-ttu-id="9036b-152">用來允許控制項取得容器的 HPAL。</span><span class="sxs-lookup"><span data-stu-id="9036b-152">Used to allow the control to get the container's HPAL.</span></span> <span data-ttu-id="9036b-153">如果容器提供環境調色板，則這是可在前景中實現的唯一調色板。</span><span class="sxs-lookup"><span data-stu-id="9036b-153">If the container supplies an ambient palette then that is the only palette that may be realized into the foreground.</span></span> <span data-ttu-id="9036b-154">想要實現本身調色板的控制項，在背景中必須這樣做。</span><span class="sxs-lookup"><span data-stu-id="9036b-154">Controls that want to realize their own palettes must do so in the background.</span></span> <span data-ttu-id="9036b-155">如果容器未提供任何環境調色板，則現用控制項可以在前景中實現其調色板。</span><span class="sxs-lookup"><span data-stu-id="9036b-155">If there is no ambient palette provided by the container, then the active control can realize its palette in the foreground.</span></span> <span data-ttu-id="9036b-156">在適用于 ActiveX SDK 的 OLE 控制項的調色板行為中，會進一步討論調色板處理。</span><span class="sxs-lookup"><span data-stu-id="9036b-156">Palette handling is further discussed in Palette Behavior for OLE Controls which is in the ActiveX SDK.</span></span>

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





