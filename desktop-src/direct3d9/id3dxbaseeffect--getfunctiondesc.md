---
description: 取得函數描述。
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect：： GetFunctionDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974896"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="291e9-103">ID3DXBaseEffect：： GetFunctionDesc 方法</span><span class="sxs-lookup"><span data-stu-id="291e9-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="291e9-104">取得函數描述。</span><span class="sxs-lookup"><span data-stu-id="291e9-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="291e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="291e9-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="291e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="291e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="291e9-107">*hFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="291e9-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="291e9-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="291e9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="291e9-109">函數控制碼。</span><span class="sxs-lookup"><span data-stu-id="291e9-109">Function handle.</span></span> <span data-ttu-id="291e9-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="291e9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="291e9-111">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="291e9-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="291e9-112">類型： **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="291e9-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="291e9-113">傳回函數的描述。</span><span class="sxs-lookup"><span data-stu-id="291e9-113">Returns a description of the function.</span></span> <span data-ttu-id="291e9-114">請參閱 [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="291e9-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="291e9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="291e9-115">Return value</span></span>

<span data-ttu-id="291e9-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="291e9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="291e9-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="291e9-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="291e9-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="291e9-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="291e9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="291e9-119">Requirements</span></span>



| <span data-ttu-id="291e9-120">需求</span><span class="sxs-lookup"><span data-stu-id="291e9-120">Requirement</span></span> | <span data-ttu-id="291e9-121">值</span><span class="sxs-lookup"><span data-stu-id="291e9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="291e9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="291e9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="291e9-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="291e9-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="291e9-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="291e9-124">Library</span></span><br/> | <dl> <span data-ttu-id="291e9-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="291e9-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="291e9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="291e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291e9-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="291e9-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




