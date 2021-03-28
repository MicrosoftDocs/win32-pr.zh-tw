---
title: D3DX_R16G16_UINT_to_UINT2 函式
description: 解壓縮 DXGI \_ FORMAT \_ R16G16 \_ UINT 著色器資料到 XMUINT2。
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322595"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a><span data-ttu-id="814a7-104">D3DX \_ R16G16 \_ UINT \_ to \_ UINT2 function</span><span class="sxs-lookup"><span data-stu-id="814a7-104">D3DX\_R16G16\_UINT\_to\_UINT2 function</span></span>

<span data-ttu-id="814a7-105">解壓縮 DXGI \_ FORMAT \_ R16G16 \_ UINT 著色器資料到 XMUINT2。</span><span class="sxs-lookup"><span data-stu-id="814a7-105">Unpacks DXGI\_FORMAT\_R16G16\_UINT shader data to an XMUINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="814a7-106">語法</span><span class="sxs-lookup"><span data-stu-id="814a7-106">Syntax</span></span>

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="814a7-107">參數</span><span class="sxs-lookup"><span data-stu-id="814a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814a7-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="814a7-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="814a7-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="814a7-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814a7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="814a7-110">Return value</span></span>

<span data-ttu-id="814a7-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="814a7-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="814a7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="814a7-112">Requirements</span></span>



| <span data-ttu-id="814a7-113">需求</span><span class="sxs-lookup"><span data-stu-id="814a7-113">Requirement</span></span> | <span data-ttu-id="814a7-114">值</span><span class="sxs-lookup"><span data-stu-id="814a7-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814a7-115">標頭</span><span class="sxs-lookup"><span data-stu-id="814a7-115">Header</span></span><br/> | <dl> <span data-ttu-id="814a7-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="814a7-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814a7-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="814a7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814a7-118">函式</span><span class="sxs-lookup"><span data-stu-id="814a7-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="814a7-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="814a7-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





