---
description: 建立 ID3DXMATRIXStack 介面的實例。
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: 'D3DXCreateMatrixStack 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986122"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="fcc1b-103">D3DXCreateMatrixStack 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="fcc1b-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="fcc1b-104">建立 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc1b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fcc1b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="fcc1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fcc1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc1b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fcc1b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc1b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc1b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcc1b-109">未實作。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-109">Not implemented.</span></span> <span data-ttu-id="fcc1b-110">指定零。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="fcc1b-111">*ppStack* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fcc1b-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc1b-112">類型： **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="fcc1b-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="fcc1b-113">如果函式成功，則為以 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面指標填滿之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc1b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcc1b-114">Return value</span></span>

<span data-ttu-id="fcc1b-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcc1b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcc1b-116">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcc1b-117">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="fcc1b-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc1b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcc1b-118">Requirements</span></span>



| <span data-ttu-id="fcc1b-119">需求</span><span class="sxs-lookup"><span data-stu-id="fcc1b-119">Requirement</span></span> | <span data-ttu-id="fcc1b-120">值</span><span class="sxs-lookup"><span data-stu-id="fcc1b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc1b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fcc1b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fcc1b-122"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc1b-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fcc1b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fcc1b-123">Library</span></span><br/> | <dl> <span data-ttu-id="fcc1b-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcc1b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcc1b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcc1b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc1b-126">數學函數</span><span class="sxs-lookup"><span data-stu-id="fcc1b-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
