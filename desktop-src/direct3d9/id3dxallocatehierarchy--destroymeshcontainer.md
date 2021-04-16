---
description: 要求解除配置網格容器物件。
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: 'ID3DXAllocateHierarchy：:D estroyMeshContainer 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514705"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="8efeb-103">ID3DXAllocateHierarchy：:D estroyMeshContainer 方法</span><span class="sxs-lookup"><span data-stu-id="8efeb-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="8efeb-104">要求解除配置網格容器物件。</span><span class="sxs-lookup"><span data-stu-id="8efeb-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efeb-105">語法</span><span class="sxs-lookup"><span data-stu-id="8efeb-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="8efeb-106">參數</span><span class="sxs-lookup"><span data-stu-id="8efeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efeb-107">*pMeshContainerToFree* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8efeb-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efeb-108">類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="8efeb-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="8efeb-109">要解除配置之網狀容器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8efeb-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efeb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8efeb-110">Return value</span></span>

<span data-ttu-id="8efeb-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8efeb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8efeb-112">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="8efeb-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="8efeb-113">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8efeb-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="8efeb-114">否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8efeb-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efeb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8efeb-115">Requirements</span></span>



| <span data-ttu-id="8efeb-116">需求</span><span class="sxs-lookup"><span data-stu-id="8efeb-116">Requirement</span></span> | <span data-ttu-id="8efeb-117">值</span><span class="sxs-lookup"><span data-stu-id="8efeb-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8efeb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8efeb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8efeb-119"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="8efeb-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8efeb-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8efeb-120">Library</span></span><br/> | <dl> <span data-ttu-id="8efeb-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8efeb-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8efeb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8efeb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efeb-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="8efeb-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




