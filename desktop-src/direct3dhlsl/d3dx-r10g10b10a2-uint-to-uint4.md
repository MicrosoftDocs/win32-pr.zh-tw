---
title: D3DX_R10G10B10A2_UINT_to_UINT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT 著色器資料到 XMINT4。
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- D3DX_R10G10B10A2_UINT_to_UINT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378b013ad077c787253b4a58f24082d1c64b416f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974693"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a><span data-ttu-id="99d34-104">D3DX \_ R10G10B10A2 \_ UINT \_ to \_ UINT4 function</span><span class="sxs-lookup"><span data-stu-id="99d34-104">D3DX\_R10G10B10A2\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="99d34-105">解壓縮 DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT 著色器資料到 XMINT4。</span><span class="sxs-lookup"><span data-stu-id="99d34-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d34-106">語法</span><span class="sxs-lookup"><span data-stu-id="99d34-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="99d34-107">參數</span><span class="sxs-lookup"><span data-stu-id="99d34-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99d34-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="99d34-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="99d34-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="99d34-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99d34-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="99d34-110">Return value</span></span>

<span data-ttu-id="99d34-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="99d34-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="99d34-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="99d34-112">Requirements</span></span>



| <span data-ttu-id="99d34-113">需求</span><span class="sxs-lookup"><span data-stu-id="99d34-113">Requirement</span></span> | <span data-ttu-id="99d34-114">值</span><span class="sxs-lookup"><span data-stu-id="99d34-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99d34-115">標頭</span><span class="sxs-lookup"><span data-stu-id="99d34-115">Header</span></span><br/> | <dl> <span data-ttu-id="99d34-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="99d34-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99d34-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="99d34-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d34-118">函式</span><span class="sxs-lookup"><span data-stu-id="99d34-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="99d34-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="99d34-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





