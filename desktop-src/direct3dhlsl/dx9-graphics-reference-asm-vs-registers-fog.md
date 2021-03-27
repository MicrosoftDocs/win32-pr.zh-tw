---
title: 霧化暫存器
description: 此頂點著色器輸出暫存器包含每個頂點的霧化色彩。
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971424"
---
# <a name="fog-register"></a><span data-ttu-id="21b8e-103">霧化暫存器</span><span class="sxs-lookup"><span data-stu-id="21b8e-103">Fog Register</span></span>

<span data-ttu-id="21b8e-104">此頂點著色器輸出暫存器包含每個頂點的霧化色彩。</span><span class="sxs-lookup"><span data-stu-id="21b8e-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="21b8e-105">暫存器包含的屬性會決定每個註冊的行為。</span><span class="sxs-lookup"><span data-stu-id="21b8e-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="21b8e-106">屬性</span><span class="sxs-lookup"><span data-stu-id="21b8e-106">Property</span></span>        | <span data-ttu-id="21b8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="21b8e-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b8e-108">Name</span><span class="sxs-lookup"><span data-stu-id="21b8e-108">Name</span></span>            | <span data-ttu-id="21b8e-109">oFog</span><span class="sxs-lookup"><span data-stu-id="21b8e-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="21b8e-110">Count</span><span class="sxs-lookup"><span data-stu-id="21b8e-110">Count</span></span>           | <span data-ttu-id="21b8e-111">一個向量，其中只可使用一個元件，而且必須由元件遮罩指定</span><span class="sxs-lookup"><span data-stu-id="21b8e-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="21b8e-112">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="21b8e-112">I/O permissions</span></span> | <span data-ttu-id="21b8e-113">唯寫。</span><span class="sxs-lookup"><span data-stu-id="21b8e-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="21b8e-114">輸出霧化值會註冊。</span><span class="sxs-lookup"><span data-stu-id="21b8e-114">The output fog value registers.</span></span> <span data-ttu-id="21b8e-115">值是要插入的霧化因數，然後路由傳送至霧化資料表。</span><span class="sxs-lookup"><span data-stu-id="21b8e-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="21b8e-116">只會使用霧化的純量 x 元件。</span><span class="sxs-lookup"><span data-stu-id="21b8e-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21b8e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="21b8e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21b8e-118">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="21b8e-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




