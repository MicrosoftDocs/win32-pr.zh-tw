---
title: D3DX_INT4_to_R8G8B8A8_SINT 函式
description: 將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ 聖。
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992154"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="5c17b-104">D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ 聖函數</span><span class="sxs-lookup"><span data-stu-id="5c17b-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="5c17b-105">將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ 聖。</span><span class="sxs-lookup"><span data-stu-id="5c17b-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c17b-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c17b-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5c17b-107">參數</span><span class="sxs-lookup"><span data-stu-id="5c17b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c17b-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="5c17b-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5c17b-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="5c17b-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c17b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c17b-110">Return value</span></span>

<span data-ttu-id="5c17b-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="5c17b-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c17b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c17b-112">Requirements</span></span>



| <span data-ttu-id="5c17b-113">需求</span><span class="sxs-lookup"><span data-stu-id="5c17b-113">Requirement</span></span> | <span data-ttu-id="5c17b-114">值</span><span class="sxs-lookup"><span data-stu-id="5c17b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c17b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5c17b-115">Header</span></span><br/> | <dl> <span data-ttu-id="5c17b-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="5c17b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c17b-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="5c17b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c17b-118">函式</span><span class="sxs-lookup"><span data-stu-id="5c17b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5c17b-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="5c17b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





