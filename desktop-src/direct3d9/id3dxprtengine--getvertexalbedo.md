---
description: 抓取網格頂點的 >albedo 值。
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'ID3DXPRTEngine：： GetVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986542"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a><span data-ttu-id="b6052-103">ID3DXPRTEngine：： GetVertexAlbedo 方法</span><span class="sxs-lookup"><span data-stu-id="b6052-103">ID3DXPRTEngine::GetVertexAlbedo method</span></span>

<span data-ttu-id="b6052-104">抓取網格頂點的 >albedo 值。</span><span class="sxs-lookup"><span data-stu-id="b6052-104">Retrieves albedo values of the mesh vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6052-105">語法</span><span class="sxs-lookup"><span data-stu-id="b6052-105">Syntax</span></span>


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a><span data-ttu-id="b6052-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6052-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6052-107">*pVertColors* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b6052-107">*pVertColors* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6052-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6052-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b6052-109">網格頂點的 >albedo 值之目的地陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b6052-109">Pointer to a destination array of albedo values of the mesh vertices.</span></span> <span data-ttu-id="b6052-110">請參閱 [**D3DXCOLOR**](d3dxcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="b6052-110">See [**D3DXCOLOR**](d3dxcolor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6052-111">*NumVerts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6052-111">*NumVerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6052-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6052-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6052-113">網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="b6052-113">Number of vertices in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6052-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6052-114">Return value</span></span>

<span data-ttu-id="b6052-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6052-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6052-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b6052-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b6052-117">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b6052-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6052-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6052-118">Requirements</span></span>



| <span data-ttu-id="b6052-119">需求</span><span class="sxs-lookup"><span data-stu-id="b6052-119">Requirement</span></span> | <span data-ttu-id="b6052-120">值</span><span class="sxs-lookup"><span data-stu-id="b6052-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6052-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b6052-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b6052-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6052-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b6052-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6052-123">Library</span></span><br/> | <dl> <span data-ttu-id="b6052-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6052-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b6052-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6052-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6052-126">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b6052-126">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
