---
title: D3DX_UINT2_to_R16G16_UINT 函式
description: 將指定的 XMUINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ UINT。
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- D3DX_UINT2_to_R16G16_UINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992195"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a><span data-ttu-id="3dad7-104">D3DX \_ UINT2 \_ to \_ R16G16 \_ UINT 函數</span><span class="sxs-lookup"><span data-stu-id="3dad7-104">D3DX\_UINT2\_to\_R16G16\_UINT function</span></span>

<span data-ttu-id="3dad7-105">將指定的 XMUINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ UINT。</span><span class="sxs-lookup"><span data-stu-id="3dad7-105">Packs the given XMUINT2 back into a DXGI\_FORMAT\_R16G16\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dad7-106">語法</span><span class="sxs-lookup"><span data-stu-id="3dad7-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3dad7-107">參數</span><span class="sxs-lookup"><span data-stu-id="3dad7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dad7-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="3dad7-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3dad7-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="3dad7-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dad7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dad7-110">Return value</span></span>

<span data-ttu-id="3dad7-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="3dad7-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dad7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dad7-112">Requirements</span></span>



| <span data-ttu-id="3dad7-113">需求</span><span class="sxs-lookup"><span data-stu-id="3dad7-113">Requirement</span></span> | <span data-ttu-id="3dad7-114">值</span><span class="sxs-lookup"><span data-stu-id="3dad7-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dad7-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3dad7-115">Header</span></span><br/> | <dl> <span data-ttu-id="3dad7-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="3dad7-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dad7-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="3dad7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dad7-118">函式</span><span class="sxs-lookup"><span data-stu-id="3dad7-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3dad7-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="3dad7-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





