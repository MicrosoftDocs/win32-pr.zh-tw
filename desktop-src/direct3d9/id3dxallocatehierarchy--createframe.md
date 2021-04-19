---
description: 要求組態架構物件。
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'ID3DXAllocateHierarchy：： CreateFrame 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976509"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="21412-103">ID3DXAllocateHierarchy：： CreateFrame 方法</span><span class="sxs-lookup"><span data-stu-id="21412-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="21412-104">要求組態架構物件。</span><span class="sxs-lookup"><span data-stu-id="21412-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="21412-105">語法</span><span class="sxs-lookup"><span data-stu-id="21412-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="21412-106">參數</span><span class="sxs-lookup"><span data-stu-id="21412-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21412-107">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21412-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21412-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21412-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21412-109">要建立的框架名稱。</span><span class="sxs-lookup"><span data-stu-id="21412-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="21412-110">*ppNewFrame* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="21412-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="21412-111">類型： **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="21412-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="21412-112">傳回建立的框架物件。</span><span class="sxs-lookup"><span data-stu-id="21412-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21412-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="21412-113">Return value</span></span>

<span data-ttu-id="21412-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21412-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21412-115">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="21412-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="21412-116">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="21412-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="21412-117">否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="21412-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="21412-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="21412-118">Requirements</span></span>



| <span data-ttu-id="21412-119">需求</span><span class="sxs-lookup"><span data-stu-id="21412-119">Requirement</span></span> | <span data-ttu-id="21412-120">值</span><span class="sxs-lookup"><span data-stu-id="21412-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21412-121">標頭</span><span class="sxs-lookup"><span data-stu-id="21412-121">Header</span></span><br/>  | <dl> <span data-ttu-id="21412-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="21412-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="21412-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="21412-123">Library</span></span><br/> | <dl> <span data-ttu-id="21412-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21412-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21412-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21412-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21412-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="21412-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
