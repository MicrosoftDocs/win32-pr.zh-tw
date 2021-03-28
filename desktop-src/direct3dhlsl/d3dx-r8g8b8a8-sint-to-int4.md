---
title: D3DX_R8G8B8A8_SINT_to_INT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ 聖著色器資料到 XMINT4。
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116245"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="91006-104">D3DX \_ R8G8B8A8 \_ 聖 \_ 至 \_ INT4 函式</span><span class="sxs-lookup"><span data-stu-id="91006-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="91006-105">解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ 聖著色器資料到 XMINT4。</span><span class="sxs-lookup"><span data-stu-id="91006-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="91006-106">語法</span><span class="sxs-lookup"><span data-stu-id="91006-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="91006-107">參數</span><span class="sxs-lookup"><span data-stu-id="91006-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91006-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="91006-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="91006-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="91006-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91006-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="91006-110">Return value</span></span>

<span data-ttu-id="91006-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="91006-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="91006-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="91006-112">Requirements</span></span>



| <span data-ttu-id="91006-113">需求</span><span class="sxs-lookup"><span data-stu-id="91006-113">Requirement</span></span> | <span data-ttu-id="91006-114">值</span><span class="sxs-lookup"><span data-stu-id="91006-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91006-115">標頭</span><span class="sxs-lookup"><span data-stu-id="91006-115">Header</span></span><br/> | <dl> <span data-ttu-id="91006-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="91006-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91006-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="91006-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91006-118">函式</span><span class="sxs-lookup"><span data-stu-id="91006-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="91006-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="91006-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





