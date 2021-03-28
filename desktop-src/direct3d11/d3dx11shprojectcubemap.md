---
title: 'D3DX11SHProjectCubeMap 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用球形諧波數學程式庫 SHProjectCubeMap。
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992259"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="ec103-105">D3DX11SHProjectCubeMap 函式</span><span class="sxs-lookup"><span data-stu-id="ec103-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="ec103-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec103-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec103-107">我們建議您不要使用這個函數，而是使用 [球形諧波數學](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) 程式庫 **SHProjectCubeMap**。</span><span class="sxs-lookup"><span data-stu-id="ec103-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="ec103-108">將 cube 地圖中表示的函式投射到球面諧波。</span><span class="sxs-lookup"><span data-stu-id="ec103-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec103-109">語法</span><span class="sxs-lookup"><span data-stu-id="ec103-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="ec103-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec103-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec103-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="ec103-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-112">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="ec103-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="ec103-113">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ec103-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="ec103-114">*順序*</span><span class="sxs-lookup"><span data-stu-id="ec103-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec103-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec103-116">SH 評估的順序會產生順序 ^ 2 係數，其度為順序-1。</span><span class="sxs-lookup"><span data-stu-id="ec103-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="ec103-117">有效範圍介於2到6之間。</span><span class="sxs-lookup"><span data-stu-id="ec103-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="ec103-118">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="ec103-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-119">類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="ec103-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="ec103-120">[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)的指標，代表即將投射到球面諧波的立方體貼圖。</span><span class="sxs-lookup"><span data-stu-id="ec103-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="ec103-121">*pROut*</span><span class="sxs-lookup"><span data-stu-id="ec103-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-122">類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ec103-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ec103-123">紅色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="ec103-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="ec103-124">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="ec103-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-125">類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ec103-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ec103-126">綠色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="ec103-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="ec103-127">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="ec103-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ec103-128">類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="ec103-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="ec103-129">藍色的輸出 SH 向量。</span><span class="sxs-lookup"><span data-stu-id="ec103-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec103-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec103-130">Return value</span></span>

<span data-ttu-id="ec103-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec103-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec103-132">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ec103-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec103-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec103-133">Requirements</span></span>



| <span data-ttu-id="ec103-134">需求</span><span class="sxs-lookup"><span data-stu-id="ec103-134">Requirement</span></span> | <span data-ttu-id="ec103-135">值</span><span class="sxs-lookup"><span data-stu-id="ec103-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec103-136">標頭</span><span class="sxs-lookup"><span data-stu-id="ec103-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ec103-137"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec103-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ec103-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec103-138">Library</span></span><br/> | <dl> <span data-ttu-id="ec103-139"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec103-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ec103-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec103-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec103-141">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="ec103-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

