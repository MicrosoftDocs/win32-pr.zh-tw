---
description: 將指定的矩陣載入至目前的矩陣。
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'ID3DXMATRIXStack：： LoadMatrix 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce6b99abf4c9a82a8b9d1c7643a1098d19e18c15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323383"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="3e6d2-103">ID3DXMATRIXStack：： LoadMatrix 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="3e6d2-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="3e6d2-104">將指定的矩陣載入至目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e6d2-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e6d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e6d2-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="3e6d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e6d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e6d2-107">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e6d2-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e6d2-108">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e6d2-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3e6d2-109">載入至目前矩陣的 D3DXMATRIX 結構指標。</span><span class="sxs-lookup"><span data-stu-id="3e6d2-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e6d2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e6d2-110">Return value</span></span>

<span data-ttu-id="3e6d2-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e6d2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e6d2-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3e6d2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e6d2-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="3e6d2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e6d2-114">備註</span><span class="sxs-lookup"><span data-stu-id="3e6d2-114">Remarks</span></span>

<span data-ttu-id="3e6d2-115">請注意，這個方法不會將專案新增至堆疊。相反地，它會將目前的矩陣取代為提供的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3e6d2-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6d2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e6d2-116">Requirements</span></span>



| <span data-ttu-id="3e6d2-117">需求</span><span class="sxs-lookup"><span data-stu-id="3e6d2-117">Requirement</span></span> | <span data-ttu-id="3e6d2-118">值</span><span class="sxs-lookup"><span data-stu-id="3e6d2-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6d2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3e6d2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3e6d2-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e6d2-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e6d2-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e6d2-121">Library</span></span><br/> | <dl> <span data-ttu-id="3e6d2-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e6d2-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e6d2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e6d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6d2-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="3e6d2-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="3e6d2-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="3e6d2-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
