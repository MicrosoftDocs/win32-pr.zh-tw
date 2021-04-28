---
description: ID3DXKeyframedAnimationSet：： GetCallbackKey 方法-取得動畫集中特定回呼的相關資訊。
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet：： GetCallbackKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f3ebbf93bd482a2259ffdaaf272c65b5e86d5270
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090316"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="4665e-103">ID3DXKeyframedAnimationSet：： GetCallbackKey 方法</span><span class="sxs-lookup"><span data-stu-id="4665e-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="4665e-104">取得動畫集中特定回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4665e-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4665e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4665e-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="4665e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4665e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4665e-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4665e-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4665e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4665e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4665e-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="4665e-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="4665e-110">*pCallbackKeys* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4665e-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4665e-111">類型： **[ **LPD3DXKEY \_ 回呼**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="4665e-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="4665e-112">[**回呼函數**](d3dxkey-callback.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="4665e-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4665e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4665e-113">Return value</span></span>

<span data-ttu-id="4665e-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4665e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4665e-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4665e-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4665e-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="4665e-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4665e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4665e-117">Requirements</span></span>



| <span data-ttu-id="4665e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4665e-118">Requirement</span></span> | <span data-ttu-id="4665e-119">值</span><span class="sxs-lookup"><span data-stu-id="4665e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4665e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4665e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4665e-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="4665e-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4665e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="4665e-122">Library</span></span><br/> | <dl> <span data-ttu-id="4665e-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4665e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4665e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4665e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4665e-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4665e-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
