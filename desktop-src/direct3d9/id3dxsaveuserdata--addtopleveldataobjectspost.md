---
description: 在框架階層之後加入最上層物件。
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'ID3DXSaveUserData：： AddTopLevelDataObjectsPost 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035426"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a><span data-ttu-id="01a45-103">ID3DXSaveUserData：： AddTopLevelDataObjectsPost 方法</span><span class="sxs-lookup"><span data-stu-id="01a45-103">ID3DXSaveUserData::AddTopLevelDataObjectsPost method</span></span>

<span data-ttu-id="01a45-104">在框架階層之後加入最上層物件。</span><span class="sxs-lookup"><span data-stu-id="01a45-104">Add a top level object after the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a45-105">語法</span><span class="sxs-lookup"><span data-stu-id="01a45-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="01a45-106">參數</span><span class="sxs-lookup"><span data-stu-id="01a45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a45-107">*pXofSave* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a45-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a45-108">類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="01a45-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="01a45-109">. X 檔儲存物件的指標。</span><span class="sxs-lookup"><span data-stu-id="01a45-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="01a45-110">使用這個指標來呼叫 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) ，以建立要儲存的資料物件。</span><span class="sxs-lookup"><span data-stu-id="01a45-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="01a45-111">然後呼叫 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md) 來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="01a45-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a45-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="01a45-112">Return value</span></span>

<span data-ttu-id="01a45-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01a45-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01a45-114">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="01a45-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="01a45-115">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="01a45-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="01a45-116">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="01a45-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a45-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="01a45-117">Requirements</span></span>



| <span data-ttu-id="01a45-118">需求</span><span class="sxs-lookup"><span data-stu-id="01a45-118">Requirement</span></span> | <span data-ttu-id="01a45-119">值</span><span class="sxs-lookup"><span data-stu-id="01a45-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a45-120">標頭</span><span class="sxs-lookup"><span data-stu-id="01a45-120">Header</span></span><br/>  | <dl> <span data-ttu-id="01a45-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="01a45-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="01a45-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="01a45-122">Library</span></span><br/> | <dl> <span data-ttu-id="01a45-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="01a45-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01a45-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01a45-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a45-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="01a45-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
