---
description: 應用程式會使用這個介面的方法來執行主要畫面格動畫集。
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: 'ID3DXKeyframedAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001793"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="d06e7-103">ID3DXKeyframedAnimationSet 介面</span><span class="sxs-lookup"><span data-stu-id="d06e7-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="d06e7-104">應用程式會使用這個介面的方法來執行主要畫面格動畫集。</span><span class="sxs-lookup"><span data-stu-id="d06e7-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="d06e7-105">成員</span><span class="sxs-lookup"><span data-stu-id="d06e7-105">Members</span></span>

<span data-ttu-id="d06e7-106">**ID3DXKeyframedAnimationSet** 介面繼承自 [**ID3DXAnimationSet**](id3dxanimationset.md)。</span><span class="sxs-lookup"><span data-stu-id="d06e7-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="d06e7-107">**ID3DXKeyframedAnimationSet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d06e7-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="d06e7-108">方法</span><span class="sxs-lookup"><span data-stu-id="d06e7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d06e7-109">方法</span><span class="sxs-lookup"><span data-stu-id="d06e7-109">Methods</span></span>

<span data-ttu-id="d06e7-110">**ID3DXKeyframedAnimationSet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d06e7-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="d06e7-111">方法</span><span class="sxs-lookup"><span data-stu-id="d06e7-111">Method</span></span>                                                                                   | <span data-ttu-id="d06e7-112">描述</span><span class="sxs-lookup"><span data-stu-id="d06e7-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d06e7-113">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="d06e7-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="d06e7-114">將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d06e7-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="d06e7-115">**GetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="d06e7-116">取得動畫集中特定回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d06e7-117">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="d06e7-118">使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="d06e7-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d06e7-119">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="d06e7-120">取得動畫集中的回呼索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="d06e7-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d06e7-121">**GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="d06e7-122">取得指定主要畫面格動畫中的旋轉索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="d06e7-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="d06e7-123">**GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="d06e7-124">取得指定主要畫面格動畫中的小數位數索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="d06e7-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d06e7-125">**GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="d06e7-126">取得指定主要畫面格動畫中的轉譯鍵數目。</span><span class="sxs-lookup"><span data-stu-id="d06e7-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="d06e7-127">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="d06e7-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="d06e7-128">取得動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="d06e7-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d06e7-129">**GetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="d06e7-130">取得動畫集中特定主要畫面格的旋轉資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d06e7-131">**GetRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="d06e7-132">使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="d06e7-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="d06e7-133">**GetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="d06e7-134">取得動畫集中特定主要畫面格的縮放資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d06e7-135">**GetScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="d06e7-136">使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="d06e7-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="d06e7-137">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="d06e7-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="d06e7-138">取得每秒發生的動畫主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="d06e7-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="d06e7-139">**GetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="d06e7-140">取得動畫集中特定主要畫面格的翻譯資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d06e7-141">**GetTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="d06e7-142">使用主要畫面格動畫所用的平移按鍵資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="d06e7-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="d06e7-143">**RegisterAnimationSRTKeys**</span><span class="sxs-lookup"><span data-stu-id="d06e7-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="d06e7-144">註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。</span><span class="sxs-lookup"><span data-stu-id="d06e7-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="d06e7-145">**SetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="d06e7-146">設定動畫集中特定回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d06e7-147">**SetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="d06e7-148">設定動畫集中特定主要畫面格的旋轉資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d06e7-149">**SetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="d06e7-150">設定動畫集中特定主要畫面格的縮放資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d06e7-151">**SetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="d06e7-152">設定動畫集中特定主要畫面格的翻譯資訊。</span><span class="sxs-lookup"><span data-stu-id="d06e7-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d06e7-153">**UnregisterAnimation**</span><span class="sxs-lookup"><span data-stu-id="d06e7-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="d06e7-154">從動畫集合中移除動畫資料。</span><span class="sxs-lookup"><span data-stu-id="d06e7-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d06e7-155">**UnregisterRotationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="d06e7-156">移除位於指定主要畫面格的旋轉資料。</span><span class="sxs-lookup"><span data-stu-id="d06e7-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d06e7-157">**UnregisterScaleKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="d06e7-158">移除位於指定主要畫面格的尺規資料。</span><span class="sxs-lookup"><span data-stu-id="d06e7-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d06e7-159">**UnregisterTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="d06e7-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="d06e7-160">移除位於指定主要畫面格的翻譯資料。</span><span class="sxs-lookup"><span data-stu-id="d06e7-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="d06e7-161">備註</span><span class="sxs-lookup"><span data-stu-id="d06e7-161">Remarks</span></span>

<span data-ttu-id="d06e7-162">使用 [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md)建立 keyframed 動畫集。</span><span class="sxs-lookup"><span data-stu-id="d06e7-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="d06e7-163">LPD3DXKEYFRAMEDANIMATIONSET 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d06e7-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="d06e7-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="d06e7-164">Requirements</span></span>



| <span data-ttu-id="d06e7-165">需求</span><span class="sxs-lookup"><span data-stu-id="d06e7-165">Requirement</span></span> | <span data-ttu-id="d06e7-166">值</span><span class="sxs-lookup"><span data-stu-id="d06e7-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d06e7-167">標頭</span><span class="sxs-lookup"><span data-stu-id="d06e7-167">Header</span></span><br/>  | <dl> <span data-ttu-id="d06e7-168"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="d06e7-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d06e7-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="d06e7-169">Library</span></span><br/> | <dl> <span data-ttu-id="d06e7-170"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d06e7-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d06e7-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d06e7-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06e7-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="d06e7-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="d06e7-173">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="d06e7-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




