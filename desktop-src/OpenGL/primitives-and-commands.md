---
title: 基本和命令
description: 基本和命令
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL、基本
- OpenGL、命令
- 基本 OpenGL
- 命令 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672507"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="20e42-107">基本和命令</span><span class="sxs-lookup"><span data-stu-id="20e42-107">Primitives and Commands</span></span>

<span data-ttu-id="20e42-108">OpenGL 會繪製 *基本* 點、線段或 polygonssubject 至數個可選取的模式。</span><span class="sxs-lookup"><span data-stu-id="20e42-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="20e42-109">您可以單獨控制模式。</span><span class="sxs-lookup"><span data-stu-id="20e42-109">You can control modes independently of one another.</span></span> <span data-ttu-id="20e42-110">也就是說，設定一個模式不會影響是否已設定其他模式 (雖然許多模式可能會進行互動，以判斷最終畫面格緩衝區) 的結果。</span><span class="sxs-lookup"><span data-stu-id="20e42-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="20e42-111">若要指定基本、設定模式和執行其他 OpenGL 作業，請以函式呼叫的形式發出命令。</span><span class="sxs-lookup"><span data-stu-id="20e42-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="20e42-112">基本專案是由一或多個 *頂點* 的群組所定義。</span><span class="sxs-lookup"><span data-stu-id="20e42-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="20e42-113">頂點會定義點、線條的端點，或兩個邊符合的多邊形角落。</span><span class="sxs-lookup"><span data-stu-id="20e42-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="20e42-114">由頂點座標、色彩、法線、材質座標和邊緣旗標所組成的資料 () 與頂點相關聯，而且每個頂點和其相關聯的資料會以相同方式分別以連續處理。</span><span class="sxs-lookup"><span data-stu-id="20e42-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="20e42-115">這項規則的唯一例外狀況是必須裁剪頂點群組，讓特定的基本型別符合指定區域的情況。</span><span class="sxs-lookup"><span data-stu-id="20e42-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="20e42-116">在此情況下，可能會修改頂點資料並建立新頂點。</span><span class="sxs-lookup"><span data-stu-id="20e42-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="20e42-117">裁剪的類型取決於頂點群組所代表的基本物件。</span><span class="sxs-lookup"><span data-stu-id="20e42-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="20e42-118">命令一律會依照接收的順序進行處理，但在命令生效之前可能會有不定的延遲。</span><span class="sxs-lookup"><span data-stu-id="20e42-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="20e42-119">這表示每個基本型別會在任何後續的命令生效之前完全繪製。</span><span class="sxs-lookup"><span data-stu-id="20e42-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="20e42-120">這也表示狀態查詢命令會傳回與所有先前發行之 OpenGL 命令的完整執行一致的資料。</span><span class="sxs-lookup"><span data-stu-id="20e42-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




