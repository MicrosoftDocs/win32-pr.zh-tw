---
description: 取得參數或注釋描述。
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect：： GetParameterDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997426"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="33f0f-103">ID3DXBaseEffect：： GetParameterDesc 方法</span><span class="sxs-lookup"><span data-stu-id="33f0f-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="33f0f-104">取得參數或注釋描述。</span><span class="sxs-lookup"><span data-stu-id="33f0f-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="33f0f-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="33f0f-106">參數</span><span class="sxs-lookup"><span data-stu-id="33f0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f0f-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33f0f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33f0f-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="33f0f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="33f0f-109">參數或注釋控制碼。</span><span class="sxs-lookup"><span data-stu-id="33f0f-109">Parameter or annotation handle.</span></span> <span data-ttu-id="33f0f-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="33f0f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="33f0f-111">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33f0f-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33f0f-112">類型： **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="33f0f-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="33f0f-113">傳回指定之參數或注釋的描述。</span><span class="sxs-lookup"><span data-stu-id="33f0f-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="33f0f-114">請參閱 [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="33f0f-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f0f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="33f0f-115">Return value</span></span>

<span data-ttu-id="33f0f-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33f0f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33f0f-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="33f0f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="33f0f-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="33f0f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f0f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="33f0f-119">Requirements</span></span>



| <span data-ttu-id="33f0f-120">需求</span><span class="sxs-lookup"><span data-stu-id="33f0f-120">Requirement</span></span> | <span data-ttu-id="33f0f-121">值</span><span class="sxs-lookup"><span data-stu-id="33f0f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f0f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="33f0f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="33f0f-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="33f0f-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="33f0f-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="33f0f-124">Library</span></span><br/> | <dl> <span data-ttu-id="33f0f-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="33f0f-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33f0f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f0f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f0f-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="33f0f-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




