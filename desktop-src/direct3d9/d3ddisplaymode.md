---
description: 描述顯示模式。
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: 'D3DDISPLAYMODE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116193"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="dc4a4-103">D3DDISPLAYMODE 結構</span><span class="sxs-lookup"><span data-stu-id="dc4a4-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="dc4a4-104">描述顯示模式。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc4a4-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="dc4a4-106">成員</span><span class="sxs-lookup"><span data-stu-id="dc4a4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc4a4-107">**寬度**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="dc4a4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc4a4-109">螢幕寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dc4a4-110">**高度**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="dc4a4-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc4a4-112">螢幕高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dc4a4-113">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="dc4a4-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc4a4-115">重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-115">Refresh rate.</span></span> <span data-ttu-id="dc4a4-116">值為0表示介面卡預設值。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="dc4a4-117">**格式**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="dc4a4-118">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc4a4-119">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述顯示模式的介面格式。</span><span class="sxs-lookup"><span data-stu-id="dc4a4-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc4a4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc4a4-120">Requirements</span></span>



| <span data-ttu-id="dc4a4-121">需求</span><span class="sxs-lookup"><span data-stu-id="dc4a4-121">Requirement</span></span> | <span data-ttu-id="dc4a4-122">值</span><span class="sxs-lookup"><span data-stu-id="dc4a4-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4a4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="dc4a4-123">Header</span></span><br/> | <dl> <span data-ttu-id="dc4a4-124"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4a4-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4a4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc4a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4a4-126">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="dc4a4-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="dc4a4-127">**EnumAdapterModes**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="dc4a4-128">**GetAdapterDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="dc4a4-129">**GetDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="dc4a4-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
