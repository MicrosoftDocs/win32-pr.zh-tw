---
description: 建立矩陣堆疊。
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: 'D3DXCreateMatrixStack 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386497"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="3bad0-103">D3DXCreateMatrixStack 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="3bad0-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="3bad0-104">建立矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="3bad0-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bad0-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bad0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="3bad0-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bad0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bad0-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3bad0-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bad0-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bad0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bad0-109">未實作。</span><span class="sxs-lookup"><span data-stu-id="3bad0-109">Not implemented.</span></span> <span data-ttu-id="3bad0-110">指定零。</span><span class="sxs-lookup"><span data-stu-id="3bad0-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="3bad0-111">*ppStack* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3bad0-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bad0-112">類型： **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="3bad0-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="3bad0-113">矩陣堆疊指標的位址 (查看 [**ID3DXMatrixStack 介面**](d3d10-id3dxmatrixstack.md)) 。</span><span class="sxs-lookup"><span data-stu-id="3bad0-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bad0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bad0-114">Return value</span></span>

<span data-ttu-id="3bad0-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bad0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bad0-116">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3bad0-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bad0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bad0-117">Requirements</span></span>



| <span data-ttu-id="3bad0-118">需求</span><span class="sxs-lookup"><span data-stu-id="3bad0-118">Requirement</span></span> | <span data-ttu-id="3bad0-119">值</span><span class="sxs-lookup"><span data-stu-id="3bad0-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bad0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3bad0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3bad0-121"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bad0-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3bad0-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="3bad0-122">Library</span></span><br/> | <dl> <span data-ttu-id="3bad0-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bad0-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bad0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bad0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bad0-125">數學函數</span><span class="sxs-lookup"><span data-stu-id="3bad0-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
