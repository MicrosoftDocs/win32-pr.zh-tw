---
description: 要求配置網格容器物件。
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy：： CreateMeshContainer 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988164"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="4404e-103">ID3DXAllocateHierarchy：： CreateMeshContainer 方法</span><span class="sxs-lookup"><span data-stu-id="4404e-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="4404e-104">要求配置網格容器物件。</span><span class="sxs-lookup"><span data-stu-id="4404e-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4404e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4404e-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="4404e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4404e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4404e-107">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4404e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4404e-109">網格的名稱。</span><span class="sxs-lookup"><span data-stu-id="4404e-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4404e-110">*pMeshData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-111">Type： **Const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="4404e-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="4404e-112">網格資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4404e-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="4404e-113">請參閱 [**D3DXMESHDATA**](d3dxmeshdata.md)。</span><span class="sxs-lookup"><span data-stu-id="4404e-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4404e-114">*pMaterials* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-115">Type： **Const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="4404e-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="4404e-116">網格中所使用的材質陣列。</span><span class="sxs-lookup"><span data-stu-id="4404e-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4404e-117">*pEffectInstances* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-118">Type： **Const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="4404e-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="4404e-119">網格中使用的效果實例陣列。</span><span class="sxs-lookup"><span data-stu-id="4404e-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="4404e-120">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="4404e-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="4404e-121">*NumMaterials* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4404e-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4404e-123">材質陣列中的材質數目。</span><span class="sxs-lookup"><span data-stu-id="4404e-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="4404e-124">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-125">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4404e-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4404e-126">網格的相鄰陣列。</span><span class="sxs-lookup"><span data-stu-id="4404e-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4404e-127">*pSkinInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4404e-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-128">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="4404e-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="4404e-129">如果找到面板資料，則為外觀網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4404e-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="4404e-130">請參閱 [**ID3DXSkinInfo**](id3dxskininfo.md)。</span><span class="sxs-lookup"><span data-stu-id="4404e-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="4404e-131">*ppNewMeshContainer* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4404e-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4404e-132">類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4404e-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="4404e-133">傳回已建立的網狀容器。</span><span class="sxs-lookup"><span data-stu-id="4404e-133">Returns the created mesh container.</span></span> <span data-ttu-id="4404e-134">請參閱 [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="4404e-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4404e-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="4404e-135">Return value</span></span>

<span data-ttu-id="4404e-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4404e-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4404e-137">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="4404e-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4404e-138">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4404e-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4404e-139">否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4404e-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4404e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4404e-140">Requirements</span></span>



| <span data-ttu-id="4404e-141">需求</span><span class="sxs-lookup"><span data-stu-id="4404e-141">Requirement</span></span> | <span data-ttu-id="4404e-142">值</span><span class="sxs-lookup"><span data-stu-id="4404e-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4404e-143">標頭</span><span class="sxs-lookup"><span data-stu-id="4404e-143">Header</span></span><br/>  | <dl> <span data-ttu-id="4404e-144"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="4404e-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4404e-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="4404e-145">Library</span></span><br/> | <dl> <span data-ttu-id="4404e-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4404e-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4404e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4404e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4404e-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="4404e-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
