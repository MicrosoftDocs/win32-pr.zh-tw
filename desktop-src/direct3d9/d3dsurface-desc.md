---
description: 描述表面。
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: 'D3DSURFACE_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000582"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="58c08-103">D3DSURFACE \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="58c08-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="58c08-104">描述表面。</span><span class="sxs-lookup"><span data-stu-id="58c08-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c08-105">語法</span><span class="sxs-lookup"><span data-stu-id="58c08-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="58c08-106">成員</span><span class="sxs-lookup"><span data-stu-id="58c08-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="58c08-107">**格式**</span><span class="sxs-lookup"><span data-stu-id="58c08-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-108">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-109">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述介面格式。</span><span class="sxs-lookup"><span data-stu-id="58c08-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-110">**型別**</span><span class="sxs-lookup"><span data-stu-id="58c08-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-111">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-112">[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為介面。</span><span class="sxs-lookup"><span data-stu-id="58c08-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-113">**使用量**</span><span class="sxs-lookup"><span data-stu-id="58c08-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-115">可能是 D3DUSAGE \_ DEPTHSTENCIL 或 D3DUSAGE \_ RENDERTARGET 值。</span><span class="sxs-lookup"><span data-stu-id="58c08-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="58c08-116">如需詳細資訊，請參閱 [**D3DUSAGE**](d3dusage.md)。</span><span class="sxs-lookup"><span data-stu-id="58c08-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="58c08-117">**集區**</span><span class="sxs-lookup"><span data-stu-id="58c08-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-118">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-119">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個介面的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="58c08-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-120">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="58c08-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-121">類型： **[ **D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-122">[**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md)別列舉型別的成員，指定介面所支援的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="58c08-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-123">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="58c08-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-124">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-125">品質層級。</span><span class="sxs-lookup"><span data-stu-id="58c08-125">Quality level.</span></span> <span data-ttu-id="58c08-126">有效範圍介於零到1之間，且小於 [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)所使用的 pQualityLevels 所傳回的層級。</span><span class="sxs-lookup"><span data-stu-id="58c08-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="58c08-127">傳遞較大的值會傳回錯誤，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="58c08-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="58c08-128">配對轉譯目標、深度樣板表面和多級取樣類型的 MultisampleQuality 值必須全部相符。</span><span class="sxs-lookup"><span data-stu-id="58c08-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-129">**寬度**</span><span class="sxs-lookup"><span data-stu-id="58c08-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-130">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-131">介面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="58c08-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="58c08-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="58c08-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="58c08-133">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c08-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="58c08-134">介面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="58c08-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58c08-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="58c08-135">Requirements</span></span>



| <span data-ttu-id="58c08-136">需求</span><span class="sxs-lookup"><span data-stu-id="58c08-136">Requirement</span></span> | <span data-ttu-id="58c08-137">值</span><span class="sxs-lookup"><span data-stu-id="58c08-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58c08-138">標頭</span><span class="sxs-lookup"><span data-stu-id="58c08-138">Header</span></span><br/> | <dl> <span data-ttu-id="58c08-139"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="58c08-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c08-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58c08-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c08-141">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="58c08-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="58c08-142">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="58c08-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="58c08-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="58c08-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="58c08-144">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="58c08-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
