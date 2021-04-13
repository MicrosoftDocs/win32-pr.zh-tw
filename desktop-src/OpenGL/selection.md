---
title: 選取
description: 選取範圍會傳回名稱堆疊的目前內容，這是具有整數值的名稱陣列。
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- 選取模式 OpenGL
- 選取範圍命中 OpenGL
- 命中記錄 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301215"
---
# <a name="selection"></a><span data-ttu-id="edabd-106">選取</span><span class="sxs-lookup"><span data-stu-id="edabd-106">Selection</span></span>

<span data-ttu-id="edabd-107">選取範圍會傳回名稱堆疊的目前內容，這是具有整數值的名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="edabd-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="edabd-108">您可以指派名稱，並在模型程式碼內建立名稱堆疊，以指定您想要繪製之物件的幾何。</span><span class="sxs-lookup"><span data-stu-id="edabd-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="edabd-109">然後，在 [選取] 模式中，每當基本型別與剪輯磁片區相交時，就會發生選取的點擊。</span><span class="sxs-lookup"><span data-stu-id="edabd-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="edabd-110">點擊記錄會寫入至您在 [**glSelectBuffer**](glselectbuffer.md)中提供的選取範圍陣列，其中包含在叫用時，名稱堆疊內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="edabd-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="edabd-111">先呼叫 [**glSelectBuffer**](glselectbuffer.md) ，然後再使用 [**glRenderMode**](glrendermode.md)讓 OpenGL 進入選取模式。</span><span class="sxs-lookup"><span data-stu-id="edabd-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="edabd-112">在您呼叫 **glRenderMode** 讓 OpenGL 離開選取模式之前，不保證會傳回完整的名稱堆疊內容。</span><span class="sxs-lookup"><span data-stu-id="edabd-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="edabd-113">使用 [**glInitNames**](glinitnames.md)、 [**glLoadName**](glloadname.md)、 [**glPushName**](glpushname.md)和 [**glPopName**](glpopname.md)操作名稱堆疊。</span><span class="sxs-lookup"><span data-stu-id="edabd-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="edabd-114">您也可以使用 [**gluPickMatrix**](glupickmatrix.md) 來進行選取。</span><span class="sxs-lookup"><span data-stu-id="edabd-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




