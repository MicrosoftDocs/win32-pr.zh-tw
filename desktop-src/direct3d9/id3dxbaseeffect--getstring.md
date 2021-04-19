---
description: 取得字串。
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'ID3DXBaseEffect：： GetString 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001485"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="354c6-103">ID3DXBaseEffect：： GetString 方法</span><span class="sxs-lookup"><span data-stu-id="354c6-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="354c6-104">取得字串。</span><span class="sxs-lookup"><span data-stu-id="354c6-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="354c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="354c6-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="354c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="354c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354c6-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="354c6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354c6-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="354c6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="354c6-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="354c6-109">Unique identifier.</span></span> <span data-ttu-id="354c6-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="354c6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="354c6-111">*ppString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="354c6-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="354c6-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="354c6-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="354c6-113">傳回 hParameter 所識別的字串。</span><span class="sxs-lookup"><span data-stu-id="354c6-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354c6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="354c6-114">Return value</span></span>

<span data-ttu-id="354c6-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="354c6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="354c6-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="354c6-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="354c6-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="354c6-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="354c6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="354c6-118">Requirements</span></span>



| <span data-ttu-id="354c6-119">需求</span><span class="sxs-lookup"><span data-stu-id="354c6-119">Requirement</span></span> | <span data-ttu-id="354c6-120">值</span><span class="sxs-lookup"><span data-stu-id="354c6-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="354c6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="354c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="354c6-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="354c6-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="354c6-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="354c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="354c6-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="354c6-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="354c6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="354c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354c6-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="354c6-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="354c6-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="354c6-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
