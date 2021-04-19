---
description: 從動畫控制器移除動畫集。
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'ID3DXAnimationController：： UnregisterAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976746"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="21d3b-103">ID3DXAnimationController：： UnregisterAnimationSet 方法</span><span class="sxs-lookup"><span data-stu-id="21d3b-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="21d3b-104">從動畫控制器移除動畫集。</span><span class="sxs-lookup"><span data-stu-id="21d3b-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="21d3b-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="21d3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="21d3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d3b-107">*pAnimSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21d3b-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d3b-108">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="21d3b-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="21d3b-109">要移除之 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫集合的指標。</span><span class="sxs-lookup"><span data-stu-id="21d3b-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21d3b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="21d3b-110">Return value</span></span>

<span data-ttu-id="21d3b-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21d3b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21d3b-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="21d3b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="21d3b-113">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="21d3b-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d3b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="21d3b-114">Requirements</span></span>



| <span data-ttu-id="21d3b-115">需求</span><span class="sxs-lookup"><span data-stu-id="21d3b-115">Requirement</span></span> | <span data-ttu-id="21d3b-116">值</span><span class="sxs-lookup"><span data-stu-id="21d3b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21d3b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="21d3b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="21d3b-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="21d3b-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="21d3b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="21d3b-119">Library</span></span><br/> | <dl> <span data-ttu-id="21d3b-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21d3b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21d3b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21d3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d3b-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="21d3b-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




