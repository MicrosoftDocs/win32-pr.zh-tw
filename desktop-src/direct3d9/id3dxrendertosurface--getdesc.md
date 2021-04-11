---
description: 捕獲呈現介面的參數。
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface：： GetDesc 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196432"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="691e9-103">ID3DXRenderToSurface：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="691e9-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="691e9-104">捕獲呈現介面的參數。</span><span class="sxs-lookup"><span data-stu-id="691e9-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="691e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="691e9-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="691e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="691e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="691e9-107">*pParameters* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="691e9-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="691e9-108">類型： **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="691e9-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="691e9-109">[**D3DXRTS \_ DESC**](d3dxrts-desc.md)結構的指標，描述呈現介面的參數。</span><span class="sxs-lookup"><span data-stu-id="691e9-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="691e9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="691e9-110">Return value</span></span>

<span data-ttu-id="691e9-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="691e9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="691e9-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="691e9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="691e9-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="691e9-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="691e9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="691e9-114">Requirements</span></span>



| <span data-ttu-id="691e9-115">需求</span><span class="sxs-lookup"><span data-stu-id="691e9-115">Requirement</span></span> | <span data-ttu-id="691e9-116">值</span><span class="sxs-lookup"><span data-stu-id="691e9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="691e9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="691e9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="691e9-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="691e9-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="691e9-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="691e9-119">Library</span></span><br/> | <dl> <span data-ttu-id="691e9-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="691e9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="691e9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="691e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691e9-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="691e9-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




