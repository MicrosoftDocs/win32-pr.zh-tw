---
title: D3DX_INT2_to_R16G16_SINT 函式
description: 將指定的 XMINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ 聖。
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974703"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="01dd2-104">D3DX \_ INT2 \_ to \_ R16G16 \_ 聖函數</span><span class="sxs-lookup"><span data-stu-id="01dd2-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="01dd2-105">將指定的 XMINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ 聖。</span><span class="sxs-lookup"><span data-stu-id="01dd2-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="01dd2-106">語法</span><span class="sxs-lookup"><span data-stu-id="01dd2-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="01dd2-107">參數</span><span class="sxs-lookup"><span data-stu-id="01dd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01dd2-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="01dd2-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="01dd2-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="01dd2-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01dd2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="01dd2-110">Return value</span></span>

<span data-ttu-id="01dd2-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="01dd2-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="01dd2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="01dd2-112">Requirements</span></span>



| <span data-ttu-id="01dd2-113">需求</span><span class="sxs-lookup"><span data-stu-id="01dd2-113">Requirement</span></span> | <span data-ttu-id="01dd2-114">值</span><span class="sxs-lookup"><span data-stu-id="01dd2-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01dd2-115">標頭</span><span class="sxs-lookup"><span data-stu-id="01dd2-115">Header</span></span><br/> | <dl> <span data-ttu-id="01dd2-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="01dd2-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01dd2-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="01dd2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01dd2-118">函式</span><span class="sxs-lookup"><span data-stu-id="01dd2-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="01dd2-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="01dd2-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





