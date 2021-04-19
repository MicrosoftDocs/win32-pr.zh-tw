---
description: 此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: 'ID3DXLoadUserData 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999969"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="681bc-103">ID3DXLoadUserData 介面</span><span class="sxs-lookup"><span data-stu-id="681bc-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="681bc-104">此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="681bc-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="681bc-105">這個介面的實例會傳遞至 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)，而 D3DX 會在每次遇到適當的資料時，在此介面上呼叫適當的方法。</span><span class="sxs-lookup"><span data-stu-id="681bc-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="681bc-106">例如，針對. x 檔案中的每個框架物件，會呼叫 [**ID3DXLoadUserData：： LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) ，並傳遞子資料。</span><span class="sxs-lookup"><span data-stu-id="681bc-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="681bc-107">成員</span><span class="sxs-lookup"><span data-stu-id="681bc-107">Members</span></span>

<span data-ttu-id="681bc-108">**ID3DXLoadUserData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="681bc-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="681bc-109">**ID3DXLoadUserData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="681bc-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="681bc-110">方法</span><span class="sxs-lookup"><span data-stu-id="681bc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="681bc-111">方法</span><span class="sxs-lookup"><span data-stu-id="681bc-111">Methods</span></span>

<span data-ttu-id="681bc-112">**ID3DXLoadUserData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="681bc-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="681bc-113">方法</span><span class="sxs-lookup"><span data-stu-id="681bc-113">Method</span></span>                                                              | <span data-ttu-id="681bc-114">描述</span><span class="sxs-lookup"><span data-stu-id="681bc-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="681bc-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="681bc-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="681bc-116">從. x 檔案載入框架子資料。</span><span class="sxs-lookup"><span data-stu-id="681bc-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="681bc-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="681bc-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="681bc-118">從. x 檔案載入網格子資料。</span><span class="sxs-lookup"><span data-stu-id="681bc-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="681bc-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="681bc-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="681bc-120">從. x 檔案載入最上層資料。</span><span class="sxs-lookup"><span data-stu-id="681bc-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="681bc-121">備註</span><span class="sxs-lookup"><span data-stu-id="681bc-121">Remarks</span></span>

<span data-ttu-id="681bc-122">LPD3DXLOADUSERDATA 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="681bc-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="681bc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="681bc-123">Requirements</span></span>



| <span data-ttu-id="681bc-124">需求</span><span class="sxs-lookup"><span data-stu-id="681bc-124">Requirement</span></span> | <span data-ttu-id="681bc-125">值</span><span class="sxs-lookup"><span data-stu-id="681bc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="681bc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="681bc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="681bc-127"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="681bc-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="681bc-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="681bc-128">Library</span></span><br/> | <dl> <span data-ttu-id="681bc-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="681bc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="681bc-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="681bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681bc-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="681bc-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
