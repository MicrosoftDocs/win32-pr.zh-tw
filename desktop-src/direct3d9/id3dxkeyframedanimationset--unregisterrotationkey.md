---
description: 移除位於指定主要畫面格的旋轉資料。
ms.assetid: 8e95d684-fa22-4eba-a721-e7551e8f393b
title: 'ID3DXKeyframedAnimationSet：： UnregisterRotationKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 420a15d0086f94def7db8c7d558640d03b69562f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981855"
---
# <a name="id3dxkeyframedanimationsetunregisterrotationkey-method"></a><span data-ttu-id="69dd5-103">ID3DXKeyframedAnimationSet：： UnregisterRotationKey 方法</span><span class="sxs-lookup"><span data-stu-id="69dd5-103">ID3DXKeyframedAnimationSet::UnregisterRotationKey method</span></span>

<span data-ttu-id="69dd5-104">移除位於指定主要畫面格的旋轉資料。</span><span class="sxs-lookup"><span data-stu-id="69dd5-104">Removes the rotation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="69dd5-105">語法</span><span class="sxs-lookup"><span data-stu-id="69dd5-105">Syntax</span></span>


```C++
HRESULT UnregisterRotationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="69dd5-106">參數</span><span class="sxs-lookup"><span data-stu-id="69dd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69dd5-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69dd5-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dd5-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69dd5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69dd5-109">動畫識別碼。</span><span class="sxs-lookup"><span data-stu-id="69dd5-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="69dd5-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69dd5-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69dd5-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69dd5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69dd5-112">主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="69dd5-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69dd5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="69dd5-113">Return value</span></span>

<span data-ttu-id="69dd5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69dd5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69dd5-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="69dd5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69dd5-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="69dd5-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="69dd5-117">備註</span><span class="sxs-lookup"><span data-stu-id="69dd5-117">Remarks</span></span>

<span data-ttu-id="69dd5-118">這個方法很慢，而且不應該在動畫開始播放之後使用。</span><span class="sxs-lookup"><span data-stu-id="69dd5-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="69dd5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="69dd5-119">Requirements</span></span>



| <span data-ttu-id="69dd5-120">需求</span><span class="sxs-lookup"><span data-stu-id="69dd5-120">Requirement</span></span> | <span data-ttu-id="69dd5-121">值</span><span class="sxs-lookup"><span data-stu-id="69dd5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69dd5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="69dd5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="69dd5-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="69dd5-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="69dd5-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="69dd5-124">Library</span></span><br/> | <dl> <span data-ttu-id="69dd5-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69dd5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69dd5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69dd5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69dd5-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="69dd5-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
