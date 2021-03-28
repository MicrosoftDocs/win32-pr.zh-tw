---
title: 點大小暫存器
description: 此頂點著色器輸出暫存器包含每個頂點的點大小資料。
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372100"
---
# <a name="point-size-register"></a><span data-ttu-id="8aec3-103">點大小暫存器</span><span class="sxs-lookup"><span data-stu-id="8aec3-103">Point Size Register</span></span>

<span data-ttu-id="8aec3-104">此頂點著色器輸出暫存器包含每個頂點的點大小資料。</span><span class="sxs-lookup"><span data-stu-id="8aec3-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="8aec3-105">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="8aec3-105">Vertex shader versions</span></span> | <span data-ttu-id="8aec3-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="8aec3-106">1\_1</span></span> | <span data-ttu-id="8aec3-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aec3-107">2\_0</span></span> | <span data-ttu-id="8aec3-108">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="8aec3-108">2\_sw</span></span> | <span data-ttu-id="8aec3-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8aec3-109">2\_x</span></span> | <span data-ttu-id="8aec3-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aec3-110">3\_0</span></span> | <span data-ttu-id="8aec3-111">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="8aec3-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="8aec3-112">點大小暫存器</span><span class="sxs-lookup"><span data-stu-id="8aec3-112">Point Size Register</span></span>    | <span data-ttu-id="8aec3-113">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-113">x</span></span>    | <span data-ttu-id="8aec3-114">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-114">x</span></span>    | <span data-ttu-id="8aec3-115">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-115">x</span></span>     | <span data-ttu-id="8aec3-116">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-116">x</span></span>    | <span data-ttu-id="8aec3-117">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-117">x</span></span>    | <span data-ttu-id="8aec3-118">x</span><span class="sxs-lookup"><span data-stu-id="8aec3-118">x</span></span>     |



 

<span data-ttu-id="8aec3-119">暫存器包含的屬性會決定每個註冊的行為。</span><span class="sxs-lookup"><span data-stu-id="8aec3-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="8aec3-120">屬性</span><span class="sxs-lookup"><span data-stu-id="8aec3-120">Property</span></span>        | <span data-ttu-id="8aec3-121">描述</span><span class="sxs-lookup"><span data-stu-id="8aec3-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aec3-122">Name</span><span class="sxs-lookup"><span data-stu-id="8aec3-122">Name</span></span>            | <span data-ttu-id="8aec3-123">選擇</span><span class="sxs-lookup"><span data-stu-id="8aec3-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="8aec3-124">Count</span><span class="sxs-lookup"><span data-stu-id="8aec3-124">Count</span></span>           | <span data-ttu-id="8aec3-125">1個向量，只能使用1個元件，而且必須由元件遮罩指定。</span><span class="sxs-lookup"><span data-stu-id="8aec3-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="8aec3-126">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="8aec3-126">I/O permissions</span></span> | <span data-ttu-id="8aec3-127">唯寫。</span><span class="sxs-lookup"><span data-stu-id="8aec3-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="8aec3-128">只會使用點大小的純量 x 部分。</span><span class="sxs-lookup"><span data-stu-id="8aec3-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aec3-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="8aec3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aec3-130">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="8aec3-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




