---
description: 將子資料新增至框架。
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData：： AddFrameChildData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196430"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="7663b-103">ID3DXSaveUserData：： AddFrameChildData 方法</span><span class="sxs-lookup"><span data-stu-id="7663b-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="7663b-104">將子資料新增至框架。</span><span class="sxs-lookup"><span data-stu-id="7663b-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7663b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7663b-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="7663b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7663b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7663b-107">*pFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7663b-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7663b-108">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="7663b-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="7663b-109">網格容器的指標。</span><span class="sxs-lookup"><span data-stu-id="7663b-109">Pointer to a mesh container.</span></span> <span data-ttu-id="7663b-110">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="7663b-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="7663b-111">*pXofSave* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7663b-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7663b-112">類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="7663b-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="7663b-113">. X 檔儲存物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7663b-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="7663b-114">使用指標來呼叫 [**ID3DXFileSaveObject：： AddDataObject**](id3dxfilesaveobject--adddataobject.md) ，以加入子資料物件。</span><span class="sxs-lookup"><span data-stu-id="7663b-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="7663b-115">請勿使用 [**ID3DXFileSaveObject：： save**](id3dxfilesaveobject--save.md)來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="7663b-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="7663b-116">*pXofFrameData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7663b-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7663b-117">類型： **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="7663b-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="7663b-118">. X 檔案資料節點的指標。</span><span class="sxs-lookup"><span data-stu-id="7663b-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="7663b-119">使用指標來呼叫 [**ID3DXFileSaveData：： AddDataObject**](id3dxfilesavedata--adddataobject.md) ，以加入子資料物件。</span><span class="sxs-lookup"><span data-stu-id="7663b-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7663b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="7663b-120">Return value</span></span>

<span data-ttu-id="7663b-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7663b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7663b-122">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="7663b-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7663b-123">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7663b-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7663b-124">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7663b-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7663b-125">備註</span><span class="sxs-lookup"><span data-stu-id="7663b-125">Remarks</span></span>

<span data-ttu-id="7663b-126">[**ID3DXSaveUserData：： RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) 和 [**ID3DXSaveUserData：： SaveTemplates**](id3dxsaveuserdata--savetemplates.md) 提供一種機制，可將範本加入至用來儲存使用者資料的. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="7663b-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7663b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7663b-127">Requirements</span></span>



| <span data-ttu-id="7663b-128">需求</span><span class="sxs-lookup"><span data-stu-id="7663b-128">Requirement</span></span> | <span data-ttu-id="7663b-129">值</span><span class="sxs-lookup"><span data-stu-id="7663b-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7663b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7663b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7663b-131"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="7663b-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7663b-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="7663b-132">Library</span></span><br/> | <dl> <span data-ttu-id="7663b-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7663b-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7663b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7663b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7663b-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="7663b-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
