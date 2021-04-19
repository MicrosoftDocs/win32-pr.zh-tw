---
description: 將 cube 地圖中表示的函式投射到球面諧波。
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: 'D3DX10SHProjectCubeMap 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982015"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="2efa4-103">D3DX10SHProjectCubeMap 函式</span><span class="sxs-lookup"><span data-stu-id="2efa4-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="2efa4-104">將 cube 地圖中表示的函式投射到球面諧波。</span><span class="sxs-lookup"><span data-stu-id="2efa4-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="2efa4-105">語法</span><span class="sxs-lookup"><span data-stu-id="2efa4-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="2efa4-106">參數</span><span class="sxs-lookup"><span data-stu-id="2efa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2efa4-107">*順序*</span><span class="sxs-lookup"><span data-stu-id="2efa4-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="2efa4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2efa4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2efa4-109">SH 評估的順序會產生 Order ^ 2 coefs，度數為 Order-1。</span><span class="sxs-lookup"><span data-stu-id="2efa4-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="2efa4-110">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="2efa4-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="2efa4-111">類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="2efa4-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="2efa4-112">即將投射到球形諧波的立方體貼圖。</span><span class="sxs-lookup"><span data-stu-id="2efa4-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="2efa4-113">請參閱 [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)。</span><span class="sxs-lookup"><span data-stu-id="2efa4-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="2efa4-114">*pROut*</span><span class="sxs-lookup"><span data-stu-id="2efa4-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="2efa4-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2efa4-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2efa4-116">紅色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="2efa4-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="2efa4-117">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="2efa4-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="2efa4-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2efa4-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2efa4-119">綠色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="2efa4-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="2efa4-120">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="2efa4-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="2efa4-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2efa4-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2efa4-122">藍色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="2efa4-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2efa4-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="2efa4-123">Return value</span></span>

<span data-ttu-id="2efa4-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2efa4-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2efa4-125">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2efa4-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2efa4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2efa4-126">Requirements</span></span>



| <span data-ttu-id="2efa4-127">需求</span><span class="sxs-lookup"><span data-stu-id="2efa4-127">Requirement</span></span> | <span data-ttu-id="2efa4-128">值</span><span class="sxs-lookup"><span data-stu-id="2efa4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2efa4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2efa4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2efa4-130"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="2efa4-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2efa4-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="2efa4-131">Library</span></span><br/> | <dl> <span data-ttu-id="2efa4-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2efa4-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2efa4-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2efa4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efa4-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="2efa4-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
