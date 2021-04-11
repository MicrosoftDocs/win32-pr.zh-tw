---
description: 定義用來描述背景緩衝區類型的常數。
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: 'D3DBACKBUFFER_TYPE 列舉 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946065"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="52786-103">D3DBACKBUFFER \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="52786-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="52786-104">定義用來描述背景緩衝區類型的常數。</span><span class="sxs-lookup"><span data-stu-id="52786-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="52786-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52786-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="52786-106">常數</span><span class="sxs-lookup"><span data-stu-id="52786-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52786-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER \_ 類型 \_ MONO**</span><span class="sxs-lookup"><span data-stu-id="52786-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="52786-108">指定 nonstereo 交換鏈。</span><span class="sxs-lookup"><span data-stu-id="52786-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="52786-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**左邊的 D3DBACKBUFFER \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="52786-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="52786-110">指定交換鏈中身歷聲配對的左邊。</span><span class="sxs-lookup"><span data-stu-id="52786-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="52786-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ 類型 \_ RIGHT**</span><span class="sxs-lookup"><span data-stu-id="52786-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="52786-112">指定交換鏈中身歷聲配對的右側。</span><span class="sxs-lookup"><span data-stu-id="52786-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="52786-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ 類型 \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52786-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52786-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="52786-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="52786-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="52786-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="52786-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="52786-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52786-117">備註</span><span class="sxs-lookup"><span data-stu-id="52786-117">Remarks</span></span>

<span data-ttu-id="52786-118">Direct3D 9 不支援身歷聲視圖，因此 Direct3D 不會使用 \_ \_ 此列舉型別左邊的 D3DBACKBUFFER 類型和 D3DBACKBUFFER \_ 類型的 \_ 正確值。</span><span class="sxs-lookup"><span data-stu-id="52786-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="52786-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="52786-119">Requirements</span></span>



| <span data-ttu-id="52786-120">需求</span><span class="sxs-lookup"><span data-stu-id="52786-120">Requirement</span></span> | <span data-ttu-id="52786-121">值</span><span class="sxs-lookup"><span data-stu-id="52786-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52786-122">標頭</span><span class="sxs-lookup"><span data-stu-id="52786-122">Header</span></span><br/> | <dl> <span data-ttu-id="52786-123"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="52786-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52786-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52786-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52786-125">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="52786-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="52786-126">**IDirect3DDevice9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="52786-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="52786-127">**IDirect3DSwapChain9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="52786-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
