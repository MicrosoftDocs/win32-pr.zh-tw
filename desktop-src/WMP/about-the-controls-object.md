---
title: 關於控制項物件
description: 關於控制項物件
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player，控制項物件
- Windows Media Player 物件模型，控制項物件
- 物件模型、控制項物件
- Windows Media Player ActiveX 控制項、Controls 物件
- ActiveX 控制項、Controls 物件
- Windows Media Player 的行動 ActiveX 控制項、控制項物件
- Windows Media Player Mobile、Controls 物件
- Controls 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371870"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="daf02-111">關於控制項物件</span><span class="sxs-lookup"><span data-stu-id="daf02-111">About the Controls Object</span></span>

<span data-ttu-id="daf02-112">**Controls** 物件使用像是 **播放** 和 **停止** 的方法，透過控制項來控制數字媒體內容的傳輸。</span><span class="sxs-lookup"><span data-stu-id="daf02-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="daf02-113">它只能透過 **Player** 物件的 **Controls** 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="daf02-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="daf02-114">**Controls** 屬性會傳回 **controls** 物件。</span><span class="sxs-lookup"><span data-stu-id="daf02-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="daf02-115">您只能在建立 **控制項** 物件之後，才存取這些屬性。</span><span class="sxs-lookup"><span data-stu-id="daf02-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="daf02-116">例如，若要使用 **Play** 方法，您必須使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="daf02-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="daf02-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="daf02-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf02-118">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="daf02-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="daf02-119">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="daf02-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




