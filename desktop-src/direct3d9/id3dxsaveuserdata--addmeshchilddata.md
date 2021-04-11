---
description: 將子資料新增至網格。
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'ID3DXSaveUserData：： AddMeshChildData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196429"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="3baa8-103">ID3DXSaveUserData：： AddMeshChildData 方法</span><span class="sxs-lookup"><span data-stu-id="3baa8-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="3baa8-104">將子資料新增至網格。</span><span class="sxs-lookup"><span data-stu-id="3baa8-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3baa8-105">語法</span><span class="sxs-lookup"><span data-stu-id="3baa8-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="3baa8-106">參數</span><span class="sxs-lookup"><span data-stu-id="3baa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3baa8-107">*pMeshContainer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3baa8-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3baa8-108">Type： **Const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="3baa8-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="3baa8-109">網格容器的指標。</span><span class="sxs-lookup"><span data-stu-id="3baa8-109">Pointer to a mesh container.</span></span> <span data-ttu-id="3baa8-110">請參閱 [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="3baa8-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="3baa8-111">*pXofSave* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3baa8-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3baa8-112">類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="3baa8-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="3baa8-113">. X 檔儲存物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3baa8-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="3baa8-114">使用指標來呼叫 [**ID3DXFileSaveObject：： AddDataObject**](id3dxfilesaveobject--adddataobject.md) ，以加入子資料物件。</span><span class="sxs-lookup"><span data-stu-id="3baa8-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="3baa8-115">請勿使用 [**ID3DXFileSaveObject：： save**](id3dxfilesaveobject--save.md)來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="3baa8-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="3baa8-116">*pXofMeshData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3baa8-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3baa8-117">類型： **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="3baa8-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="3baa8-118">. X 檔案資料節點的指標。</span><span class="sxs-lookup"><span data-stu-id="3baa8-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="3baa8-119">使用指標來呼叫 [**ID3DXFileSaveData：： AddDataObject**](id3dxfilesavedata--adddataobject.md) ，以加入子資料物件。</span><span class="sxs-lookup"><span data-stu-id="3baa8-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3baa8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3baa8-120">Return value</span></span>

<span data-ttu-id="3baa8-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3baa8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3baa8-122">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="3baa8-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="3baa8-123">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3baa8-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="3baa8-124">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3baa8-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3baa8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3baa8-125">Requirements</span></span>



| <span data-ttu-id="3baa8-126">需求</span><span class="sxs-lookup"><span data-stu-id="3baa8-126">Requirement</span></span> | <span data-ttu-id="3baa8-127">值</span><span class="sxs-lookup"><span data-stu-id="3baa8-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3baa8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3baa8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3baa8-129"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="3baa8-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3baa8-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="3baa8-130">Library</span></span><br/> | <dl> <span data-ttu-id="3baa8-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3baa8-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3baa8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3baa8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3baa8-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="3baa8-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
