---
description: 建立效果集區。 集區是用來共用效果之間的參數。
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: 'D3DXCreateEffectPool 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196412"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="d9060-104">D3DXCreateEffectPool 函式</span><span class="sxs-lookup"><span data-stu-id="d9060-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="d9060-105">建立效果集區。</span><span class="sxs-lookup"><span data-stu-id="d9060-105">Create an effect pool.</span></span> <span data-ttu-id="d9060-106">集區是用來共用效果之間的參數。</span><span class="sxs-lookup"><span data-stu-id="d9060-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9060-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9060-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="d9060-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9060-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9060-109">*ppPool* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9060-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9060-110">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9060-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="d9060-111">傳回已建立之集區的指標。</span><span class="sxs-lookup"><span data-stu-id="d9060-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9060-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9060-112">Return value</span></span>

<span data-ttu-id="d9060-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9060-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9060-114">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d9060-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="d9060-115">如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d9060-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="d9060-116">如果方法失敗，傳回值將會是 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="d9060-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9060-117">備註</span><span class="sxs-lookup"><span data-stu-id="d9060-117">Remarks</span></span>

<span data-ttu-id="d9060-118">針對集區中的效果，具有相同名稱共用值的共用參數。</span><span class="sxs-lookup"><span data-stu-id="d9060-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9060-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9060-119">Requirements</span></span>



| <span data-ttu-id="d9060-120">需求</span><span class="sxs-lookup"><span data-stu-id="d9060-120">Requirement</span></span> | <span data-ttu-id="d9060-121">值</span><span class="sxs-lookup"><span data-stu-id="d9060-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9060-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d9060-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9060-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9060-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d9060-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9060-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9060-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9060-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d9060-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9060-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9060-127">效果函數</span><span class="sxs-lookup"><span data-stu-id="d9060-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




