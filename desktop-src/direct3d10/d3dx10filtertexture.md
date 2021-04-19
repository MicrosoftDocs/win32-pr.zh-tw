---
description: 使用特定的材質篩選器產生 mipmap 鏈。
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: 'D3DX10FilterTexture 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990012"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="95e37-103">D3DX10FilterTexture 函式</span><span class="sxs-lookup"><span data-stu-id="95e37-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="95e37-104">使用特定的材質篩選器產生 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="95e37-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e37-105">語法</span><span class="sxs-lookup"><span data-stu-id="95e37-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="95e37-106">參數</span><span class="sxs-lookup"><span data-stu-id="95e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e37-107">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="95e37-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="95e37-108">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="95e37-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="95e37-109">要篩選的材質物件。</span><span class="sxs-lookup"><span data-stu-id="95e37-109">The texture object to be filtered.</span></span> <span data-ttu-id="95e37-110">請參閱 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="95e37-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="95e37-111">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="95e37-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="95e37-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e37-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e37-113">Mipmap 層級的資料會用來產生 mipmap 鏈的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="95e37-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="95e37-114">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="95e37-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="95e37-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e37-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e37-116">旗標控制每個 miplevel 的篩選方式 (或 D3DX10 \_ D3DX10 篩選方塊) 的預設值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="95e37-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="95e37-117">請參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="95e37-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e37-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="95e37-118">Return value</span></span>

<span data-ttu-id="95e37-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95e37-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95e37-120">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="95e37-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95e37-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="95e37-121">Requirements</span></span>



| <span data-ttu-id="95e37-122">需求</span><span class="sxs-lookup"><span data-stu-id="95e37-122">Requirement</span></span> | <span data-ttu-id="95e37-123">值</span><span class="sxs-lookup"><span data-stu-id="95e37-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95e37-124">標頭</span><span class="sxs-lookup"><span data-stu-id="95e37-124">Header</span></span><br/> | <dl> <span data-ttu-id="95e37-125"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="95e37-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e37-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95e37-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e37-127">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="95e37-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
