---
title: D3DX_UINT4_to_R10G10B10A2_UINT 函式
description: 將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UINT。
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- D3DX_UINT4_to_R10G10B10A2_UINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc7076b9e44ab1491bb8abbf8d4edb82158282c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992194"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a><span data-ttu-id="5316b-104">D3DX \_ UINT4 \_ to \_ R10G10B10A2 \_ UINT 函數</span><span class="sxs-lookup"><span data-stu-id="5316b-104">D3DX\_UINT4\_to\_R10G10B10A2\_UINT function</span></span>

<span data-ttu-id="5316b-105">將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UINT。</span><span class="sxs-lookup"><span data-stu-id="5316b-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5316b-106">語法</span><span class="sxs-lookup"><span data-stu-id="5316b-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5316b-107">參數</span><span class="sxs-lookup"><span data-stu-id="5316b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5316b-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="5316b-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5316b-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="5316b-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5316b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5316b-110">Return value</span></span>

<span data-ttu-id="5316b-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="5316b-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5316b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5316b-112">Requirements</span></span>



| <span data-ttu-id="5316b-113">需求</span><span class="sxs-lookup"><span data-stu-id="5316b-113">Requirement</span></span> | <span data-ttu-id="5316b-114">值</span><span class="sxs-lookup"><span data-stu-id="5316b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5316b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5316b-115">Header</span></span><br/> | <dl> <span data-ttu-id="5316b-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="5316b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5316b-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="5316b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5316b-118">函式</span><span class="sxs-lookup"><span data-stu-id="5316b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5316b-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="5316b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





