---
description: 應用程式會使用 IDirectXFileDataReference 介面的方法來支援資料參考物件。
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: 'IDirectXFileDataReference 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116309"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="3d8e3-103">IDirectXFileDataReference 介面</span><span class="sxs-lookup"><span data-stu-id="3d8e3-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="3d8e3-104">應用程式會使用 IDirectXFileDataReference 介面的方法來支援資料參考物件。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="3d8e3-105">資料參考物件會參考先前在檔案中定義的資料物件。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="3d8e3-106">這可讓您多次使用相同的物件，而不需要在檔案中重複。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="3d8e3-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="3d8e3-108">成員</span><span class="sxs-lookup"><span data-stu-id="3d8e3-108">Members</span></span>

<span data-ttu-id="3d8e3-109">**IDirectXFileDataReference** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="3d8e3-110">**IDirectXFileDataReference** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d8e3-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="3d8e3-111">方法</span><span class="sxs-lookup"><span data-stu-id="3d8e3-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3d8e3-112">方法</span><span class="sxs-lookup"><span data-stu-id="3d8e3-112">Methods</span></span>

<span data-ttu-id="3d8e3-113">**IDirectXFileDataReference** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="3d8e3-114">方法</span><span class="sxs-lookup"><span data-stu-id="3d8e3-114">Method</span></span>                                                | <span data-ttu-id="3d8e3-115">描述</span><span class="sxs-lookup"><span data-stu-id="3d8e3-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="3d8e3-116">**解決**</span><span class="sxs-lookup"><span data-stu-id="3d8e3-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="3d8e3-117">解析資料參考。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-117">Resolves data references.</span></span> <span data-ttu-id="3d8e3-118">已取代。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d8e3-119">備註</span><span class="sxs-lookup"><span data-stu-id="3d8e3-119">Remarks</span></span>

<span data-ttu-id="3d8e3-120">確定物件是資料參考物件之後，請使用 [**IDirectXFileDataReference：： Resolve**](idirectxfiledatareference--resolve.md) 方法來取出先前在檔案中定義的參考物件。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="3d8e3-121">如需如何識別資料參考物件的詳細資訊，請參閱 [**IDirectXFileData**](idirectxfiledata.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="3d8e3-122">IDirectXFileDataReference 介面的 GUID 是 IID \_ IDirectXFileDataReference。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="3d8e3-123">LPDIRECTXFILEDataReference 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3d8e3-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="3d8e3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d8e3-124">Requirements</span></span>



| <span data-ttu-id="3d8e3-125">需求</span><span class="sxs-lookup"><span data-stu-id="3d8e3-125">Requirement</span></span> | <span data-ttu-id="3d8e3-126">值</span><span class="sxs-lookup"><span data-stu-id="3d8e3-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8e3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3d8e3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3d8e3-128"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8e3-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d8e3-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3d8e3-129">Library</span></span><br/> | <dl> <span data-ttu-id="3d8e3-130"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d8e3-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8e3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d8e3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8e3-132">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="3d8e3-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="3d8e3-133">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="3d8e3-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




