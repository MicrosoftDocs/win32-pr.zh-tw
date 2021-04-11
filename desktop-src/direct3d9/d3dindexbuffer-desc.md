---
description: 描述索引緩衝區。
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: 'D3DINDEXBUFFER_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946128"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="ae983-103">D3DINDEXBUFFER \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="ae983-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="ae983-104">描述索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae983-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae983-105">語法</span><span class="sxs-lookup"><span data-stu-id="ae983-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="ae983-106">成員</span><span class="sxs-lookup"><span data-stu-id="ae983-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae983-107">**格式**</span><span class="sxs-lookup"><span data-stu-id="ae983-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ae983-108">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ae983-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ae983-109">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述索引緩衝區資料的介面格式。</span><span class="sxs-lookup"><span data-stu-id="ae983-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="ae983-110">**型別**</span><span class="sxs-lookup"><span data-stu-id="ae983-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ae983-111">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="ae983-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ae983-112">[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae983-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ae983-113">**使用量**</span><span class="sxs-lookup"><span data-stu-id="ae983-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="ae983-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae983-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ae983-115">下列其中一個或多個旗標的組合，指定此資源的使用方式。</span><span class="sxs-lookup"><span data-stu-id="ae983-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="ae983-116">值</span><span class="sxs-lookup"><span data-stu-id="ae983-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="ae983-117">意義</span><span class="sxs-lookup"><span data-stu-id="ae983-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="ae983-118"><dt>**D3DUSAGE \_ DONOTCLIP**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="ae983-119">設定以指出索引緩衝區內容永遠不需要剪切。</span><span class="sxs-lookup"><span data-stu-id="ae983-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="ae983-120"><dt>**D3DUSAGE \_ 動態**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="ae983-121">設定以表示索引緩衝區需要動態記憶體使用。</span><span class="sxs-lookup"><span data-stu-id="ae983-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="ae983-122">這對驅動程式很有用，因為它可讓它們決定緩衝區的放置位置。</span><span class="sxs-lookup"><span data-stu-id="ae983-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="ae983-123">一般而言，靜態索引緩衝區會放置在視訊記憶體中，而且動態索引緩衝區會放置在 AGP 記憶體中。</span><span class="sxs-lookup"><span data-stu-id="ae983-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="ae983-124">請注意，沒有個別的靜態使用方式;如果您未指定 D3DUSAGE \_ 動態，索引緩衝區就會設為靜態。</span><span class="sxs-lookup"><span data-stu-id="ae983-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="ae983-125">D3DUSAGE \_ DYNAMIC 是透過 D3DLOCK \_ 捨棄和 D3DLOCK \_ NOOVERWRITE 鎖定旗標嚴格強制執行。</span><span class="sxs-lookup"><span data-stu-id="ae983-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="ae983-126">因此，D3DLOCK \_ 捨棄和 D3DLOCK \_ NOOVERWRITE 只適用于使用 D3DUSAGE 動態建立的索引緩衝區 \_ ; 它們在靜態頂點緩衝區上是不正確旗標。</span><span class="sxs-lookup"><span data-stu-id="ae983-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="ae983-127">如需使用動態索引緩衝區的詳細資訊，請參閱 [使用動態頂點和索引緩衝區](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="ae983-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="ae983-128">請注意， \_ 無法在 managed 索引緩衝區上指定 D3DUSAGE DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="ae983-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="ae983-129">如需詳細資訊，請參閱 [管理資源 (Direct3D 9) ](managing-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="ae983-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="ae983-130"><dt>**D3DUSAGE \_ RTPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="ae983-131">設定以指出何時要使用索引緩衝區來繪製高序位基本專案。</span><span class="sxs-lookup"><span data-stu-id="ae983-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="ae983-132"><dt>**D3DUSAGE \_ NPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="ae983-133">設定以指出何時使用索引緩衝區來繪製 N 個修補程式。</span><span class="sxs-lookup"><span data-stu-id="ae983-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="ae983-134"><dt>**D3DUSAGE \_ 點**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="ae983-135">設定以指出何時要將索引緩衝區用於繪製點 sprite 或索引點清單。</span><span class="sxs-lookup"><span data-stu-id="ae983-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="ae983-136"><dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="ae983-137">設定以表示緩衝區要與軟體處理搭配使用。</span><span class="sxs-lookup"><span data-stu-id="ae983-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="ae983-138"><dt>**D3DUSAGE \_ WRITEONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="ae983-139">通知系統應用程式只寫入索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae983-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="ae983-140">使用這個旗標可讓驅動程式選擇最佳的記憶體位置，以進行有效率的寫入作業和轉譯。</span><span class="sxs-lookup"><span data-stu-id="ae983-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="ae983-141">嘗試從使用這項功能建立的索引緩衝區讀取，可能會導致效能降低。</span><span class="sxs-lookup"><span data-stu-id="ae983-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="ae983-142">**集區**</span><span class="sxs-lookup"><span data-stu-id="ae983-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="ae983-143">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ae983-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ae983-144">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給此索引緩衝區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="ae983-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ae983-145">**大小**</span><span class="sxs-lookup"><span data-stu-id="ae983-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ae983-146">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae983-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ae983-147">索引緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ae983-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae983-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae983-148">Requirements</span></span>



| <span data-ttu-id="ae983-149">需求</span><span class="sxs-lookup"><span data-stu-id="ae983-149">Requirement</span></span> | <span data-ttu-id="ae983-150">值</span><span class="sxs-lookup"><span data-stu-id="ae983-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae983-151">標頭</span><span class="sxs-lookup"><span data-stu-id="ae983-151">Header</span></span><br/> | <dl> <span data-ttu-id="ae983-152"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae983-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae983-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae983-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae983-154">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="ae983-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ae983-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="ae983-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="ae983-156"> (Direct3D 9) 的索引緩衝區 </span><span class="sxs-lookup"><span data-stu-id="ae983-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
