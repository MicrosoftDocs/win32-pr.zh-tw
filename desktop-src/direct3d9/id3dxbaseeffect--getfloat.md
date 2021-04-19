---
description: 取得浮點值。
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'ID3DXBaseEffect：： GetFloat 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982242"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="26dab-103">ID3DXBaseEffect：： GetFloat 方法</span><span class="sxs-lookup"><span data-stu-id="26dab-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="26dab-104">取得浮點值。</span><span class="sxs-lookup"><span data-stu-id="26dab-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="26dab-105">語法</span><span class="sxs-lookup"><span data-stu-id="26dab-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="26dab-106">參數</span><span class="sxs-lookup"><span data-stu-id="26dab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26dab-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26dab-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26dab-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="26dab-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="26dab-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="26dab-109">Unique identifier.</span></span> <span data-ttu-id="26dab-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="26dab-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="26dab-111">*pf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="26dab-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26dab-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="26dab-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="26dab-113">傳回浮點值。</span><span class="sxs-lookup"><span data-stu-id="26dab-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26dab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="26dab-114">Return value</span></span>

<span data-ttu-id="26dab-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26dab-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26dab-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="26dab-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="26dab-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="26dab-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="26dab-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="26dab-118">Requirements</span></span>



| <span data-ttu-id="26dab-119">需求</span><span class="sxs-lookup"><span data-stu-id="26dab-119">Requirement</span></span> | <span data-ttu-id="26dab-120">值</span><span class="sxs-lookup"><span data-stu-id="26dab-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26dab-121">標頭</span><span class="sxs-lookup"><span data-stu-id="26dab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="26dab-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="26dab-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="26dab-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="26dab-123">Library</span></span><br/> | <dl> <span data-ttu-id="26dab-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26dab-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="26dab-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26dab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26dab-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="26dab-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="26dab-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="26dab-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
