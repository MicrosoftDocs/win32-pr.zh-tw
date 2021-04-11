---
description: 設定要傳遞至裝置的陣列範圍。
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'ID3DXBaseEffect：： SetArrayRange 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116169"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="16296-103">ID3DXBaseEffect：： SetArrayRange 方法</span><span class="sxs-lookup"><span data-stu-id="16296-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="16296-104">設定要傳遞至裝置的陣列範圍。</span><span class="sxs-lookup"><span data-stu-id="16296-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="16296-105">語法</span><span class="sxs-lookup"><span data-stu-id="16296-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="16296-106">參數</span><span class="sxs-lookup"><span data-stu-id="16296-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16296-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16296-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16296-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="16296-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="16296-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="16296-109">Unique identifier.</span></span> <span data-ttu-id="16296-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="16296-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="16296-111">*開始* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16296-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16296-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16296-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16296-113">開始索引。</span><span class="sxs-lookup"><span data-stu-id="16296-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="16296-114">*停止* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16296-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16296-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16296-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16296-116">停止索引。</span><span class="sxs-lookup"><span data-stu-id="16296-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16296-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="16296-117">Return value</span></span>

<span data-ttu-id="16296-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16296-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16296-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="16296-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16296-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="16296-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="16296-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="16296-121">Requirements</span></span>



| <span data-ttu-id="16296-122">需求</span><span class="sxs-lookup"><span data-stu-id="16296-122">Requirement</span></span> | <span data-ttu-id="16296-123">值</span><span class="sxs-lookup"><span data-stu-id="16296-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16296-124">標頭</span><span class="sxs-lookup"><span data-stu-id="16296-124">Header</span></span><br/>  | <dl> <span data-ttu-id="16296-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="16296-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16296-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="16296-126">Library</span></span><br/> | <dl> <span data-ttu-id="16296-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16296-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16296-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16296-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16296-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="16296-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
