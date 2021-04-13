---
title: '全域屬性 (Windows Media Player SDK) '
description: 全域屬性
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player 的外觀、全域屬性
- 外觀，全域屬性
- 外觀、全域屬性的參考
- 全域屬性
- 屬性，全域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104373667"
---
# <a name="global-attributes"></a><span data-ttu-id="37b79-108">全域屬性</span><span class="sxs-lookup"><span data-stu-id="37b79-108">Global Attributes</span></span>

<span data-ttu-id="37b79-109">全域屬性是一種屬性，可讓您輕鬆存取面板內任何位置的特定播放機元素或物件。</span><span class="sxs-lookup"><span data-stu-id="37b79-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="37b79-110">**Player** global 屬性是 [player](player-object.md)物件的參考，可用來存取 Windows Media Player 的主要功能。</span><span class="sxs-lookup"><span data-stu-id="37b79-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="37b79-111">下列範例會使用 **player** 開始播放數位媒體播放。</span><span class="sxs-lookup"><span data-stu-id="37b79-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="37b79-112">**主題** 全域屬性是 [主題](theme-element.md)元素的參考。</span><span class="sxs-lookup"><span data-stu-id="37b79-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="37b79-113">這是存取 **主題** 屬性的適當方式，而不是在 **主題** 元素內指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="37b79-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="37b79-114">下列範例會使用 **主題** 來開啟新的視圖。</span><span class="sxs-lookup"><span data-stu-id="37b79-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="37b79-115">**View** global 屬性是目前 [視圖](view-element.md)的參考。</span><span class="sxs-lookup"><span data-stu-id="37b79-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="37b79-116">這可以用來取代在不同 **VIEW** 元素內指定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37b79-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="37b79-117">下列範例會使用 **view** 來關閉目前的視圖。</span><span class="sxs-lookup"><span data-stu-id="37b79-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="37b79-118">**事件** 全域屬性是用來從事件處理常式記憶體取環境事件屬性。</span><span class="sxs-lookup"><span data-stu-id="37b79-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="37b79-119">下列範例會使用 **事件** ，判斷按一下按鈕時是否按下 ALT 鍵。</span><span class="sxs-lookup"><span data-stu-id="37b79-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="37b79-120">**PlayerApplication** global 屬性是 [playerApplication](playerapplication-object.md)物件的參考，而且會由提供作為遠端播放機控制項之自訂使用者介面的外觀檔案使用。</span><span class="sxs-lookup"><span data-stu-id="37b79-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="37b79-121">只有在執行 **IWMPRemoteMediaServices** 介面的 c + + 程式中，才能將 Player 控制項內嵌在遠端模式中。</span><span class="sxs-lookup"><span data-stu-id="37b79-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="37b79-122">下列範例會使用 **playerApplication** 切換到播放程式的完整模式。</span><span class="sxs-lookup"><span data-stu-id="37b79-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="37b79-123">如需詳細資訊，請參閱 [環境事件屬性](ambient-event-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="37b79-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37b79-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="37b79-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37b79-125">**雜項**</span><span class="sxs-lookup"><span data-stu-id="37b79-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




