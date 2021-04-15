---
title: 接聽屬性
description: 接聽屬性
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player 的外觀，接聽屬性
- 外觀，接聽屬性
- 外觀的參考，接聽屬性
- 接聽屬性
- 屬性，接聽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507173"
---
# <a name="listening-attributes"></a><span data-ttu-id="ba3e5-108">接聽屬性</span><span class="sxs-lookup"><span data-stu-id="ba3e5-108">Listening Attributes</span></span>

<span data-ttu-id="ba3e5-109">接聽屬性是用來將某個屬性連接到另一個屬性，讓它的值會在每次其他屬性的值變更時變更。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="ba3e5-110">接聽屬性 **wmpprop：** 是最有用的。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="ba3e5-111">如果有一個屬性的值指定為 **wmpprop：** 第二個屬性，則第一個值會自動更新，以反映第二個值變更時的第二個值。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="ba3e5-112">**範例︰**</span><span class="sxs-lookup"><span data-stu-id="ba3e5-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="ba3e5-113">如此一來，mySlider 的值（顯示于滑杆控制項的位置）也可以在文字方塊內顯示為數字。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="ba3e5-114">您可以使用其他兩個接聽屬性 **wmpenabled：** 和 **wmpdisabled：** 來變更控制項的 **已啟用** 屬性，視播放程式中目前是否有可用的功能而定。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="ba3e5-115">這些屬性只能接聽 **Controls** 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="ba3e5-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="ba3e5-116">**範例︰**</span><span class="sxs-lookup"><span data-stu-id="ba3e5-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="ba3e5-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba3e5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba3e5-118">**雜項**</span><span class="sxs-lookup"><span data-stu-id="ba3e5-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




