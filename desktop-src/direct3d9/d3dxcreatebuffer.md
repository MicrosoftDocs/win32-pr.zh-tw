---
description: 建立緩衝區物件。
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: 'D3DXCreateBuffer 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999044"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="e33c0-103">D3DXCreateBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="e33c0-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="e33c0-104">建立緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="e33c0-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e33c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="e33c0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e33c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e33c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e33c0-107">*NumBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e33c0-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e33c0-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e33c0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e33c0-109">要建立的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e33c0-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e33c0-110">*ppBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e33c0-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e33c0-111">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e33c0-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e33c0-112">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，表示建立的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="e33c0-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e33c0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e33c0-113">Return value</span></span>

<span data-ttu-id="e33c0-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e33c0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e33c0-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e33c0-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e33c0-116">如果函式失敗，則傳回值可以是下列其中一項： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e33c0-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e33c0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e33c0-117">Requirements</span></span>



| <span data-ttu-id="e33c0-118">需求</span><span class="sxs-lookup"><span data-stu-id="e33c0-118">Requirement</span></span> | <span data-ttu-id="e33c0-119">值</span><span class="sxs-lookup"><span data-stu-id="e33c0-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e33c0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e33c0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e33c0-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e33c0-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e33c0-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="e33c0-122">Library</span></span><br/> | <dl> <span data-ttu-id="e33c0-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e33c0-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e33c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e33c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e33c0-125">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="e33c0-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
