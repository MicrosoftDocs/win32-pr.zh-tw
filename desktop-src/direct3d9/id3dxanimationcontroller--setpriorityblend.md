---
description: 設定動畫控制器所使用的優先順序混合權數。
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController：： SetPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000613"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="a5fa0-103">ID3DXAnimationController：： SetPriorityBlend 方法</span><span class="sxs-lookup"><span data-stu-id="a5fa0-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="a5fa0-104">設定動畫控制器所使用的優先順序混合權數。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fa0-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5fa0-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="a5fa0-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5fa0-107">*BlendWeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5fa0-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa0-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5fa0-109">動畫控制器所使用的優先順序混合權數。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5fa0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5fa0-110">Return value</span></span>

<span data-ttu-id="a5fa0-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5fa0-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5fa0-113">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5fa0-114">備註</span><span class="sxs-lookup"><span data-stu-id="a5fa0-114">Remarks</span></span>

<span data-ttu-id="a5fa0-115">Blend 權數是用來將高優先順序和低優先順序的追蹤一起結合在一起。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fa0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5fa0-116">Requirements</span></span>



| <span data-ttu-id="a5fa0-117">需求</span><span class="sxs-lookup"><span data-stu-id="a5fa0-117">Requirement</span></span> | <span data-ttu-id="a5fa0-118">值</span><span class="sxs-lookup"><span data-stu-id="a5fa0-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fa0-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a5fa0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a5fa0-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa0-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a5fa0-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5fa0-121">Library</span></span><br/> | <dl> <span data-ttu-id="a5fa0-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa0-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5fa0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5fa0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fa0-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a5fa0-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="a5fa0-125">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
