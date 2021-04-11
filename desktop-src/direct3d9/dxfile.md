---
description: 下列旗標用來指定要在材質中操作的通道。 已取代。
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: DXFILE 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025723"
---
# <a name="dxfile-constants"></a><span data-ttu-id="91639-104">DXFILE 常數</span><span class="sxs-lookup"><span data-stu-id="91639-104">DXFILE Constants</span></span>

<span data-ttu-id="91639-105">下列旗標用來指定要在材質中操作的通道。</span><span class="sxs-lookup"><span data-stu-id="91639-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="91639-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="91639-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="91639-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="91639-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="91639-108">\#定義</span><span class="sxs-lookup"><span data-stu-id="91639-108">\#define</span></span>                 | <span data-ttu-id="91639-109">值</span><span class="sxs-lookup"><span data-stu-id="91639-109">Value</span></span> | <span data-ttu-id="91639-110">描述</span><span class="sxs-lookup"><span data-stu-id="91639-110">Description</span></span>      |
| <span data-ttu-id="91639-111">DXFILEFORMAT \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="91639-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="91639-112">0</span><span class="sxs-lookup"><span data-stu-id="91639-112">0</span></span>     | <span data-ttu-id="91639-113">二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-113">Binary file.</span></span>     |
| <span data-ttu-id="91639-114">DXFILEFORMAT \_ 文字</span><span class="sxs-lookup"><span data-stu-id="91639-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="91639-115">1</span><span class="sxs-lookup"><span data-stu-id="91639-115">1</span></span>     | <span data-ttu-id="91639-116">文字檔。</span><span class="sxs-lookup"><span data-stu-id="91639-116">Text file.</span></span>       |
| <span data-ttu-id="91639-117">DXFILEFORMAT \_ 壓縮</span><span class="sxs-lookup"><span data-stu-id="91639-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="91639-118">2</span><span class="sxs-lookup"><span data-stu-id="91639-118">2</span></span>     | <span data-ttu-id="91639-119">壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-119">Compressed file.</span></span> |



 

<span data-ttu-id="91639-120">這些 \# 定義是在 Dxfile 中宣告。</span><span class="sxs-lookup"><span data-stu-id="91639-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="91639-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="91639-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="91639-122">\#定義</span><span class="sxs-lookup"><span data-stu-id="91639-122">\#define</span></span>                 | <span data-ttu-id="91639-123">值</span><span class="sxs-lookup"><span data-stu-id="91639-123">Value</span></span> | <span data-ttu-id="91639-124">描述</span><span class="sxs-lookup"><span data-stu-id="91639-124">Description</span></span>                  |
| <span data-ttu-id="91639-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="91639-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="91639-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="91639-126">0x00L</span></span> | <span data-ttu-id="91639-127">從檔案載入檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="91639-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="91639-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="91639-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="91639-129">0x01L</span></span> | <span data-ttu-id="91639-130">從資源載入檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="91639-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="91639-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="91639-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="91639-132">0x02L</span></span> | <span data-ttu-id="91639-133">從記憶體載入檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="91639-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="91639-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="91639-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="91639-135">0x04L</span></span> | <span data-ttu-id="91639-136">從資料流程載入檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="91639-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="91639-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="91639-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="91639-138">0x08L</span></span> | <span data-ttu-id="91639-139">從 URL 載入檔案。</span><span class="sxs-lookup"><span data-stu-id="91639-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="91639-140">這些 \# 定義是在 Dxfile 中宣告。</span><span class="sxs-lookup"><span data-stu-id="91639-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91639-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="91639-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91639-142"> (舊版) 的 X 檔案參考 </span><span class="sxs-lookup"><span data-stu-id="91639-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



