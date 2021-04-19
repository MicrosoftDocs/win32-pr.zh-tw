---
description: 使用緩衝區中的資料來設定常數資料表。
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader：： SetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981820"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="1de06-103">ID3DXTextureShader：： SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="1de06-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="1de06-104">使用緩衝區中的資料來設定常數資料表。</span><span class="sxs-lookup"><span data-stu-id="1de06-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de06-105">語法</span><span class="sxs-lookup"><span data-stu-id="1de06-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="1de06-106">參數</span><span class="sxs-lookup"><span data-stu-id="1de06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de06-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1de06-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1de06-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1de06-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1de06-109">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de06-109">Unique identifier to a constant.</span></span> <span data-ttu-id="1de06-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="1de06-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="1de06-111">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1de06-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1de06-112">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1de06-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1de06-113">包含常數資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="1de06-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="1de06-114">*位元組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1de06-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1de06-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1de06-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1de06-116">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1de06-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de06-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1de06-117">Return value</span></span>

<span data-ttu-id="1de06-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1de06-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1de06-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1de06-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1de06-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1de06-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de06-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1de06-121">Requirements</span></span>



| <span data-ttu-id="1de06-122">需求</span><span class="sxs-lookup"><span data-stu-id="1de06-122">Requirement</span></span> | <span data-ttu-id="1de06-123">值</span><span class="sxs-lookup"><span data-stu-id="1de06-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de06-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1de06-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1de06-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="1de06-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1de06-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1de06-126">Library</span></span><br/> | <dl> <span data-ttu-id="1de06-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1de06-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1de06-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1de06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de06-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="1de06-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
