---
description: 使用者執行的方法，用於關閉著色器的 \# 包含檔案。
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude：： Close 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974894"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="e2bf6-103">ID3DXInclude：： Close 方法</span><span class="sxs-lookup"><span data-stu-id="e2bf6-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="e2bf6-104">使用者執行的方法，用於關閉著色器的 \# 包含檔案。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2bf6-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2bf6-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="e2bf6-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2bf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2bf6-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2bf6-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2bf6-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2bf6-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2bf6-109">傳回之緩衝區的指標，其中包含 include 指示詞。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="e2bf6-110">這是對應的 [**ID3DXInclude：： Open**](id3dxinclude--open.md) 呼叫所傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2bf6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2bf6-111">Return value</span></span>

<span data-ttu-id="e2bf6-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2bf6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2bf6-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e2bf6-114">如果回呼在讀取 include 檔案時失敗 \# ，則造成呼叫回呼的 API 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="e2bf6-115">這是下列項目之一：</span><span class="sxs-lookup"><span data-stu-id="e2bf6-115">This is one of the following:</span></span>

-   <span data-ttu-id="e2bf6-116">HLSL 著色器將會失敗其中一個 D3DXCompileShader \* \* \* 函數。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e2bf6-117">元件著色器將會使其中一個 D3DXAssembleShader 函式失敗 \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e2bf6-118">此效果將會使其中一個 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數失敗。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2bf6-119">備註</span><span class="sxs-lookup"><span data-stu-id="e2bf6-119">Remarks</span></span>

<span data-ttu-id="e2bf6-120">如果 [**ID3DXInclude：： Open**](id3dxinclude--open.md) 成功，就保證會在使用此介面的 API 傳回之前呼叫 **ID3DXInclude：： Close** 。</span><span class="sxs-lookup"><span data-stu-id="e2bf6-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2bf6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2bf6-121">Requirements</span></span>



| <span data-ttu-id="e2bf6-122">需求</span><span class="sxs-lookup"><span data-stu-id="e2bf6-122">Requirement</span></span> | <span data-ttu-id="e2bf6-123">值</span><span class="sxs-lookup"><span data-stu-id="e2bf6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bf6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e2bf6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e2bf6-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2bf6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e2bf6-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2bf6-126">Library</span></span><br/> | <dl> <span data-ttu-id="e2bf6-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2bf6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2bf6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2bf6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bf6-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="e2bf6-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="e2bf6-130">**ID3DXInclude：： Open**</span><span class="sxs-lookup"><span data-stu-id="e2bf6-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
