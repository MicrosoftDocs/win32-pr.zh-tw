---
description: 此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: 'ID3DXSaveUserData 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976701"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="6a1f0-103">ID3DXSaveUserData 介面</span><span class="sxs-lookup"><span data-stu-id="6a1f0-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="6a1f0-104">此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="6a1f0-105">這個介面的實例會傳遞至 [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)，而 D3DX 會在每次遇到適當的資料時，在此介面上呼叫適當的方法。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="6a1f0-106">例如，針對. x 檔案中的每個框架物件，會呼叫 [**ID3DXSaveUserData：： AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) ，並傳遞子資料。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="6a1f0-107">成員</span><span class="sxs-lookup"><span data-stu-id="6a1f0-107">Members</span></span>

<span data-ttu-id="6a1f0-108">**ID3DXSaveUserData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a1f0-109">**ID3DXSaveUserData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6a1f0-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="6a1f0-110">方法</span><span class="sxs-lookup"><span data-stu-id="6a1f0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a1f0-111">方法</span><span class="sxs-lookup"><span data-stu-id="6a1f0-111">Methods</span></span>

<span data-ttu-id="6a1f0-112">**ID3DXSaveUserData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="6a1f0-113">方法</span><span class="sxs-lookup"><span data-stu-id="6a1f0-113">Method</span></span>                                                                              | <span data-ttu-id="6a1f0-114">描述</span><span class="sxs-lookup"><span data-stu-id="6a1f0-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="6a1f0-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="6a1f0-116">將子資料新增至框架。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="6a1f0-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="6a1f0-118">將子資料新增至網格。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="6a1f0-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="6a1f0-120">在框架階層之後加入最上層物件。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="6a1f0-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="6a1f0-122">在框架階層之前加入最上層物件。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="6a1f0-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="6a1f0-124">用來註冊. x 檔案範本的使用者回呼。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="6a1f0-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="6a1f0-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="6a1f0-126">使用者用來儲存. x 檔案範本的回呼。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6a1f0-127">備註</span><span class="sxs-lookup"><span data-stu-id="6a1f0-127">Remarks</span></span>

<span data-ttu-id="6a1f0-128">LPD3DXSAVEUSERDATA 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6a1f0-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="6a1f0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a1f0-129">Requirements</span></span>



| <span data-ttu-id="6a1f0-130">需求</span><span class="sxs-lookup"><span data-stu-id="6a1f0-130">Requirement</span></span> | <span data-ttu-id="6a1f0-131">值</span><span class="sxs-lookup"><span data-stu-id="6a1f0-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1f0-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6a1f0-132">Header</span></span><br/>  | <dl> <span data-ttu-id="6a1f0-133"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a1f0-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6a1f0-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a1f0-134">Library</span></span><br/> | <dl> <span data-ttu-id="6a1f0-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a1f0-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a1f0-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a1f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1f0-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="6a1f0-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
