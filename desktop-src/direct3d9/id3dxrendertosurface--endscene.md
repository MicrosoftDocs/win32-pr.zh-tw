---
description: 結束場景。
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'ID3DXRenderToSurface：： EndScene 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696607"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="52660-103">ID3DXRenderToSurface：： EndScene 方法</span><span class="sxs-lookup"><span data-stu-id="52660-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="52660-104">結束場景。</span><span class="sxs-lookup"><span data-stu-id="52660-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="52660-105">語法</span><span class="sxs-lookup"><span data-stu-id="52660-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="52660-106">參數</span><span class="sxs-lookup"><span data-stu-id="52660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52660-107">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52660-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52660-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52660-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52660-109">篩選選項，以 [D3DX \_ 篩選準則](d3dx-filter.md)列舉。</span><span class="sxs-lookup"><span data-stu-id="52660-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52660-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="52660-110">Return value</span></span>

<span data-ttu-id="52660-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52660-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52660-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="52660-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52660-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="52660-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="52660-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="52660-114">Requirements</span></span>



| <span data-ttu-id="52660-115">需求</span><span class="sxs-lookup"><span data-stu-id="52660-115">Requirement</span></span> | <span data-ttu-id="52660-116">值</span><span class="sxs-lookup"><span data-stu-id="52660-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52660-117">標頭</span><span class="sxs-lookup"><span data-stu-id="52660-117">Header</span></span><br/>  | <dl> <span data-ttu-id="52660-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="52660-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="52660-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="52660-119">Library</span></span><br/> | <dl> <span data-ttu-id="52660-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52660-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52660-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52660-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52660-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="52660-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="52660-123">**ID3DXRenderToSurface::BeginScene**</span><span class="sxs-lookup"><span data-stu-id="52660-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
