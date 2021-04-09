---
title: OpenGL 函數名稱
description: 許多 OpenGL 函式都是彼此的變化，大多不同于其引數的資料類型。
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL、函數名稱
- 函數名稱 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673271"
---
# <a name="opengl-function-names"></a><span data-ttu-id="80f8e-105">OpenGL 函數名稱</span><span class="sxs-lookup"><span data-stu-id="80f8e-105">OpenGL Function Names</span></span>

<span data-ttu-id="80f8e-106">許多 OpenGL 函式都是彼此的變化，大多不同于其引數的資料類型。</span><span class="sxs-lookup"><span data-stu-id="80f8e-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="80f8e-107">某些函式的相關引數數目，以及這些引數是否可指定為向量或必須在清單中分開指定。</span><span class="sxs-lookup"><span data-stu-id="80f8e-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="80f8e-108">例如，如果您使用 **glVertex2f** 函式，您必須提供 x 和 y 座標作為32位浮點數;使用 **glVertex3sv** 時，您必須為 x、y 和 z 提供三個簡短 (16 位) 整數值的陣列。</span><span class="sxs-lookup"><span data-stu-id="80f8e-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="80f8e-109">接下來的主題只會使用函式的基底名稱。</span><span class="sxs-lookup"><span data-stu-id="80f8e-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="80f8e-110">星號表示實際的函式名稱可能會比顯示的還多。</span><span class="sxs-lookup"><span data-stu-id="80f8e-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="80f8e-111">例如， [glVertex \*](glvertex-functions.md)代表您用來指定頂點的函式的所有變化： **glVertex2d**、 **glVertex2f**、 **glVertex2i** 等等。</span><span class="sxs-lookup"><span data-stu-id="80f8e-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="80f8e-112">OpenGL 函式的效果會根據是否啟用特定模式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="80f8e-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="80f8e-113">例如，如果光源相關的函式要產生適當的發亮物件，您就必須啟用光源。</span><span class="sxs-lookup"><span data-stu-id="80f8e-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="80f8e-114">若要啟用特定模式，請使用 [**glEnable**](glenable.md) 函式，並提供適當的常數來識別 (例如 GL \_ 照明) 的模式。</span><span class="sxs-lookup"><span data-stu-id="80f8e-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="80f8e-115">若要停用模式，請使用 [**glDisable**](gldisable.md)。</span><span class="sxs-lookup"><span data-stu-id="80f8e-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="80f8e-116">如需可啟用之模式的完整清單，請參閱 **glEnable** 。</span><span class="sxs-lookup"><span data-stu-id="80f8e-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




