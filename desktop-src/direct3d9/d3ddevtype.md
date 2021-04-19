---
description: 定義裝置類型。
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: 'D3DDEVTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974849"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="955d1-103">D3DDEVTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="955d1-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="955d1-104">定義裝置類型。</span><span class="sxs-lookup"><span data-stu-id="955d1-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="955d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="955d1-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="955d1-106">常數</span><span class="sxs-lookup"><span data-stu-id="955d1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="955d1-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**</span><span class="sxs-lookup"><span data-stu-id="955d1-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="955d1-108">硬體柵格化。</span><span class="sxs-lookup"><span data-stu-id="955d1-108">Hardware rasterization.</span></span> <span data-ttu-id="955d1-109">使用軟體、硬體或混合轉換和光源來完成陰影。</span><span class="sxs-lookup"><span data-stu-id="955d1-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="955d1-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NullREF**</span><span class="sxs-lookup"><span data-stu-id="955d1-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="955d1-111">在未提供硬體和參考光柵的電腦上初始化 Direct3D，並啟用建立3D 內容的資源。</span><span class="sxs-lookup"><span data-stu-id="955d1-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="955d1-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="955d1-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="955d1-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**</span><span class="sxs-lookup"><span data-stu-id="955d1-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="955d1-114">Direct3D 功能是在軟體中執行;不過，參考轉譯器會在每次可以時使用特殊的 CPU 指示。</span><span class="sxs-lookup"><span data-stu-id="955d1-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="955d1-115">參考裝置是由 Windows SDK 8.0 或更新版本所安裝，旨在做為僅供開發之用的協助工具。</span><span class="sxs-lookup"><span data-stu-id="955d1-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="955d1-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="955d1-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="955d1-117">已向 [**IDirect3D9：： RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice)註冊的可插入軟體裝置。</span><span class="sxs-lookup"><span data-stu-id="955d1-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="955d1-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="955d1-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="955d1-119">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="955d1-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="955d1-120">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="955d1-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="955d1-121">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="955d1-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="955d1-122">備註</span><span class="sxs-lookup"><span data-stu-id="955d1-122">Remarks</span></span>

<span data-ttu-id="955d1-123">如果指定了 D3DDEVTYPE NullREF，則採用 **D3DDEVTYPE** 裝置類型之 [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9)介面的所有方法都將會失敗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="955d1-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="955d1-124">若要使用這些方法，請 \_ 在方法呼叫中替代 D3DDEVTYPE REF。</span><span class="sxs-lookup"><span data-stu-id="955d1-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="955d1-125">\_ \_ 除非需要頂點和索引緩衝區，否則應在 D3DPOOL 臨時記憶體中建立 D3DDEVTYPE REF 裝置。</span><span class="sxs-lookup"><span data-stu-id="955d1-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="955d1-126">若要支援頂點和索引緩衝區，請在 D3DPOOL SYSTEMMEM 記憶體中建立裝置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="955d1-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="955d1-127">如果已安裝 D3dref9.dll，即使指定了 D3DDEVTYPE NullREF，Direct3D 仍會使用參考轉譯器來建立 D3DDEVTYPE \_ REF 裝置類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="955d1-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="955d1-128">如果 D3dref9.dll 無法使用且 \_ 已指定 D3DDEVTYPE NullREF，Direct3D 將不會轉譯或呈現場景。</span><span class="sxs-lookup"><span data-stu-id="955d1-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="955d1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="955d1-129">Requirements</span></span>



| <span data-ttu-id="955d1-130">需求</span><span class="sxs-lookup"><span data-stu-id="955d1-130">Requirement</span></span> | <span data-ttu-id="955d1-131">值</span><span class="sxs-lookup"><span data-stu-id="955d1-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="955d1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="955d1-132">Header</span></span><br/> | <dl> <span data-ttu-id="955d1-133"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="955d1-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955d1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="955d1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955d1-135">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="955d1-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="955d1-136">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="955d1-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="955d1-137">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="955d1-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="955d1-138">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="955d1-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="955d1-139">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="955d1-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="955d1-140">**IDirect3D9：： GetDeviceCaps**</span><span class="sxs-lookup"><span data-stu-id="955d1-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="955d1-141">**D3DDEVICE \_ 建立 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="955d1-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
