---
description: ID3DXLoadUserData 介面-這個介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。
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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093626"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="d113d-103">ID3DXLoadUserData 介面</span><span class="sxs-lookup"><span data-stu-id="d113d-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="d113d-104">此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="d113d-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="d113d-105">這個介面的實例會傳遞至 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)，而 D3DX 會在每次遇到適當的資料時，在此介面上呼叫適當的方法。</span><span class="sxs-lookup"><span data-stu-id="d113d-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="d113d-106">例如，針對. x 檔案中的每個框架物件，會呼叫 [**ID3DXLoadUserData：： LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) ，並傳遞子資料。</span><span class="sxs-lookup"><span data-stu-id="d113d-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="d113d-107">成員</span><span class="sxs-lookup"><span data-stu-id="d113d-107">Members</span></span>

<span data-ttu-id="d113d-108">**ID3DXLoadUserData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d113d-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d113d-109">**ID3DXLoadUserData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d113d-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="d113d-110">方法</span><span class="sxs-lookup"><span data-stu-id="d113d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d113d-111">方法</span><span class="sxs-lookup"><span data-stu-id="d113d-111">Methods</span></span>

<span data-ttu-id="d113d-112">**ID3DXLoadUserData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d113d-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="d113d-113">方法</span><span class="sxs-lookup"><span data-stu-id="d113d-113">Method</span></span>                                                              | <span data-ttu-id="d113d-114">描述</span><span class="sxs-lookup"><span data-stu-id="d113d-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="d113d-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="d113d-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="d113d-116">從. x 檔案載入框架子資料。</span><span class="sxs-lookup"><span data-stu-id="d113d-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="d113d-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="d113d-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="d113d-118">從. x 檔案載入網格子資料。</span><span class="sxs-lookup"><span data-stu-id="d113d-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="d113d-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="d113d-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="d113d-120">從. x 檔案載入最上層資料。</span><span class="sxs-lookup"><span data-stu-id="d113d-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="d113d-121">備註</span><span class="sxs-lookup"><span data-stu-id="d113d-121">Remarks</span></span>

<span data-ttu-id="d113d-122">LPD3DXLOADUSERDATA 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d113d-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="d113d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d113d-123">Requirements</span></span>



| <span data-ttu-id="d113d-124">需求</span><span class="sxs-lookup"><span data-stu-id="d113d-124">Requirement</span></span> | <span data-ttu-id="d113d-125">值</span><span class="sxs-lookup"><span data-stu-id="d113d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d113d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d113d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d113d-127"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="d113d-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d113d-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d113d-128">Library</span></span><br/> | <dl> <span data-ttu-id="d113d-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d113d-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d113d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d113d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d113d-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="d113d-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
