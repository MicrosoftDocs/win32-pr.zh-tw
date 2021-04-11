---
description: 設定任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect：： SetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116253"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="ac2a0-103">ID3DXBaseEffect：： SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="ac2a0-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="ac2a0-104">設定任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac2a0-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="ac2a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac2a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac2a0-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac2a0-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac2a0-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ac2a0-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-109">Unique identifier.</span></span> <span data-ttu-id="ac2a0-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac2a0-111">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac2a0-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac2a0-112">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac2a0-113">包含資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="ac2a0-114">*位元組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac2a0-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac2a0-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac2a0-116">\[緩衝區中的 \] 位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="ac2a0-117">\_如果您知道您的緩衝區夠大而足以包含整個參數，且您想要略過大小驗證，則會傳入 D3DX 預設值。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac2a0-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac2a0-118">Return value</span></span>

<span data-ttu-id="ac2a0-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac2a0-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac2a0-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2a0-122">備註</span><span class="sxs-lookup"><span data-stu-id="ac2a0-122">Remarks</span></span>

<span data-ttu-id="ac2a0-123">這個方法可以用來取代幾乎所有的效果集 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ac2a0-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2a0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac2a0-124">Requirements</span></span>



| <span data-ttu-id="ac2a0-125">需求</span><span class="sxs-lookup"><span data-stu-id="ac2a0-125">Requirement</span></span> | <span data-ttu-id="ac2a0-126">值</span><span class="sxs-lookup"><span data-stu-id="ac2a0-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2a0-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ac2a0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ac2a0-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac2a0-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ac2a0-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac2a0-129">Library</span></span><br/> | <dl> <span data-ttu-id="ac2a0-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac2a0-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ac2a0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac2a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2a0-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ac2a0-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ac2a0-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
