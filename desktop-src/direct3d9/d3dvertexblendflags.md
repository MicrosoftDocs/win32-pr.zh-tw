---
description: 定義旗標，用來控制執行 multimatrix 頂點混合時，系統所套用的數位或矩陣。
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: 'D3DVERTEXBLENDFLAGS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322871"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="9a355-103">D3DVERTEXBLENDFLAGS 列舉</span><span class="sxs-lookup"><span data-stu-id="9a355-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="9a355-104">定義旗標，用來控制執行 multimatrix 頂點混合時，系統所套用的數位或矩陣。</span><span class="sxs-lookup"><span data-stu-id="9a355-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a355-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a355-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="9a355-106">常數</span><span class="sxs-lookup"><span data-stu-id="9a355-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9a355-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="9a355-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-108">停用頂點混合;只套用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定的世界矩陣，其中轉換狀態的索引值為0。</span><span class="sxs-lookup"><span data-stu-id="9a355-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="9a355-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="9a355-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-110">啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之兩個矩陣之間的頂點混合，其中轉換狀態的索引值為0和1。</span><span class="sxs-lookup"><span data-stu-id="9a355-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="9a355-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="9a355-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-112">啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之三個矩陣之間的頂點混合，其中轉換狀態的索引值為0、1和2。</span><span class="sxs-lookup"><span data-stu-id="9a355-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="9a355-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="9a355-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-114">啟用 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 宏所設定之四個矩陣之間的頂點混合，其中轉換狀態的索引值為0、1、2和3。</span><span class="sxs-lookup"><span data-stu-id="9a355-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="9a355-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF \_ 補間**</span><span class="sxs-lookup"><span data-stu-id="9a355-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-116">您可以使用指派給 D3DRS TWEENFACTOR 的值來完成頂點混色 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9a355-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="9a355-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="9a355-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="9a355-118">使用權數為1.0 的單一矩陣。</span><span class="sxs-lookup"><span data-stu-id="9a355-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a355-119">備註</span><span class="sxs-lookup"><span data-stu-id="9a355-119">Remarks</span></span>

<span data-ttu-id="9a355-120">此類型的成員會搭配 D3DRS VERTEXBLEND 轉譯 \_ 狀態使用。</span><span class="sxs-lookup"><span data-stu-id="9a355-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="9a355-121">幾何混合 (multimatrix 頂點混色) 需要您的應用程式使用已針對每個頂點混合 (Beta) 權數的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="9a355-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a355-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a355-122">Requirements</span></span>



| <span data-ttu-id="9a355-123">需求</span><span class="sxs-lookup"><span data-stu-id="9a355-123">Requirement</span></span> | <span data-ttu-id="9a355-124">值</span><span class="sxs-lookup"><span data-stu-id="9a355-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a355-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9a355-125">Header</span></span><br/> | <dl> <span data-ttu-id="9a355-126"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a355-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a355-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a355-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a355-128">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="9a355-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9a355-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="9a355-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="9a355-130">**D3DTS \_ 世界**</span><span class="sxs-lookup"><span data-stu-id="9a355-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="9a355-131">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="9a355-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="9a355-132">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="9a355-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
