---
description: 取得動畫集合的縮放、旋轉和轉譯值。
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet：： GetSRT 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988218"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="a3f0b-103">ID3DXAnimationSet：： GetSRT 方法</span><span class="sxs-lookup"><span data-stu-id="a3f0b-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="a3f0b-104">取得動畫集合的縮放、旋轉和轉譯值。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3f0b-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="a3f0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f0b-107">*PeriodicPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3f0b-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f0b-108">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3f0b-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3f0b-109">動畫集合的位置。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-109">Position of the animation set.</span></span> <span data-ttu-id="a3f0b-110">您可以藉由呼叫 [**ID3DXAnimationSet：： GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)來取得位置。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3f0b-111">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3f0b-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f0b-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3f0b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3f0b-113">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="a3f0b-114">*pScale* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3f0b-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f0b-115">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3f0b-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3f0b-116">描述動畫集合尺規的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="a3f0b-117">*pRotation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3f0b-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f0b-118">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3f0b-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a3f0b-119">[**D3DXQUATERNION**](d3dxquaternion.md)四元數的指標，該四元數描述動畫集合的旋轉。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="a3f0b-120">*pTranslation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3f0b-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f0b-121">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3f0b-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3f0b-122">描述動畫集合轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f0b-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3f0b-123">Return value</span></span>

<span data-ttu-id="a3f0b-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3f0b-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3f0b-125">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="a3f0b-126">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="a3f0b-127">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a3f0b-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f0b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3f0b-128">Requirements</span></span>



| <span data-ttu-id="a3f0b-129">需求</span><span class="sxs-lookup"><span data-stu-id="a3f0b-129">Requirement</span></span> | <span data-ttu-id="a3f0b-130">值</span><span class="sxs-lookup"><span data-stu-id="a3f0b-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f0b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a3f0b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f0b-132"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f0b-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a3f0b-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3f0b-133">Library</span></span><br/> | <dl> <span data-ttu-id="a3f0b-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3f0b-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3f0b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3f0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f0b-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a3f0b-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
