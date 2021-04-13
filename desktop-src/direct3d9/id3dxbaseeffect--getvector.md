---
description: 取得向量。
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'ID3DXBaseEffect：： GetVector 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322628"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="f85ef-103">ID3DXBaseEffect：： GetVector 方法</span><span class="sxs-lookup"><span data-stu-id="f85ef-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="f85ef-104">取得向量。</span><span class="sxs-lookup"><span data-stu-id="f85ef-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f85ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="f85ef-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="f85ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="f85ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f85ef-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f85ef-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f85ef-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f85ef-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f85ef-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f85ef-109">Unique identifier.</span></span> <span data-ttu-id="f85ef-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="f85ef-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f85ef-111">*pVector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f85ef-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f85ef-112">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f85ef-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f85ef-113">傳回4D 向量。</span><span class="sxs-lookup"><span data-stu-id="f85ef-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f85ef-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f85ef-114">Return value</span></span>

<span data-ttu-id="f85ef-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f85ef-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f85ef-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f85ef-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f85ef-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f85ef-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f85ef-118">備註</span><span class="sxs-lookup"><span data-stu-id="f85ef-118">Remarks</span></span>

<span data-ttu-id="f85ef-119">如果目的地向量大於來源向量，則只會填入目的地向量的初始元件，其餘元件則會設定為零。</span><span class="sxs-lookup"><span data-stu-id="f85ef-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f85ef-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f85ef-120">Requirements</span></span>



| <span data-ttu-id="f85ef-121">需求</span><span class="sxs-lookup"><span data-stu-id="f85ef-121">Requirement</span></span> | <span data-ttu-id="f85ef-122">值</span><span class="sxs-lookup"><span data-stu-id="f85ef-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85ef-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f85ef-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f85ef-124"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="f85ef-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f85ef-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="f85ef-125">Library</span></span><br/> | <dl> <span data-ttu-id="f85ef-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f85ef-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f85ef-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f85ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85ef-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f85ef-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f85ef-129">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="f85ef-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




