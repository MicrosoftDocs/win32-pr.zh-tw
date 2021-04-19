---
description: 抓取在建立時為此網格啟用的網格選項。
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh：： GetOptions 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999033"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="6d681-103">ID3DXBaseMesh：： GetOptions 方法</span><span class="sxs-lookup"><span data-stu-id="6d681-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="6d681-104">抓取在建立時為此網格啟用的網格選項。</span><span class="sxs-lookup"><span data-stu-id="6d681-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d681-105">語法</span><span class="sxs-lookup"><span data-stu-id="6d681-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="6d681-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d681-106">Parameters</span></span>

<span data-ttu-id="6d681-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6d681-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d681-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d681-108">Return value</span></span>

<span data-ttu-id="6d681-109">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d681-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d681-110">傳回下列一或多個旗標的組合，表示在建立時為此網格啟用的選項。</span><span class="sxs-lookup"><span data-stu-id="6d681-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="6d681-111">值</span><span class="sxs-lookup"><span data-stu-id="6d681-111">Value</span></span>                   | <span data-ttu-id="6d681-112">描述</span><span class="sxs-lookup"><span data-stu-id="6d681-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d681-113">D3DXMESH \_ 32 位</span><span class="sxs-lookup"><span data-stu-id="6d681-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="6d681-114">使用32位的索引。</span><span class="sxs-lookup"><span data-stu-id="6d681-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6d681-115">D3DXMESH \_ DONOTCLIP</span><span class="sxs-lookup"><span data-stu-id="6d681-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="6d681-116">\_針對頂點和索引緩衝區使用 D3DUSAGE DONOTCLIP usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="6d681-117">D3DXMESH \_ 動態</span><span class="sxs-lookup"><span data-stu-id="6d681-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="6d681-118">相當於同時指定 D3DXMESH \_ VB \_ DYNAMIC 和 D3DXMESH \_ IB \_ dynamic。</span><span class="sxs-lookup"><span data-stu-id="6d681-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="6d681-119">D3DXMESH \_ RTPATCHES</span><span class="sxs-lookup"><span data-stu-id="6d681-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="6d681-120">\_針對頂點和索引緩衝區使用 D3DUSAGE RTPATCHES usage 旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="6d681-121">D3DXMESH \_ NPATCHES</span><span class="sxs-lookup"><span data-stu-id="6d681-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="6d681-122">指定此旗標會讓網格的頂點和索引緩衝區以 D3DUSAGE \_ NPATCHES 旗標建立。</span><span class="sxs-lookup"><span data-stu-id="6d681-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="6d681-123">如果要使用 N 修補程式增強功能來呈現網格物件，則這是必要的。</span><span class="sxs-lookup"><span data-stu-id="6d681-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="6d681-124">D3DXMESH \_ 受控</span><span class="sxs-lookup"><span data-stu-id="6d681-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="6d681-125">相當於指定 D3DXMESH \_ VB managed \_ 和 D3DXMESH \_ IB \_ managed。</span><span class="sxs-lookup"><span data-stu-id="6d681-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="6d681-126">D3DXMESH \_ 點</span><span class="sxs-lookup"><span data-stu-id="6d681-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="6d681-127">\_針對頂點和索引緩衝區使用 D3DUSAGE 點使用方式旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="6d681-128">D3DXMESH \_ IB \_ 動態</span><span class="sxs-lookup"><span data-stu-id="6d681-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="6d681-129">使用 \_ 索引緩衝區的 D3DUSAGE 動態使用旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="6d681-130">D3DXMESH \_ IB \_ 管理</span><span class="sxs-lookup"><span data-stu-id="6d681-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="6d681-131">將 D3DPOOL \_ 受控記憶體類別用於索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6d681-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="6d681-132">D3DXMESH \_ IB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="6d681-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="6d681-133">將 D3DPOOL \_ SYSTEMMEM memory 類別用於索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6d681-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="6d681-134">D3DXMESH \_ IB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="6d681-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="6d681-135">使用 \_ 索引緩衝區的 D3DUSAGE WRITEONLY 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="6d681-136">D3DXMESH \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="6d681-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="6d681-137">相當於同時指定 D3DXMESH \_ VB \_ SYSTEMMEM 和 D3DXMESH \_ IB \_ SYSTEMMEM。</span><span class="sxs-lookup"><span data-stu-id="6d681-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="6d681-138">D3DXMESH \_ VB \_ 動態</span><span class="sxs-lookup"><span data-stu-id="6d681-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="6d681-139">\_針對頂點緩衝區使用 D3DUSAGE 動態使用旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="6d681-140">D3DXMESH \_ VB \_ MANAGED</span><span class="sxs-lookup"><span data-stu-id="6d681-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="6d681-141">\_針對頂點緩衝區使用 D3DPOOL 受控記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="6d681-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="6d681-142">D3DXMESH \_ VB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="6d681-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="6d681-143">\_針對頂點緩衝區使用 D3DPOOL SYSTEMMEM memory 類別。</span><span class="sxs-lookup"><span data-stu-id="6d681-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="6d681-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="6d681-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="6d681-145">\_針對頂點緩衝區使用 D3DUSAGE WRITEONLY 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="6d681-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="6d681-146">D3DXMESH \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="6d681-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="6d681-147">相當於同時指定 D3DXMESH \_ VB \_ WRITEONLY 和 D3DXMESH \_ IB \_ writeonly。</span><span class="sxs-lookup"><span data-stu-id="6d681-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="6d681-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d681-148">Requirements</span></span>



| <span data-ttu-id="6d681-149">需求</span><span class="sxs-lookup"><span data-stu-id="6d681-149">Requirement</span></span> | <span data-ttu-id="6d681-150">值</span><span class="sxs-lookup"><span data-stu-id="6d681-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d681-151">標頭</span><span class="sxs-lookup"><span data-stu-id="6d681-151">Header</span></span><br/>  | <dl> <span data-ttu-id="6d681-152"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d681-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6d681-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d681-153">Library</span></span><br/> | <dl> <span data-ttu-id="6d681-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d681-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6d681-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d681-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d681-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="6d681-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
