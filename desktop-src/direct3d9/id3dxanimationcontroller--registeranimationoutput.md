---
description: 將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController：： RegisterAnimationOutput 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986763"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="e7180-103">ID3DXAnimationController：： RegisterAnimationOutput 方法</span><span class="sxs-lookup"><span data-stu-id="e7180-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="e7180-104">將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。</span><span class="sxs-lookup"><span data-stu-id="e7180-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7180-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7180-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="e7180-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7180-107">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7180-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7180-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7180-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7180-109">動畫輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7180-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="e7180-110">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7180-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7180-111">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7180-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e7180-112">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，其中包含 SRT 轉換資料。</span><span class="sxs-lookup"><span data-stu-id="e7180-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="e7180-113">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e7180-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7180-114">*pScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7180-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7180-115">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7180-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7180-116">[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可描述動畫集合的尺規。</span><span class="sxs-lookup"><span data-stu-id="e7180-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="e7180-117">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e7180-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7180-118">*pRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7180-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7180-119">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7180-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e7180-120">[**D3DXQUATERNION**](d3dxquaternion.md)四元數的指標，該四元數描述動畫集合的旋轉。</span><span class="sxs-lookup"><span data-stu-id="e7180-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="e7180-121">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e7180-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7180-122">*pTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7180-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7180-123">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7180-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7180-124">描述動畫集合轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。</span><span class="sxs-lookup"><span data-stu-id="e7180-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="e7180-125">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e7180-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7180-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7180-126">Return value</span></span>

<span data-ttu-id="e7180-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7180-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7180-128">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e7180-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7180-129">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e7180-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7180-130">備註</span><span class="sxs-lookup"><span data-stu-id="e7180-130">Remarks</span></span>

<span data-ttu-id="e7180-131">如果動畫輸出已經註冊，pMatrix 就會填入輸入轉換資料。</span><span class="sxs-lookup"><span data-stu-id="e7180-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="e7180-132">使用 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 建立的動畫集合會自動註冊所有載入的動畫集合。</span><span class="sxs-lookup"><span data-stu-id="e7180-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7180-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7180-133">Requirements</span></span>



| <span data-ttu-id="e7180-134">需求</span><span class="sxs-lookup"><span data-stu-id="e7180-134">Requirement</span></span> | <span data-ttu-id="e7180-135">值</span><span class="sxs-lookup"><span data-stu-id="e7180-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7180-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e7180-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e7180-137"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7180-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e7180-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7180-138">Library</span></span><br/> | <dl> <span data-ttu-id="e7180-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7180-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7180-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7180-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7180-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e7180-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
