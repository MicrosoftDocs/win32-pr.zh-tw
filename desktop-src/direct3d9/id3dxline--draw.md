---
description: 在螢幕空間中繪製帶狀線。 輸入的格式為數組，可定義 D3DXVECTOR2) 在行條紋 (的點。
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: 'ID3DXLine：:D 原始方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975707"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="3c4ca-104">ID3DXLine：:D 原始方法</span><span class="sxs-lookup"><span data-stu-id="3c4ca-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="3c4ca-105">在螢幕空間中繪製帶狀線。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="3c4ca-106">輸入的格式為數組，可定義 [**D3DXVECTOR2**](d3dxvector2.md)) 在行條紋 (的點。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c4ca-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="3c4ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="3c4ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4ca-109">*pVertexList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c4ca-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ca-110">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c4ca-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3c4ca-111">構成線條的頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="3c4ca-112">請參閱 [**D3DXVECTOR2**](d3dxvector2.md)。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c4ca-113">*dwVertexListCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c4ca-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ca-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c4ca-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c4ca-115">頂點清單中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="3c4ca-116">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c4ca-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ca-117">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3c4ca-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3c4ca-118">線條的色彩。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-118">Color of the line.</span></span> <span data-ttu-id="3c4ca-119">請參閱 [**D3DCOLOR**](d3dcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4ca-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c4ca-120">Return value</span></span>

<span data-ttu-id="3c4ca-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c4ca-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c4ca-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c4ca-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="3c4ca-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4ca-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c4ca-124">Requirements</span></span>



| <span data-ttu-id="3c4ca-125">需求</span><span class="sxs-lookup"><span data-stu-id="3c4ca-125">Requirement</span></span> | <span data-ttu-id="3c4ca-126">值</span><span class="sxs-lookup"><span data-stu-id="3c4ca-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4ca-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3c4ca-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3c4ca-128"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ca-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3c4ca-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c4ca-129">Library</span></span><br/> | <dl> <span data-ttu-id="3c4ca-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ca-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c4ca-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c4ca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4ca-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="3c4ca-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
