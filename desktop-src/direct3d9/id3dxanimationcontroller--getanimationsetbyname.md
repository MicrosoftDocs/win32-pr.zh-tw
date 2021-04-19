---
description: 取得動畫集合，並指定其名稱。
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController：： GetAnimationSetByName 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982893"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="5e654-103">ID3DXAnimationController：： GetAnimationSetByName 方法</span><span class="sxs-lookup"><span data-stu-id="5e654-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="5e654-104">取得動畫集合，並指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="5e654-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e654-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e654-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="5e654-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e654-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e654-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e654-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e654-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e654-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e654-109">字串，包含動畫集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e654-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="5e654-110">*ppAnimSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5e654-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e654-111">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e654-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="5e654-112">[**ID3DXAnimationSet**](id3dxanimationset.md)動畫集合的指標。</span><span class="sxs-lookup"><span data-stu-id="5e654-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e654-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e654-113">Return value</span></span>

<span data-ttu-id="5e654-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e654-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e654-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5e654-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5e654-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5e654-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e654-117">備註</span><span class="sxs-lookup"><span data-stu-id="5e654-117">Remarks</span></span>

<span data-ttu-id="5e654-118">動畫控制器包含動畫集合的陣列。</span><span class="sxs-lookup"><span data-stu-id="5e654-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="5e654-119">這個方法會傳回具有指定名稱的動畫集。</span><span class="sxs-lookup"><span data-stu-id="5e654-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e654-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e654-120">Requirements</span></span>



| <span data-ttu-id="5e654-121">需求</span><span class="sxs-lookup"><span data-stu-id="5e654-121">Requirement</span></span> | <span data-ttu-id="5e654-122">值</span><span class="sxs-lookup"><span data-stu-id="5e654-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e654-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5e654-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5e654-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e654-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5e654-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e654-125">Library</span></span><br/> | <dl> <span data-ttu-id="5e654-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e654-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e654-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e654-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e654-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="5e654-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
