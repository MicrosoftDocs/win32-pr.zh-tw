---
description: 取得傳遞描述。
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect：： GetPassDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989225"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="d7579-103">ID3DXBaseEffect：： GetPassDesc 方法</span><span class="sxs-lookup"><span data-stu-id="d7579-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="d7579-104">取得傳遞描述。</span><span class="sxs-lookup"><span data-stu-id="d7579-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7579-105">語法</span><span class="sxs-lookup"><span data-stu-id="d7579-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d7579-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7579-107">*hPass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7579-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7579-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d7579-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d7579-109">Pass 控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7579-109">Pass handle.</span></span> <span data-ttu-id="d7579-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="d7579-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7579-111">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d7579-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7579-112">類型： **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7579-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="d7579-113">傳回指定之傳遞的描述。</span><span class="sxs-lookup"><span data-stu-id="d7579-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="d7579-114">請參閱 [**D3DXPASS \_ DESC**](d3dxpass-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="d7579-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7579-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7579-115">Return value</span></span>

<span data-ttu-id="d7579-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7579-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7579-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d7579-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d7579-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d7579-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7579-119">備註</span><span class="sxs-lookup"><span data-stu-id="d7579-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7579-120">如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，這個方法將會傳回 **Null** 指標 (在 [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) 至著色器函式。</span><span class="sxs-lookup"><span data-stu-id="d7579-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7579-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7579-121">Requirements</span></span>



| <span data-ttu-id="d7579-122">需求</span><span class="sxs-lookup"><span data-stu-id="d7579-122">Requirement</span></span> | <span data-ttu-id="d7579-123">值</span><span class="sxs-lookup"><span data-stu-id="d7579-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7579-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d7579-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d7579-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7579-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d7579-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7579-126">Library</span></span><br/> | <dl> <span data-ttu-id="d7579-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7579-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d7579-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7579-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7579-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d7579-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




