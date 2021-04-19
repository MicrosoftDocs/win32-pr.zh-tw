---
description: 指定如何旋轉用來顯示全螢幕應用程式的監視器。
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: 'D3DDISPLAYROTATION 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981998"
---
# <a name="d3ddisplayrotation-enumeration"></a><span data-ttu-id="67b17-103">D3DDISPLAYROTATION 列舉</span><span class="sxs-lookup"><span data-stu-id="67b17-103">D3DDISPLAYROTATION enumeration</span></span>

<span data-ttu-id="67b17-104">指定如何旋轉用來顯示全螢幕應用程式的監視器。</span><span class="sxs-lookup"><span data-stu-id="67b17-104">Specifies how the monitor being used to display a full-screen application is rotated.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67b17-105">Syntax</span></span>


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a><span data-ttu-id="67b17-106">常數</span><span class="sxs-lookup"><span data-stu-id="67b17-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="67b17-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION 身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="67b17-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION\_IDENTITY**</span></span>
</dt> <dd>

<span data-ttu-id="67b17-108">顯示未旋轉。</span><span class="sxs-lookup"><span data-stu-id="67b17-108">Display is not rotated.</span></span>

</dd> <dt>

<span data-ttu-id="67b17-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**</span><span class="sxs-lookup"><span data-stu-id="67b17-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION\_90**</span></span>
</dt> <dd>

<span data-ttu-id="67b17-110">顯示旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="67b17-110">Display is rotated 90 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="67b17-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**</span><span class="sxs-lookup"><span data-stu-id="67b17-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION\_180**</span></span>
</dt> <dd>

<span data-ttu-id="67b17-112">顯示旋轉180度。</span><span class="sxs-lookup"><span data-stu-id="67b17-112">Display is rotated 180 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="67b17-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**</span><span class="sxs-lookup"><span data-stu-id="67b17-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION\_270**</span></span>
</dt> <dd>

<span data-ttu-id="67b17-114">顯示旋轉270度。</span><span class="sxs-lookup"><span data-stu-id="67b17-114">Display is rotated 270 degrees.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67b17-115">備註</span><span class="sxs-lookup"><span data-stu-id="67b17-115">Remarks</span></span>

<span data-ttu-id="67b17-116">此列舉用於 [**IDirect3D9Ex：： GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex)、 [**IDirect3DDevice9Ex：： GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)和 [**IDirect3DSwapChain9Ex：： GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex)。</span><span class="sxs-lookup"><span data-stu-id="67b17-116">This enumeration is used in [**IDirect3D9Ex::GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex), and [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).</span></span>

<span data-ttu-id="67b17-117">應用程式可以選擇使用 [D3DPRESENTFLAG \_ NOAUTOROTATE](d3dpresentflag.md)來處理監視器輪替本身，在這種情況下，應用程式將需要知道監視器的旋轉方式，讓它能夠據以調整其轉譯。</span><span class="sxs-lookup"><span data-stu-id="67b17-117">Applications may choose to handle monitor rotation themselves by using the [D3DPRESENTFLAG\_NOAUTOROTATE](d3dpresentflag.md), in which case, the application will need to know how the monitor is rotated so that it may adjust its rendering accordingly.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b17-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="67b17-118">Requirements</span></span>



| <span data-ttu-id="67b17-119">需求</span><span class="sxs-lookup"><span data-stu-id="67b17-119">Requirement</span></span> | <span data-ttu-id="67b17-120">值</span><span class="sxs-lookup"><span data-stu-id="67b17-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67b17-121">標頭</span><span class="sxs-lookup"><span data-stu-id="67b17-121">Header</span></span><br/> | <dl> <span data-ttu-id="67b17-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="67b17-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b17-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67b17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b17-124">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="67b17-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




