---
title: 變更屬性值
description: 變更屬性值
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，變更值
- 變更屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021599"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="ceb41-114">變更屬性值</span><span class="sxs-lookup"><span data-stu-id="ceb41-114">Changing Attribute Values</span></span>

<span data-ttu-id="ceb41-115">如果您的網頁或應用程式具有程式庫的讀取/寫入權限，而且可以讀取和寫入屬性，則可以變更屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ceb41-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="ceb41-116">您可以變更目前媒體專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb41-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="ceb41-117">若要變更多個媒體專案的屬性，您可以將每個媒體專案依次指派給 *播放* 程式。**currentMedia** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb41-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="ceb41-118">在本主題中， **Player** 物件是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="ceb41-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="ceb41-119">若要變更屬性，請呼叫 *Player*。*currentMedia*。**setItemInfo** 方法，如下列 c # 範例所示。</span><span class="sxs-lookup"><span data-stu-id="ceb41-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="ceb41-120">建議您呼叫 *媒體*。**isReadOnlyItem** 方法來判斷您是否可以變更特定屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb41-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="ceb41-121">如果您將控制項內嵌在您的應用程式中，除非使用者執行 Windows Media Player，否則您變更的檔案屬性不會寫入數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ceb41-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="ceb41-122">如果您在以 c + + 撰寫的遠端應用程式中使用控制項，則在進行變更之後，將會立即將您變更的檔案屬性寫入數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ceb41-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="ceb41-123">無論是哪一種情況，您都可以透過程式庫立即使用變更。</span><span class="sxs-lookup"><span data-stu-id="ceb41-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ceb41-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ceb41-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb41-125">**媒體專案屬性**</span><span class="sxs-lookup"><span data-stu-id="ceb41-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="ceb41-126">**程式庫存取**</span><span class="sxs-lookup"><span data-stu-id="ceb41-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="ceb41-127">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="ceb41-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ceb41-128">**讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="ceb41-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




