---
description: ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法-使用用於主要畫面格動畫的回呼金鑰資料來填滿陣列。
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093716"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="2a168-103">ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法</span><span class="sxs-lookup"><span data-stu-id="2a168-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="2a168-104">使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="2a168-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a168-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a168-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="2a168-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a168-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a168-107">*pCallbackKeys* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2a168-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a168-108">類型： **[ **LPD3DXKEY \_ 回呼**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="2a168-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="2a168-109">方法用來填滿回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構之使用者配置陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="2a168-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a168-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a168-110">Return value</span></span>

<span data-ttu-id="2a168-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a168-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a168-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2a168-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a168-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2a168-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a168-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a168-114">Requirements</span></span>



| <span data-ttu-id="2a168-115">需求</span><span class="sxs-lookup"><span data-stu-id="2a168-115">Requirement</span></span> | <span data-ttu-id="2a168-116">值</span><span class="sxs-lookup"><span data-stu-id="2a168-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a168-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2a168-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2a168-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a168-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2a168-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a168-119">Library</span></span><br/> | <dl> <span data-ttu-id="2a168-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a168-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a168-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a168-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a168-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="2a168-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="2a168-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="2a168-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




