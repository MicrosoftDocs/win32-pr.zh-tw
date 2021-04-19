---
description: 將動畫集加入至動畫控制器。
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'ID3DXAnimationController：： RegisterAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981080"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="1453f-103">ID3DXAnimationController：： RegisterAnimationSet 方法</span><span class="sxs-lookup"><span data-stu-id="1453f-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="1453f-104">將動畫集加入至動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="1453f-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="1453f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1453f-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="1453f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1453f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1453f-107">*pAnimSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1453f-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1453f-108">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="1453f-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="1453f-109">要加入之 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫集合的指標。</span><span class="sxs-lookup"><span data-stu-id="1453f-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1453f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1453f-110">Return value</span></span>

<span data-ttu-id="1453f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1453f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1453f-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1453f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1453f-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1453f-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1453f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1453f-114">Requirements</span></span>



| <span data-ttu-id="1453f-115">需求</span><span class="sxs-lookup"><span data-stu-id="1453f-115">Requirement</span></span> | <span data-ttu-id="1453f-116">值</span><span class="sxs-lookup"><span data-stu-id="1453f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1453f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1453f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1453f-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="1453f-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1453f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="1453f-119">Library</span></span><br/> | <dl> <span data-ttu-id="1453f-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1453f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1453f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1453f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1453f-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1453f-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




