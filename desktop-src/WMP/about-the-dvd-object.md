---
title: 關於 DVD 物件
description: 關於 DVD 物件
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player、DVD 物件
- Windows Media Player 物件模型、DVD 物件
- 物件模型、DVD 物件
- Windows Media Player ActiveX 控制項、DVD 物件
- ActiveX 控制項、DVD 物件
- Windows Media Player Mobile ActiveX 控制項、DVD 物件
- Windows Media Player Mobile、DVD 物件
- DVD 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300140"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="77c11-111">關於 DVD 物件</span><span class="sxs-lookup"><span data-stu-id="77c11-111">About the DVD Object</span></span>

<span data-ttu-id="77c11-112">**Dvd** 物件會新增 dvd 媒體的特定功能。</span><span class="sxs-lookup"><span data-stu-id="77c11-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="77c11-113">一般而言，DVD 媒體的處理方式就像 Windows Media Player 中的其他數位媒體一樣。</span><span class="sxs-lookup"><span data-stu-id="77c11-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="77c11-114">比方說，DVD 光碟機是使用 **CdromCollection** 物件來列舉，而 dvd 標題和章節則是使用 **播放清單** 物件和 **媒體** 物件來操作。</span><span class="sxs-lookup"><span data-stu-id="77c11-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="77c11-115">有些功能是 DVD 專用的，而 **dvd** 物件則提供此功能。</span><span class="sxs-lookup"><span data-stu-id="77c11-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="77c11-116">例如，DVD 的概念稱為「網域」。</span><span class="sxs-lookup"><span data-stu-id="77c11-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="77c11-117">若要取出 DVD 媒體的目前網域，請輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="77c11-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="77c11-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="77c11-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c11-119">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="77c11-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="77c11-120">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="77c11-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




