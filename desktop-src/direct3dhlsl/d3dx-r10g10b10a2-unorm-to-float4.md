---
title: D3DX_R10G10B10A2_UNORM_to_FLOAT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM 著色器資料至 XMFLOAT4。
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c93bd6fb9cce07ee13a873b4fade91bd322824
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974692"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a><span data-ttu-id="4b491-104">D3DX \_ R10G10B10A2 \_ UNORM \_ to \_ FLOAT4 function</span><span class="sxs-lookup"><span data-stu-id="4b491-104">D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="4b491-105">解壓縮 DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM 著色器資料至 XMFLOAT4。</span><span class="sxs-lookup"><span data-stu-id="4b491-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b491-106">語法</span><span class="sxs-lookup"><span data-stu-id="4b491-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4b491-107">參數</span><span class="sxs-lookup"><span data-stu-id="4b491-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b491-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="4b491-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4b491-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="4b491-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b491-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b491-110">Return value</span></span>

<span data-ttu-id="4b491-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="4b491-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b491-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b491-112">Requirements</span></span>



| <span data-ttu-id="4b491-113">需求</span><span class="sxs-lookup"><span data-stu-id="4b491-113">Requirement</span></span> | <span data-ttu-id="4b491-114">值</span><span class="sxs-lookup"><span data-stu-id="4b491-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b491-115">標頭</span><span class="sxs-lookup"><span data-stu-id="4b491-115">Header</span></span><br/> | <dl> <span data-ttu-id="4b491-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="4b491-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b491-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="4b491-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b491-118">函式</span><span class="sxs-lookup"><span data-stu-id="4b491-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4b491-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="4b491-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





