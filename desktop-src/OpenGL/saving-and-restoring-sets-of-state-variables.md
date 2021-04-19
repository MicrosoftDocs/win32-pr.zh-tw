---
title: 儲存和還原狀態變數集
description: 您可以使用 glPushAttrib 和 glPopAttrib 函數來儲存和還原屬性堆疊上的狀態變數集合值。
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- OpenGL 狀態變數
- 儲存狀態變數 OpenGL
- 還原狀態變數 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999579"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="97bad-106">儲存和還原狀態變數集</span><span class="sxs-lookup"><span data-stu-id="97bad-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="97bad-107">您可以使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 函數來儲存和還原屬性堆疊上的狀態變數集合值。</span><span class="sxs-lookup"><span data-stu-id="97bad-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="97bad-108">屬性堆疊的深度至少為16。</span><span class="sxs-lookup"><span data-stu-id="97bad-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="97bad-109">若要取得實際的深度，請使用 GL \_ MAX \_ ATTRIB \_ STACK \_ depth with [**glGetIntegerv**](glgetintegerv.md)。</span><span class="sxs-lookup"><span data-stu-id="97bad-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="97bad-110">推送完整堆疊或快顯空的堆疊會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="97bad-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="97bad-111">使用 **glPushAttrib** 和 **glPopAttrib** 的速度通常會比自行取得和還原值更快。</span><span class="sxs-lookup"><span data-stu-id="97bad-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="97bad-112">某些值可能會在硬體中推送和快顯，並儲存和還原這些值可能需要大量資源。</span><span class="sxs-lookup"><span data-stu-id="97bad-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="97bad-113">此外，如果您是在遠端用戶端上操作，則所有屬性資料都必須透過網路連線傳輸，並在儲存和還原時回復。</span><span class="sxs-lookup"><span data-stu-id="97bad-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="97bad-114">不過，您的 OpenGL 執行會將屬性堆疊保留在伺服器上，以避免不必要的網路延遲。</span><span class="sxs-lookup"><span data-stu-id="97bad-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="97bad-115">**GlPushAttrib** 的原型是：</span><span class="sxs-lookup"><span data-stu-id="97bad-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="97bad-116">**void** **glPushAttrib** (**GLbitfield** *mask* ) ;</span><span class="sxs-lookup"><span data-stu-id="97bad-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="97bad-117">使用 [**glPushAttrib**](glpushattrib.md) 會將位指定的所有屬性（attribute）推送至屬性堆疊，以儲存 *遮罩* 中的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="97bad-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="97bad-118">如需您可以邏輯或一起儲存任何屬性組合的可能遮罩位清單，請參閱 [屬性群組](attribute-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="97bad-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="97bad-119">每個位都對應到個別狀態變數的集合。</span><span class="sxs-lookup"><span data-stu-id="97bad-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="97bad-120">例如，GL \_ 照明 \_ 位指的是與光源相關的所有狀態變數，包括目前的材質色彩、環境、擴散、反射和發出的燈光、已啟用的燈清單，以及聚光燈的方向。</span><span class="sxs-lookup"><span data-stu-id="97bad-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="97bad-121">當您呼叫 [**glPopAttrib**](glpopattrib.md)時，所有這些變數都會還原。</span><span class="sxs-lookup"><span data-stu-id="97bad-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="97bad-122">若要找出針對特定遮罩值所儲存的屬性，請參閱 [OpenGL 狀態變數](opengl-state-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="97bad-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




