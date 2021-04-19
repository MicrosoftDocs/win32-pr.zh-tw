---
description: 使用主要畫面格動畫所用的平移按鍵資料來填滿陣列。
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'ID3DXKeyframedAnimationSet：： GetTranslationKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982905"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="d1a29-103">ID3DXKeyframedAnimationSet：： GetTranslationKeys 方法</span><span class="sxs-lookup"><span data-stu-id="d1a29-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="d1a29-104">使用主要畫面格動畫所用的平移按鍵資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="d1a29-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a29-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1a29-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="d1a29-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1a29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a29-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1a29-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a29-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1a29-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1a29-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="d1a29-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="d1a29-110">*pTranslationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1a29-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a29-111">類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="d1a29-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="d1a29-112">使用者配置的 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) 向量指標，此方法是用來填滿動畫轉譯資料。</span><span class="sxs-lookup"><span data-stu-id="d1a29-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a29-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1a29-113">Return value</span></span>

<span data-ttu-id="d1a29-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1a29-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1a29-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d1a29-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d1a29-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d1a29-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a29-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1a29-117">Requirements</span></span>



| <span data-ttu-id="d1a29-118">需求</span><span class="sxs-lookup"><span data-stu-id="d1a29-118">Requirement</span></span> | <span data-ttu-id="d1a29-119">值</span><span class="sxs-lookup"><span data-stu-id="d1a29-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a29-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d1a29-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d1a29-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a29-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d1a29-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1a29-122">Library</span></span><br/> | <dl> <span data-ttu-id="d1a29-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1a29-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1a29-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1a29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a29-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d1a29-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="d1a29-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="d1a29-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
