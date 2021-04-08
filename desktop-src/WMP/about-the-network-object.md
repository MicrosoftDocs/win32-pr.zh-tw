---
title: 關於 Network 物件
description: 關於 Network 物件
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player、Network 物件
- Windows Media Player 物件模型、Network 物件
- 物件模型，網路物件
- Windows Media Player ActiveX 控制項、Network 物件
- ActiveX 控制項、Network 物件
- Windows Media Player 的行動 ActiveX 控制項、Network 物件
- Windows Media Player Mobile、Network 物件
- Network 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671400"
---
# <a name="about-the-network-object"></a><span data-ttu-id="be453-111">關於 Network 物件</span><span class="sxs-lookup"><span data-stu-id="be453-111">About the Network Object</span></span>

<span data-ttu-id="be453-112">**Network** 物件管理的屬性可讓您決定內容透過網路進行串流的程度。</span><span class="sxs-lookup"><span data-stu-id="be453-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="be453-113">例如，您可以找出封包是否遺失，並採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="be453-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="be453-114">只有透過 **Player** 物件的 **network** 屬性才能存取 **network** 物件。</span><span class="sxs-lookup"><span data-stu-id="be453-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="be453-115">**Network** 屬性會傳回 **network** 物件。</span><span class="sxs-lookup"><span data-stu-id="be453-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="be453-116">您只能在建立 **網路** 物件的屬性之後，才存取這些屬性。</span><span class="sxs-lookup"><span data-stu-id="be453-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="be453-117">例如，若要使用 **頻寬** 屬性，您必須使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="be453-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="be453-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="be453-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be453-119">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="be453-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="be453-120">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="be453-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




