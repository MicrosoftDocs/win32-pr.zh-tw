---
description: 使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet：： GetScaleKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000624"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="9de7d-103">ID3DXKeyframedAnimationSet：： GetScaleKeys 方法</span><span class="sxs-lookup"><span data-stu-id="9de7d-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="9de7d-104">使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="9de7d-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de7d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9de7d-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="9de7d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9de7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de7d-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9de7d-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de7d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de7d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9de7d-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="9de7d-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="9de7d-110">*pScaleKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9de7d-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de7d-111">類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="9de7d-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="9de7d-112">[**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)向量的使用者配置陣列指標，此方法是用來填滿動畫尺規資料。</span><span class="sxs-lookup"><span data-stu-id="9de7d-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de7d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9de7d-113">Return value</span></span>

<span data-ttu-id="9de7d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9de7d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9de7d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9de7d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9de7d-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9de7d-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de7d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de7d-117">Requirements</span></span>



| <span data-ttu-id="9de7d-118">需求</span><span class="sxs-lookup"><span data-stu-id="9de7d-118">Requirement</span></span> | <span data-ttu-id="9de7d-119">值</span><span class="sxs-lookup"><span data-stu-id="9de7d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9de7d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9de7d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9de7d-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="9de7d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9de7d-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="9de7d-122">Library</span></span><br/> | <dl> <span data-ttu-id="9de7d-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9de7d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9de7d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de7d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de7d-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9de7d-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="9de7d-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="9de7d-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
