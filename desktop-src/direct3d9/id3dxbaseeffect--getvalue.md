---
description: 取得任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。 這個方法可以用來取代 ID3DXBaseEffect 中幾乎所有的 Getxxx 呼叫。
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect：： GetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992290"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="f47f1-104">ID3DXBaseEffect：： GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="f47f1-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="f47f1-105">取得任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。</span><span class="sxs-lookup"><span data-stu-id="f47f1-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="f47f1-106">這個方法可以用來取代 [**ID3DXBaseEffect**](id3dxbaseeffect.md)中幾乎所有的 Getxxx 呼叫。</span><span class="sxs-lookup"><span data-stu-id="f47f1-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f47f1-107">語法</span><span class="sxs-lookup"><span data-stu-id="f47f1-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="f47f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="f47f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47f1-109">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f47f1-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47f1-110">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f47f1-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f47f1-111">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f47f1-111">Unique identifier.</span></span> <span data-ttu-id="f47f1-112">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="f47f1-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47f1-113">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f47f1-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f47f1-114">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f47f1-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f47f1-115">傳回包含值的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f47f1-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="f47f1-116">*位元組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f47f1-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47f1-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f47f1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f47f1-118">\[緩衝區中的 \] 位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f47f1-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="f47f1-119">\_如果您知道您的緩衝區夠大而足以包含整個參數，且您想要略過大小驗證，則會傳入 D3DX 預設值。</span><span class="sxs-lookup"><span data-stu-id="f47f1-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47f1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f47f1-120">Return value</span></span>

<span data-ttu-id="f47f1-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f47f1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f47f1-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f47f1-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f47f1-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f47f1-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47f1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f47f1-124">Requirements</span></span>



| <span data-ttu-id="f47f1-125">需求</span><span class="sxs-lookup"><span data-stu-id="f47f1-125">Requirement</span></span> | <span data-ttu-id="f47f1-126">值</span><span class="sxs-lookup"><span data-stu-id="f47f1-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f47f1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f47f1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f47f1-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="f47f1-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f47f1-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="f47f1-129">Library</span></span><br/> | <dl> <span data-ttu-id="f47f1-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f47f1-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f47f1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f47f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47f1-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f47f1-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f47f1-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="f47f1-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
