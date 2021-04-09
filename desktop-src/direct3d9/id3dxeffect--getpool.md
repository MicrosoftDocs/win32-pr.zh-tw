---
description: 取得共用參數集區的指標。
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect：： >pooloperations.getpool 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946060"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="afa44-103">ID3DXEffect：： >pooloperations.getpool 方法</span><span class="sxs-lookup"><span data-stu-id="afa44-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="afa44-104">取得共用參數集區的指標。</span><span class="sxs-lookup"><span data-stu-id="afa44-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa44-105">語法</span><span class="sxs-lookup"><span data-stu-id="afa44-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="afa44-106">參數</span><span class="sxs-lookup"><span data-stu-id="afa44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa44-107">*ppPool* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="afa44-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afa44-108">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="afa44-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="afa44-109">[**ID3DXEffectPool**](id3dxeffectpool.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="afa44-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa44-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="afa44-110">Return value</span></span>

<span data-ttu-id="afa44-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="afa44-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="afa44-112">這個方法一律會傳回值 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="afa44-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="afa44-113">備註</span><span class="sxs-lookup"><span data-stu-id="afa44-113">Remarks</span></span>

<span data-ttu-id="afa44-114">集區包含效果之間的共用參數。</span><span class="sxs-lookup"><span data-stu-id="afa44-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="afa44-115">請參閱 [複製和共用 (Direct3D 9) ](cloning-and-sharing.md)。</span><span class="sxs-lookup"><span data-stu-id="afa44-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afa44-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="afa44-116">Requirements</span></span>



| <span data-ttu-id="afa44-117">需求</span><span class="sxs-lookup"><span data-stu-id="afa44-117">Requirement</span></span> | <span data-ttu-id="afa44-118">值</span><span class="sxs-lookup"><span data-stu-id="afa44-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa44-119">標頭</span><span class="sxs-lookup"><span data-stu-id="afa44-119">Header</span></span><br/>  | <dl> <span data-ttu-id="afa44-120"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="afa44-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="afa44-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="afa44-121">Library</span></span><br/> | <dl> <span data-ttu-id="afa44-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="afa44-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="afa44-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afa44-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa44-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="afa44-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




