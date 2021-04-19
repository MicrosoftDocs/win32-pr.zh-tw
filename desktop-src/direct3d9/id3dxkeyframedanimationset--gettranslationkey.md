---
description: 取得動畫集中特定主要畫面格的翻譯資訊。
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'ID3DXKeyframedAnimationSet：： GetTranslationKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986545"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="a0e60-103">ID3DXKeyframedAnimationSet：： GetTranslationKey 方法</span><span class="sxs-lookup"><span data-stu-id="a0e60-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="a0e60-104">取得動畫集中特定主要畫面格的翻譯資訊。</span><span class="sxs-lookup"><span data-stu-id="a0e60-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e60-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0e60-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="a0e60-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0e60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e60-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0e60-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e60-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e60-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0e60-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="a0e60-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="a0e60-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0e60-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e60-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e60-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0e60-112">主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="a0e60-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0e60-113">*pTranslationKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a0e60-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e60-114">類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e60-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="a0e60-115">旋轉資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="a0e60-115">Pointer to the rotation information.</span></span> <span data-ttu-id="a0e60-116">請參閱 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)。</span><span class="sxs-lookup"><span data-stu-id="a0e60-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0e60-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0e60-117">Return value</span></span>

<span data-ttu-id="a0e60-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0e60-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0e60-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a0e60-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a0e60-120">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a0e60-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e60-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0e60-121">Requirements</span></span>



| <span data-ttu-id="a0e60-122">需求</span><span class="sxs-lookup"><span data-stu-id="a0e60-122">Requirement</span></span> | <span data-ttu-id="a0e60-123">值</span><span class="sxs-lookup"><span data-stu-id="a0e60-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e60-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a0e60-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a0e60-125"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e60-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a0e60-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0e60-126">Library</span></span><br/> | <dl> <span data-ttu-id="a0e60-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0e60-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0e60-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0e60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e60-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a0e60-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
