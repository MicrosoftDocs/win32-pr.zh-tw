---
description: 註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet：： RegisterAnimationSRTKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999982"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="7ce4c-103">ID3DXKeyframedAnimationSet：： RegisterAnimationSRTKeys 方法</span><span class="sxs-lookup"><span data-stu-id="7ce4c-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="7ce4c-104">註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce4c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7ce4c-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="7ce4c-106">參數</span><span class="sxs-lookup"><span data-stu-id="7ce4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce4c-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce4c-109">動畫名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-110">*NumScaleKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce4c-112">調整金鑰數目。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-113">*NumRotationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce4c-115">輪替索引鍵的數目。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-116">*NumTranslationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce4c-118">轉譯金鑰數目。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-119">*pScaleKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-120">Type： **Const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ce4c-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="7ce4c-121">使用者配置的 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) 向量指標的位址，此方法會以調整資料填滿該陣列。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-122">*pRotationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-123">Type： **Const [**LPD3DXKEY \_ 四元數**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ce4c-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="7ce4c-124">[**D3DXKEY \_ 四元**](d3dxkey-quaternion.md)數四元數之使用者配置陣列的指標位址，此方法會以旋轉資料填滿。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-125">*pTranslationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-126">Type： **Const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ce4c-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="7ce4c-127">使用者配置的 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) 向量指標的位址，此方法會以轉譯資料填滿該陣列。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="7ce4c-128">*pAnimationIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ce4c-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce4c-129">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ce4c-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ce4c-130">傳回動畫索引。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce4c-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ce4c-131">Return value</span></span>

<span data-ttu-id="7ce4c-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ce4c-133">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7ce4c-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7ce4c-134">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="7ce4c-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce4c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ce4c-135">Requirements</span></span>



| <span data-ttu-id="7ce4c-136">需求</span><span class="sxs-lookup"><span data-stu-id="7ce4c-136">Requirement</span></span> | <span data-ttu-id="7ce4c-137">值</span><span class="sxs-lookup"><span data-stu-id="7ce4c-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce4c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="7ce4c-138">Header</span></span><br/>  | <dl> <span data-ttu-id="7ce4c-139"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce4c-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7ce4c-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ce4c-140">Library</span></span><br/> | <dl> <span data-ttu-id="7ce4c-141"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ce4c-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ce4c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ce4c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce4c-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="7ce4c-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="7ce4c-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="7ce4c-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="7ce4c-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="7ce4c-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
