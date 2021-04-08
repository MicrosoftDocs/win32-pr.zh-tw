---
title: 使用顯示清單
description: 使用顯示清單
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL、顯示清單
- 顯示清單 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839700"
---
# <a name="using-display-lists"></a><span data-ttu-id="62bf8-105">使用顯示清單</span><span class="sxs-lookup"><span data-stu-id="62bf8-105">Using Display Lists</span></span>

<span data-ttu-id="62bf8-106">顯示清單是已儲存以供後續執行的 OpenGL 函數群組。</span><span class="sxs-lookup"><span data-stu-id="62bf8-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="62bf8-107">[**GlNewList**](glnewlist.md)函式會開始建立顯示清單，而 [**glEndList**](glendlist.md)會將它結束。</span><span class="sxs-lookup"><span data-stu-id="62bf8-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="62bf8-108">除了少數例外，在 **glNewList** 和 **glEndList** 之間呼叫的 OpenGL 函式會附加至顯示清單。</span><span class="sxs-lookup"><span data-stu-id="62bf8-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="62bf8-109"> (請參閱 **glNewList** ，以取得您無法在顯示清單中儲存及執行的函式清單。 ) 若要觸發清單或清單集的執行，請使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) ，並提供特定清單或清單的識別編號。</span><span class="sxs-lookup"><span data-stu-id="62bf8-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="62bf8-110">您可以使用 [**glGenLists**](glgenlists.md)、 [**glListBase**](gllistbase.md)和 [**glIsList**](glislist.md)來管理用來識別顯示清單的索引。</span><span class="sxs-lookup"><span data-stu-id="62bf8-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="62bf8-111">若要刪除一組顯示清單，請使用 [**glDeleteLists**](gldeletelists.md)。</span><span class="sxs-lookup"><span data-stu-id="62bf8-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62bf8-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="62bf8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62bf8-113">顯示清單參考</span><span class="sxs-lookup"><span data-stu-id="62bf8-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




