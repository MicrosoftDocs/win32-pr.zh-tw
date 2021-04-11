---
description: 定義常數，以描述支援的材質定址模式。
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: 'D3DTEXTUREADDRESS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035338"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="e7e51-103">D3DTEXTUREADDRESS 列舉</span><span class="sxs-lookup"><span data-stu-id="e7e51-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="e7e51-104">定義常數，以描述支援的材質定址模式。</span><span class="sxs-lookup"><span data-stu-id="e7e51-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e51-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e51-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="e7e51-106">常數</span><span class="sxs-lookup"><span data-stu-id="e7e51-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e7e51-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ WRAP**</span><span class="sxs-lookup"><span data-stu-id="e7e51-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-108">並排顯示每個整數連接點的材質。</span><span class="sxs-lookup"><span data-stu-id="e7e51-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="e7e51-109">例如，如果您的值介於0和3之間，則紋理會重複三次;不執行鏡像。</span><span class="sxs-lookup"><span data-stu-id="e7e51-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="e7e51-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS \_ 鏡像**</span><span class="sxs-lookup"><span data-stu-id="e7e51-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-111">類似于 D3DTADDRESS \_ WRAP，不同之處在于材質會在每個整數連接點翻轉。</span><span class="sxs-lookup"><span data-stu-id="e7e51-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="e7e51-112">例如，如果您的值介於0和1之間，則會以正常方式定址紋理;在1和2之間，紋理會 (鏡像) 翻轉;在2和3之間，紋理會再次正常;依此類推。</span><span class="sxs-lookup"><span data-stu-id="e7e51-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e7e51-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ 夾具**</span><span class="sxs-lookup"><span data-stu-id="e7e51-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-114">在0.0 範圍之外的材質座標 \[ ，1.0 \] 會分別設定為0.0 或1.0 的材質色彩。</span><span class="sxs-lookup"><span data-stu-id="e7e51-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="e7e51-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS \_ 框線**</span><span class="sxs-lookup"><span data-stu-id="e7e51-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-116">在0.0 範圍之外的材質座標 \[ ，1.0 \] 會設定為框線色彩。</span><span class="sxs-lookup"><span data-stu-id="e7e51-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="e7e51-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**</span><span class="sxs-lookup"><span data-stu-id="e7e51-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-118">類似于 D3DTADDRESS \_ 鏡像和 D3DTADDRESS \_ 夾具。</span><span class="sxs-lookup"><span data-stu-id="e7e51-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="e7e51-119">採用紋理座標的絕對值 (因此，鏡像大約為 0) ，然後個至最大值。</span><span class="sxs-lookup"><span data-stu-id="e7e51-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="e7e51-120">最常見的用法是針對磁片區紋理，其中不需要完整 D3DTADDRESS \_ MIRRORONCE 材質定址模式的支援，但資料在一個座標軸周圍是對稱的。</span><span class="sxs-lookup"><span data-stu-id="e7e51-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="e7e51-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e7e51-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e7e51-122">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="e7e51-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e7e51-123">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="e7e51-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e7e51-124">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e7e51-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7e51-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7e51-125">Requirements</span></span>



| <span data-ttu-id="e7e51-126">需求</span><span class="sxs-lookup"><span data-stu-id="e7e51-126">Requirement</span></span> | <span data-ttu-id="e7e51-127">值</span><span class="sxs-lookup"><span data-stu-id="e7e51-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e51-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e7e51-128">Header</span></span><br/> | <dl> <span data-ttu-id="e7e51-129"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e51-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e51-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7e51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e51-131">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="e7e51-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e7e51-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e7e51-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
