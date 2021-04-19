---
description: 使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine：:D rawTransform 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000623"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="705b5-103">ID3DXLine：:D rawTransform 方法</span><span class="sxs-lookup"><span data-stu-id="705b5-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="705b5-104">使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。</span><span class="sxs-lookup"><span data-stu-id="705b5-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="705b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="705b5-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="705b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="705b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705b5-107">*pVertexList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="705b5-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705b5-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="705b5-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="705b5-109">構成線條的頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="705b5-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="705b5-110">請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="705b5-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="705b5-111">*dwVertexListCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="705b5-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705b5-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="705b5-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="705b5-113">頂點清單中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="705b5-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="705b5-114">*pTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="705b5-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705b5-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="705b5-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="705b5-116">調整、旋轉和轉譯 (SRT) 矩陣以轉換點。</span><span class="sxs-lookup"><span data-stu-id="705b5-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="705b5-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="705b5-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="705b5-118">如果此矩陣是投射矩陣，則會以觀點正確的 stippling 模式繪製任何 stippled 線。</span><span class="sxs-lookup"><span data-stu-id="705b5-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="705b5-119">或者，您可以轉換頂點並使用 [**ID3DXLine：:D raw**](id3dxline--draw.md) ，以 nonperspective 正確的 stipple 模式繪製行。</span><span class="sxs-lookup"><span data-stu-id="705b5-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="705b5-120">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="705b5-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705b5-121">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="705b5-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="705b5-122">線條的色彩。</span><span class="sxs-lookup"><span data-stu-id="705b5-122">Color of the line.</span></span> <span data-ttu-id="705b5-123">請參閱 [**D3DCOLOR**](d3dcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="705b5-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705b5-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="705b5-124">Return value</span></span>

<span data-ttu-id="705b5-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="705b5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="705b5-126">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="705b5-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="705b5-127">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="705b5-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="705b5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="705b5-128">Requirements</span></span>



| <span data-ttu-id="705b5-129">需求</span><span class="sxs-lookup"><span data-stu-id="705b5-129">Requirement</span></span> | <span data-ttu-id="705b5-130">值</span><span class="sxs-lookup"><span data-stu-id="705b5-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="705b5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="705b5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="705b5-132"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="705b5-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="705b5-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="705b5-133">Library</span></span><br/> | <dl> <span data-ttu-id="705b5-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="705b5-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="705b5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="705b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="705b5-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="705b5-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
