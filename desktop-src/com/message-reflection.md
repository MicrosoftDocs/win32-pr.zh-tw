---
title: 訊息反映
description: 訊息反映
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020769"
---
# <a name="message-reflection"></a><span data-ttu-id="33dcb-103">訊息反映</span><span class="sxs-lookup"><span data-stu-id="33dcb-103">Message Reflection</span></span>

<span data-ttu-id="33dcb-104">強烈建議 ActiveX 控制項容器支援訊息反映。</span><span class="sxs-lookup"><span data-stu-id="33dcb-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="33dcb-105">這會讓子類別化控制項更有效率地運作。</span><span class="sxs-lookup"><span data-stu-id="33dcb-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="33dcb-106">如果支援訊息反映，則必須支援 MessageReflect 環境屬性，並將值 **設為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="33dcb-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="33dcb-107">如果容器不會執行訊息反映，則 OLE CDK 會為每個子類別化控制項建立兩個視窗，以代表控制項容器提供訊息反映。</span><span class="sxs-lookup"><span data-stu-id="33dcb-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33dcb-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="33dcb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33dcb-109">容器</span><span class="sxs-lookup"><span data-stu-id="33dcb-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




