---
description: 移除位於指定主要畫面格的翻譯資料。
ms.assetid: 58cadf5d-f687-4644-83b0-e124ef2bcb5a
title: 'ID3DXKeyframedAnimationSet：： UnregisterTranslationKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 127aaa707c364e51815af09b8222d73102281b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982903"
---
# <a name="id3dxkeyframedanimationsetunregistertranslationkey-method"></a><span data-ttu-id="a70b4-103">ID3DXKeyframedAnimationSet：： UnregisterTranslationKey 方法</span><span class="sxs-lookup"><span data-stu-id="a70b4-103">ID3DXKeyframedAnimationSet::UnregisterTranslationKey method</span></span>

<span data-ttu-id="a70b4-104">移除位於指定主要畫面格的翻譯資料。</span><span class="sxs-lookup"><span data-stu-id="a70b4-104">Removes the translation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="a70b4-105">Syntax</span></span>


```C++
HRESULT UnregisterTranslationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="a70b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="a70b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a70b4-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a70b4-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70b4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a70b4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a70b4-109">動畫識別碼。</span><span class="sxs-lookup"><span data-stu-id="a70b4-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a70b4-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a70b4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70b4-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a70b4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a70b4-112">主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="a70b4-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a70b4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a70b4-113">Return value</span></span>

<span data-ttu-id="a70b4-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a70b4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a70b4-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a70b4-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a70b4-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a70b4-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a70b4-117">備註</span><span class="sxs-lookup"><span data-stu-id="a70b4-117">Remarks</span></span>

<span data-ttu-id="a70b4-118">這個方法很慢，而且不應該在動畫開始播放之後使用。</span><span class="sxs-lookup"><span data-stu-id="a70b4-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="a70b4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a70b4-119">Requirements</span></span>



| <span data-ttu-id="a70b4-120">需求</span><span class="sxs-lookup"><span data-stu-id="a70b4-120">Requirement</span></span> | <span data-ttu-id="a70b4-121">值</span><span class="sxs-lookup"><span data-stu-id="a70b4-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a70b4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a70b4-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a70b4-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a70b4-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a70b4-124">Library</span></span><br/> | <dl> <span data-ttu-id="a70b4-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70b4-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a70b4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a70b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70b4-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a70b4-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
