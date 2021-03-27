---
title: 動態連結
description: 圖形開發人員有時候會建立大型的一般用途著色器，以供各種不同的場景專案使用。
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673440"
---
# <a name="dynamic-linking"></a><span data-ttu-id="8728a-103">動態連結</span><span class="sxs-lookup"><span data-stu-id="8728a-103">Dynamic Linking</span></span>

<span data-ttu-id="8728a-104">圖形開發人員有時候會建立大型的一般用途著色器，以供各種不同的場景專案使用。</span><span class="sxs-lookup"><span data-stu-id="8728a-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="8728a-105">在執行時間，著色器會有條件地執行適用于特定情況的程式碼。</span><span class="sxs-lookup"><span data-stu-id="8728a-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="8728a-106">可惜的是，這些大型的一般用途著色器會使用一般用途的暫存器 (GPRs) 效率不高，而且可能比較小、更具針對性的著色器慢許多。</span><span class="sxs-lookup"><span data-stu-id="8728a-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="8728a-107">著色器模型5藉由引進動態著色器連結來解決這個效能問題。</span><span class="sxs-lookup"><span data-stu-id="8728a-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="8728a-108">動態連結會使用介面和虛擬函式來分隔著色器程式碼片段，並允許應用程式選取要在繪製時使用的片段。</span><span class="sxs-lookup"><span data-stu-id="8728a-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="8728a-109">這會藉由只系結所需的著色器程式碼，而不是整個大型的一般用途著色器，來改善效能。</span><span class="sxs-lookup"><span data-stu-id="8728a-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8728a-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="8728a-110">In This Section</span></span>



| <span data-ttu-id="8728a-111">項目</span><span class="sxs-lookup"><span data-stu-id="8728a-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="8728a-112">描述</span><span class="sxs-lookup"><span data-stu-id="8728a-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8728a-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[儲存要共用之著色器的變數和類型](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="8728a-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="8728a-114">描述類別連結化物件，用來儲存多個著色器可以共用的變數和類型。</span><span class="sxs-lookup"><span data-stu-id="8728a-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="8728a-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[介面和類別](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="8728a-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="8728a-116">描述如何使用 HLSL 介面和類別來執行動態連結。</span><span class="sxs-lookup"><span data-stu-id="8728a-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="8728a-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[介面使用限制](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="8728a-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="8728a-118">描述在著色器程式碼中使用介面的限制。</span><span class="sxs-lookup"><span data-stu-id="8728a-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="8728a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8728a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8728a-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="8728a-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





