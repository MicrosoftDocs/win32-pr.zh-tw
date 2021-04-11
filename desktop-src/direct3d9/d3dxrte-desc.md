---
description: 描述 ID3DXRenderToEnvMap 實例所使用的非畫面呈現目標。
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: 'D3DXRTE_DESC 結構 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196245"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="67d2b-103">D3DXRTE \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="67d2b-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="67d2b-104">描述 [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)實例所使用的非畫面呈現目標。</span><span class="sxs-lookup"><span data-stu-id="67d2b-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="67d2b-105">語法</span><span class="sxs-lookup"><span data-stu-id="67d2b-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="67d2b-106">成員</span><span class="sxs-lookup"><span data-stu-id="67d2b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="67d2b-107">**大小**</span><span class="sxs-lookup"><span data-stu-id="67d2b-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="67d2b-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67d2b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67d2b-109">寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="67d2b-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="67d2b-110">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="67d2b-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="67d2b-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67d2b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67d2b-112">詳細資料層級 (」 LOD) 的最大值。</span><span class="sxs-lookup"><span data-stu-id="67d2b-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="67d2b-113">**格式**</span><span class="sxs-lookup"><span data-stu-id="67d2b-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="67d2b-114">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="67d2b-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67d2b-115">色彩緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="67d2b-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="67d2b-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="67d2b-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="67d2b-117">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67d2b-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67d2b-118">指出是否需要 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="67d2b-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="67d2b-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="67d2b-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="67d2b-120">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="67d2b-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67d2b-121">深度緩衝區的格式。</span><span class="sxs-lookup"><span data-stu-id="67d2b-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67d2b-122">備註</span><span class="sxs-lookup"><span data-stu-id="67d2b-122">Remarks</span></span>

<span data-ttu-id="67d2b-123">這個方法是用來傳回建立 [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) 物件時所使用的建立參數。</span><span class="sxs-lookup"><span data-stu-id="67d2b-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d2b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="67d2b-124">Requirements</span></span>



| <span data-ttu-id="67d2b-125">需求</span><span class="sxs-lookup"><span data-stu-id="67d2b-125">Requirement</span></span> | <span data-ttu-id="67d2b-126">值</span><span class="sxs-lookup"><span data-stu-id="67d2b-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67d2b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="67d2b-127">Header</span></span><br/> | <dl> <span data-ttu-id="67d2b-128"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="67d2b-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d2b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67d2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d2b-130">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="67d2b-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
