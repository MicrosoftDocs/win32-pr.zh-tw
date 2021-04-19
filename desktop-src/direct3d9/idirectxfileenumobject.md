---
description: 應用程式會使用 IDirectXFileEnumObject 介面的方法來迴圈處理檔案中的資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得資料物件。 已取代。
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: 'IDirectXFileEnumObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989193"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="5c8e0-104">IDirectXFileEnumObject 介面</span><span class="sxs-lookup"><span data-stu-id="5c8e0-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="5c8e0-105">應用程式會使用 IDirectXFileEnumObject 介面的方法來迴圈處理檔案中的資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得資料物件。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="5c8e0-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="5c8e0-107">成員</span><span class="sxs-lookup"><span data-stu-id="5c8e0-107">Members</span></span>

<span data-ttu-id="5c8e0-108">**IDirectXFileEnumObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5c8e0-109">**IDirectXFileEnumObject** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c8e0-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="5c8e0-110">方法</span><span class="sxs-lookup"><span data-stu-id="5c8e0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c8e0-111">方法</span><span class="sxs-lookup"><span data-stu-id="5c8e0-111">Methods</span></span>

<span data-ttu-id="5c8e0-112">**IDirectXFileEnumObject** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="5c8e0-113">方法</span><span class="sxs-lookup"><span data-stu-id="5c8e0-113">Method</span></span>                                                                     | <span data-ttu-id="5c8e0-114">描述</span><span class="sxs-lookup"><span data-stu-id="5c8e0-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="5c8e0-115">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="5c8e0-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="5c8e0-116">抓取具有指定之 GUID 的資料物件。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="5c8e0-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="5c8e0-118">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="5c8e0-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="5c8e0-119">抓取具有指定名稱的資料物件。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="5c8e0-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="5c8e0-121">**GetNextDataObject**</span><span class="sxs-lookup"><span data-stu-id="5c8e0-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="5c8e0-122">抓取 DirectX 檔案中的下一個最上層物件。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="5c8e0-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c8e0-124">備註</span><span class="sxs-lookup"><span data-stu-id="5c8e0-124">Remarks</span></span>

<span data-ttu-id="5c8e0-125">IDirectXFileEnumObject 介面的 GUID 是 IID \_ IDirectXFileEnumObject。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="5c8e0-126">LPDIRECTXFILEENUMOBJECT 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5c8e0-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="5c8e0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c8e0-127">Requirements</span></span>



| <span data-ttu-id="5c8e0-128">需求</span><span class="sxs-lookup"><span data-stu-id="5c8e0-128">Requirement</span></span> | <span data-ttu-id="5c8e0-129">值</span><span class="sxs-lookup"><span data-stu-id="5c8e0-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8e0-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5c8e0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5c8e0-131"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8e0-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c8e0-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c8e0-132">Library</span></span><br/> | <dl> <span data-ttu-id="5c8e0-133"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c8e0-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8e0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c8e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8e0-135">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="5c8e0-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
