---
description: 在著色器中搜尋特定批註。 批註會以四個字元的程式碼識別， (FOURCC) 在批註的第一個 DWORD 中。
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: 'D3DXFindShaderComment 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982879"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="c01fb-104">D3DXFindShaderComment 函式</span><span class="sxs-lookup"><span data-stu-id="c01fb-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="c01fb-105">在著色器中搜尋特定批註。</span><span class="sxs-lookup"><span data-stu-id="c01fb-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="c01fb-106">批註會以四個字元的程式碼識別， (FOURCC) 在批註的第一個 DWORD 中。</span><span class="sxs-lookup"><span data-stu-id="c01fb-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="c01fb-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="c01fb-108">參數</span><span class="sxs-lookup"><span data-stu-id="c01fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c01fb-109">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c01fb-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c01fb-110">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c01fb-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c01fb-111">著色器函式 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="c01fb-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="c01fb-112">*FourCC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c01fb-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c01fb-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c01fb-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c01fb-114">FOURCC 識別批註區塊的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c01fb-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="c01fb-115">請參閱 [FourCC 格式](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="c01fb-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="c01fb-116">*ppData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c01fb-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c01fb-117">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c01fb-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c01fb-118">傳回批註資料的指標， (不包含註解標記和 FOURCC 程式碼) 。</span><span class="sxs-lookup"><span data-stu-id="c01fb-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="c01fb-119">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c01fb-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c01fb-120">*pSizeInBytes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c01fb-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c01fb-121">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c01fb-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c01fb-122">傳回批註資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c01fb-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="c01fb-123">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c01fb-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c01fb-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c01fb-124">Return value</span></span>

<span data-ttu-id="c01fb-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c01fb-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c01fb-126">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c01fb-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c01fb-127">如果找不到批註，且未發生其他錯誤， \_ 則會傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="c01fb-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01fb-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c01fb-128">Requirements</span></span>



| <span data-ttu-id="c01fb-129">需求</span><span class="sxs-lookup"><span data-stu-id="c01fb-129">Requirement</span></span> | <span data-ttu-id="c01fb-130">值</span><span class="sxs-lookup"><span data-stu-id="c01fb-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01fb-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c01fb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c01fb-132"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c01fb-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c01fb-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c01fb-133">Library</span></span><br/> | <dl> <span data-ttu-id="c01fb-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c01fb-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c01fb-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c01fb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01fb-136">著色器函式</span><span class="sxs-lookup"><span data-stu-id="c01fb-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
