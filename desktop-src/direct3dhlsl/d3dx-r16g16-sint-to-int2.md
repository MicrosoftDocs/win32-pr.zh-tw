---
title: D3DX_R16G16_SINT_to_INT2 函式
description: 解壓縮 DXGI \_ FORMAT \_ R16G16 \_ 聖著色器資料到 XMINT2。
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- D3DX_R16G16_SINT_to_INT2 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992353"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="c77f4-104">D3DX \_ R16G16 \_ 聖 \_ 至 \_ INT2 函式</span><span class="sxs-lookup"><span data-stu-id="c77f4-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="c77f4-105">解壓縮 DXGI \_ FORMAT \_ R16G16 \_ 聖著色器資料到 XMINT2。</span><span class="sxs-lookup"><span data-stu-id="c77f4-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="c77f4-106">語法</span><span class="sxs-lookup"><span data-stu-id="c77f4-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c77f4-107">參數</span><span class="sxs-lookup"><span data-stu-id="c77f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c77f4-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="c77f4-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c77f4-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c77f4-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c77f4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c77f4-110">Return value</span></span>

<span data-ttu-id="c77f4-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c77f4-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c77f4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c77f4-112">Requirements</span></span>



| <span data-ttu-id="c77f4-113">需求</span><span class="sxs-lookup"><span data-stu-id="c77f4-113">Requirement</span></span> | <span data-ttu-id="c77f4-114">值</span><span class="sxs-lookup"><span data-stu-id="c77f4-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c77f4-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c77f4-115">Header</span></span><br/> | <dl> <span data-ttu-id="c77f4-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="c77f4-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c77f4-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="c77f4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77f4-118">函式</span><span class="sxs-lookup"><span data-stu-id="c77f4-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c77f4-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="c77f4-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





