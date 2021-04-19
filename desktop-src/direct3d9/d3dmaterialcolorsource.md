---
description: 定義必須針對光源計算存取色彩或色彩元件的位置。
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: 'D3DMATERIALCOLORSOURCE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991477"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="23006-103">D3DMATERIALCOLORSOURCE 列舉</span><span class="sxs-lookup"><span data-stu-id="23006-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="23006-104">定義必須針對光源計算存取色彩或色彩元件的位置。</span><span class="sxs-lookup"><span data-stu-id="23006-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="23006-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23006-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="23006-106">常數</span><span class="sxs-lookup"><span data-stu-id="23006-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23006-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="23006-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="23006-108">使用目前材質的色彩。</span><span class="sxs-lookup"><span data-stu-id="23006-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="23006-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="23006-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="23006-110">使用擴散頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="23006-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="23006-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="23006-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="23006-112">使用反射頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="23006-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="23006-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="23006-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="23006-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="23006-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="23006-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="23006-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="23006-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="23006-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23006-117">備註</span><span class="sxs-lookup"><span data-stu-id="23006-117">Remarks</span></span>

<span data-ttu-id="23006-118">這些旗標是用來設定 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) 列舉類型中下列轉譯狀態的值。</span><span class="sxs-lookup"><span data-stu-id="23006-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="23006-119">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="23006-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="23006-120">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="23006-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="23006-121">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="23006-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="23006-122">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="23006-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="23006-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="23006-123">Requirements</span></span>



| <span data-ttu-id="23006-124">需求</span><span class="sxs-lookup"><span data-stu-id="23006-124">Requirement</span></span> | <span data-ttu-id="23006-125">值</span><span class="sxs-lookup"><span data-stu-id="23006-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23006-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23006-126">Header</span></span><br/> | <dl> <span data-ttu-id="23006-127"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="23006-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23006-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23006-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23006-129">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="23006-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="23006-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="23006-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
