---
description: 描述裝置所支援之頂點資料類型的常數。
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343230"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="0f025-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="0f025-103">D3DDTCAPS</span></span>

<span data-ttu-id="0f025-104">描述裝置所支援之頂點資料類型的常數。</span><span class="sxs-lookup"><span data-stu-id="0f025-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="0f025-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="0f025-105">\#define</span></span>              | <span data-ttu-id="0f025-106">值</span><span class="sxs-lookup"><span data-stu-id="0f025-106">Value</span></span>       | <span data-ttu-id="0f025-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f025-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f025-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="0f025-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="0f025-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="0f025-109">0x00000001L</span></span> | <span data-ttu-id="0f025-110">4D 不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="0f025-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="0f025-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="0f025-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="0f025-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="0f025-112">0x00000002L</span></span> | <span data-ttu-id="0f025-113">正規化、4D 不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="0f025-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="0f025-114">四個位元組的每一個都是除以255.0 來正規化。</span><span class="sxs-lookup"><span data-stu-id="0f025-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="0f025-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="0f025-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="0f025-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="0f025-116">0x00000004L</span></span> | <span data-ttu-id="0f025-117">正規化、2D 帶正負號的簡短，展開為 (第一個位元組/32767.0，第二個位元組/32767.0，0，1) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="0f025-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="0f025-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="0f025-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="0f025-119">0x00000008L</span></span> | <span data-ttu-id="0f025-120">正規化、4D 帶正負號的簡短，展開為 (第一個位元組/32767.0，第二個位元組/32767.0，第三個位元組/32767.0，第四個位元組/32767.0) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="0f025-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="0f025-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="0f025-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="0f025-122">0x00000010L</span></span> | <span data-ttu-id="0f025-123">正規化、2D 不帶正負號的短，展開為 (第一個位元組/65535.0，第二個位元組/65535.0，0，1) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="0f025-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="0f025-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="0f025-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="0f025-125">0x00000020L</span></span> | <span data-ttu-id="0f025-126">正規化的4D 不帶正負號短，展開為 (第一個位元組/65535.0，第二個位元組/65535.0，第三個位元組/65535.0，第四個位元組/65535.0) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="0f025-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="0f025-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="0f025-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="0f025-128">0x00000040L</span></span> | <span data-ttu-id="0f025-129">3D 未簽署的 10 10 10 格式會展開為 (值、值、值、1) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="0f025-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="0f025-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="0f025-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="0f025-131">0x00000080L</span></span> | <span data-ttu-id="0f025-132">以3D 簽署的 10 10 10 格式正規化和展開為 (v \[ 0 \] /511.0、v \[ 1 \] /511.0、v \[ 2 \] /511.0、1) 。</span><span class="sxs-lookup"><span data-stu-id="0f025-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="0f025-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="0f025-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="0f025-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="0f025-134">0x00000100L</span></span> | <span data-ttu-id="0f025-135">2D 16 位浮點數。</span><span class="sxs-lookup"><span data-stu-id="0f025-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="0f025-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="0f025-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="0f025-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="0f025-137">0x00000200L</span></span> | <span data-ttu-id="0f025-138">4D 16 位浮點數。</span><span class="sxs-lookup"><span data-stu-id="0f025-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="0f025-139">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 DeclTypes 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="0f025-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="0f025-140">常數資訊</span><span class="sxs-lookup"><span data-stu-id="0f025-140">Constant Information</span></span>



|  <span data-ttu-id="0f025-141">需求</span><span class="sxs-lookup"><span data-stu-id="0f025-141">Requirement</span></span>                        | <span data-ttu-id="0f025-142">值</span><span class="sxs-lookup"><span data-stu-id="0f025-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="0f025-143">標頭</span><span class="sxs-lookup"><span data-stu-id="0f025-143">Header</span></span>                   | <span data-ttu-id="0f025-144">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="0f025-144">d3d9caps.h</span></span> |
| <span data-ttu-id="0f025-145">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="0f025-145">Minimum operating system</span></span> | <span data-ttu-id="0f025-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0f025-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0f025-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f025-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f025-148">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="0f025-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



