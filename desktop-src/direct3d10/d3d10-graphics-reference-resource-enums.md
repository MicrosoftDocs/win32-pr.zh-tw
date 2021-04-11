---
description: 下列列舉是用來指定在轉譯期間如何建立和存取資源的相關資訊。
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: " (Direct3D 10 圖形) 的資源列舉"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026022"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="a8938-103"> (Direct3D 10 圖形) 的資源列舉</span><span class="sxs-lookup"><span data-stu-id="a8938-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="a8938-104">下列列舉是用來指定在轉譯期間如何建立和存取資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a8938-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="a8938-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="a8938-105">Enumeration</span></span>                                                     | <span data-ttu-id="a8938-106">描述</span><span class="sxs-lookup"><span data-stu-id="a8938-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8938-107">**D3D10 系結 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a8938-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="a8938-108">識別管線將如何使用資源，並判斷資源可系結 () 的管線階段。</span><span class="sxs-lookup"><span data-stu-id="a8938-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="a8938-109">**D3D10 \_ CPU \_ 存取 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a8938-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="a8938-110">指定資源允許的 CPU 存取類型。</span><span class="sxs-lookup"><span data-stu-id="a8938-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="a8938-111">**D3D10 \_ DSV \_ 維度**</span><span class="sxs-lookup"><span data-stu-id="a8938-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="a8938-112">指定如何存取深度範本視圖中使用的資源。</span><span class="sxs-lookup"><span data-stu-id="a8938-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="a8938-113">**D3D10 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="a8938-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="a8938-114">識別要對應以供 CPU 讀取和寫入的資源。</span><span class="sxs-lookup"><span data-stu-id="a8938-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="a8938-115">**D3D10 \_ 對應 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a8938-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="a8938-116">指定當 GPU 尚未完成資源時，CPU 應該如何回應任何對應方法。</span><span class="sxs-lookup"><span data-stu-id="a8938-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="a8938-117">**D3D10 \_ 資源 \_ 維度**</span><span class="sxs-lookup"><span data-stu-id="a8938-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="a8938-118">識別使用中的資源類型。</span><span class="sxs-lookup"><span data-stu-id="a8938-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="a8938-119">**D3D10 \_ 資源 \_ 其他 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a8938-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="a8938-120">識別較不常見的資源建立選項。</span><span class="sxs-lookup"><span data-stu-id="a8938-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="a8938-121">**D3D10 \_ RTV \_ 維度**</span><span class="sxs-lookup"><span data-stu-id="a8938-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="a8938-122">指定如何存取呈現目標視圖中使用的資源。</span><span class="sxs-lookup"><span data-stu-id="a8938-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="a8938-123">**D3D10 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="a8938-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="a8938-124">識別 CPU 和/或 GPU 應如何讀取和寫入資源。</span><span class="sxs-lookup"><span data-stu-id="a8938-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="a8938-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8938-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8938-126">資源參考</span><span class="sxs-lookup"><span data-stu-id="a8938-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



