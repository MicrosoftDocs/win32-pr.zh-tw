---
title: 關於 Cdrom 和 CdromCollection 物件
description: 關於 Cdrom 和 CdromCollection 物件
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player、Cdrom 物件
- Windows Media Player 物件模型、Cdrom 物件
- 物件模型、Cdrom 物件
- Windows Media Player ActiveX 控制項、Cdrom 物件
- ActiveX 控制項、Cdrom 物件
- Windows Media Player Mobile ActiveX 控制項、Cdrom 物件
- Windows Media Player Mobile、Cdrom 物件
- Cdrom 物件
- Windows Media Player，CdromCollection 物件
- Windows Media Player 物件模型，CdromCollection 物件
- 物件模型，CdromCollection 物件
- Windows Media Player ActiveX 控制項，CdromCollection 物件
- ActiveX 控制項，CdromCollection 物件
- Windows Media Player 行動 ActiveX 控制項，CdromCollection 物件
- Windows Media Player Mobile，CdromCollection 物件
- CdromCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673800"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="ebaf7-119">關於 Cdrom 和 CdromCollection 物件</span><span class="sxs-lookup"><span data-stu-id="ebaf7-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="ebaf7-120">**Cdrom** 和 **CdromCollection** 物件會管理電腦上的 cd 光碟機介面，以供讀取和播放 cd 之用。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="ebaf7-121">**CdromCollection** 物件只能透過 **Player** 物件的 **CdromCollection** 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="ebaf7-122">**CdromCollection** 屬性會傳回 **cdromCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="ebaf7-123">您只能在建立 **CdromCollection** 物件之後，存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="ebaf7-124">例如，若要使用 **count** 屬性，您必須使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ebaf7-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="ebaf7-125">您只能透過 **CdromCollection** 物件存取 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="ebaf7-126">例如，若要使用 **退出** 方法來退出 CD，您必須先建立集合物件，然後建立物件中的專案。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="ebaf7-127">若要退出 CD，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ebaf7-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="ebaf7-128">在這兩種情況下，您會先建立集合物件 (**CdromCollection**) 然後取得該集合的特定物件。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="ebaf7-129">物件是集合中的第一個專案，也就是對應到第一個 CD 光碟機的 **專案** (0) 。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="ebaf7-130">然後，您可以在該專案上呼叫方法 **退出**。</span><span class="sxs-lookup"><span data-stu-id="ebaf7-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebaf7-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebaf7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebaf7-132">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="ebaf7-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="ebaf7-133">**CdromCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="ebaf7-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ebaf7-134">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="ebaf7-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




