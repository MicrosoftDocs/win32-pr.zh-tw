---
description: 此介面是由應用程式所執行，以配置或釋放框架和網狀架構的容器物件。 在載入和終結框架階層時，會呼叫此上的方法。
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: 'ID3DXAllocateHierarchy 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035422"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="a86a1-104">ID3DXAllocateHierarchy 介面</span><span class="sxs-lookup"><span data-stu-id="a86a1-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="a86a1-105">此介面是由應用程式所執行，以配置或釋放框架和網狀架構的容器物件。</span><span class="sxs-lookup"><span data-stu-id="a86a1-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="a86a1-106">在載入和終結框架階層時，會呼叫此上的方法。</span><span class="sxs-lookup"><span data-stu-id="a86a1-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="a86a1-107">成員</span><span class="sxs-lookup"><span data-stu-id="a86a1-107">Members</span></span>

<span data-ttu-id="a86a1-108">**ID3DXAllocateHierarchy** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a86a1-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a86a1-109">**ID3DXAllocateHierarchy** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a86a1-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="a86a1-110">方法</span><span class="sxs-lookup"><span data-stu-id="a86a1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a86a1-111">方法</span><span class="sxs-lookup"><span data-stu-id="a86a1-111">Methods</span></span>

<span data-ttu-id="a86a1-112">**ID3DXAllocateHierarchy** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a86a1-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="a86a1-113">方法</span><span class="sxs-lookup"><span data-stu-id="a86a1-113">Method</span></span>                                                                       | <span data-ttu-id="a86a1-114">描述</span><span class="sxs-lookup"><span data-stu-id="a86a1-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="a86a1-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="a86a1-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="a86a1-116">要求組態架構物件。</span><span class="sxs-lookup"><span data-stu-id="a86a1-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="a86a1-117">**CreateMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="a86a1-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="a86a1-118">要求配置網格容器物件。</span><span class="sxs-lookup"><span data-stu-id="a86a1-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="a86a1-119">**DestroyFrame**</span><span class="sxs-lookup"><span data-stu-id="a86a1-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="a86a1-120">要求解除配置框架物件。</span><span class="sxs-lookup"><span data-stu-id="a86a1-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="a86a1-121">**DestroyMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="a86a1-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="a86a1-122">要求解除配置網格容器物件。</span><span class="sxs-lookup"><span data-stu-id="a86a1-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a86a1-123">備註</span><span class="sxs-lookup"><span data-stu-id="a86a1-123">Remarks</span></span>

<span data-ttu-id="a86a1-124">LPD3DXALLOCATEHIERARCHY 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a86a1-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="a86a1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a86a1-125">Requirements</span></span>



| <span data-ttu-id="a86a1-126">需求</span><span class="sxs-lookup"><span data-stu-id="a86a1-126">Requirement</span></span> | <span data-ttu-id="a86a1-127">值</span><span class="sxs-lookup"><span data-stu-id="a86a1-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a86a1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a86a1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a86a1-129"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a86a1-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a86a1-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="a86a1-130">Library</span></span><br/> | <dl> <span data-ttu-id="a86a1-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a86a1-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a86a1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a86a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86a1-133">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a86a1-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
