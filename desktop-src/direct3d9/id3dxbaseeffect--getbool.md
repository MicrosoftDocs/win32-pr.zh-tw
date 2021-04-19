---
description: 取得 BOOL 值。
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect：： GetBool 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993914"
---
# <a name="id3dxbaseeffectgetbool-method"></a><span data-ttu-id="975ad-103">ID3DXBaseEffect：： GetBool 方法</span><span class="sxs-lookup"><span data-stu-id="975ad-103">ID3DXBaseEffect::GetBool method</span></span>

<span data-ttu-id="975ad-104">取得 BOOL 值。</span><span class="sxs-lookup"><span data-stu-id="975ad-104">Gets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="975ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="975ad-105">Syntax</span></span>


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a><span data-ttu-id="975ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="975ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="975ad-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="975ad-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="975ad-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="975ad-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="975ad-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="975ad-109">Unique identifier.</span></span> <span data-ttu-id="975ad-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="975ad-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="975ad-111">*pb* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="975ad-111">*pb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="975ad-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="975ad-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="975ad-113">傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="975ad-113">Returns a Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="975ad-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="975ad-114">Return value</span></span>

<span data-ttu-id="975ad-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="975ad-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="975ad-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="975ad-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="975ad-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="975ad-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="975ad-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="975ad-118">Requirements</span></span>



| <span data-ttu-id="975ad-119">需求</span><span class="sxs-lookup"><span data-stu-id="975ad-119">Requirement</span></span> | <span data-ttu-id="975ad-120">值</span><span class="sxs-lookup"><span data-stu-id="975ad-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="975ad-121">標頭</span><span class="sxs-lookup"><span data-stu-id="975ad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="975ad-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="975ad-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="975ad-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="975ad-123">Library</span></span><br/> | <dl> <span data-ttu-id="975ad-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="975ad-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="975ad-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="975ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975ad-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="975ad-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="975ad-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="975ad-127">**SetBool**</span></span>](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
