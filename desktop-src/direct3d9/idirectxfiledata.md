---
description: 應用程式會使用 IDirectXFileData 介面的方法來建立或存取資料物件的直屬階層。
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: 'IDirectXFileData 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977136"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="b933c-103">IDirectXFileData 介面</span><span class="sxs-lookup"><span data-stu-id="b933c-103">IDirectXFileData interface</span></span>

<span data-ttu-id="b933c-104">應用程式會使用 IDirectXFileData 介面的方法來建立或存取資料物件的直屬階層。</span><span class="sxs-lookup"><span data-stu-id="b933c-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="b933c-105">範本限制會決定階層。</span><span class="sxs-lookup"><span data-stu-id="b933c-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="b933c-106">範本所允許的資料類型稱為選擇性成員。</span><span class="sxs-lookup"><span data-stu-id="b933c-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="b933c-107">選用的成員並不是必要的，但物件可能會遺失重要資訊。</span><span class="sxs-lookup"><span data-stu-id="b933c-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="b933c-108">這些選用的成員會儲存為數據物件的子系。</span><span class="sxs-lookup"><span data-stu-id="b933c-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="b933c-109">子系可以是另一個資料物件、較早資料物件的參考，或二進位物件。</span><span class="sxs-lookup"><span data-stu-id="b933c-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="b933c-110">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="b933c-111">成員</span><span class="sxs-lookup"><span data-stu-id="b933c-111">Members</span></span>

<span data-ttu-id="b933c-112">**IDirectXFileData** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。</span><span class="sxs-lookup"><span data-stu-id="b933c-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="b933c-113">**IDirectXFileData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b933c-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="b933c-114">方法</span><span class="sxs-lookup"><span data-stu-id="b933c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b933c-115">方法</span><span class="sxs-lookup"><span data-stu-id="b933c-115">Methods</span></span>

<span data-ttu-id="b933c-116">**IDirectXFileData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b933c-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="b933c-117">方法</span><span class="sxs-lookup"><span data-stu-id="b933c-117">Method</span></span>                                                         | <span data-ttu-id="b933c-118">描述</span><span class="sxs-lookup"><span data-stu-id="b933c-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b933c-119">**AddBinaryObject**</span><span class="sxs-lookup"><span data-stu-id="b933c-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="b933c-120">建立二進位物件，並將它新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="b933c-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="b933c-121">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="b933c-122">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="b933c-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="b933c-123">將資料物件新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="b933c-123">Adds a data object as a child object.</span></span> <span data-ttu-id="b933c-124">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="b933c-125">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="b933c-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="b933c-126">建立資料參考物件，並將其新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="b933c-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="b933c-127">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="b933c-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="b933c-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="b933c-129">抓取其中一個物件成員的資料，或所有成員的資料。</span><span class="sxs-lookup"><span data-stu-id="b933c-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="b933c-130">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="b933c-131">**GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="b933c-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="b933c-132">抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。</span><span class="sxs-lookup"><span data-stu-id="b933c-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="b933c-133">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="b933c-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="b933c-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="b933c-135">抓取物件之範本的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b933c-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="b933c-136">已取代。</span><span class="sxs-lookup"><span data-stu-id="b933c-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b933c-137">備註</span><span class="sxs-lookup"><span data-stu-id="b933c-137">Remarks</span></span>

<span data-ttu-id="b933c-138">IDirectXFileData 介面的 GUID 是 IID \_ IDirectXFileData。</span><span class="sxs-lookup"><span data-stu-id="b933c-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="b933c-139">LPDIRECTXFILEDATA 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b933c-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="b933c-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="b933c-140">Requirements</span></span>



| <span data-ttu-id="b933c-141">需求</span><span class="sxs-lookup"><span data-stu-id="b933c-141">Requirement</span></span> | <span data-ttu-id="b933c-142">值</span><span class="sxs-lookup"><span data-stu-id="b933c-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b933c-143">標頭</span><span class="sxs-lookup"><span data-stu-id="b933c-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b933c-144"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="b933c-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b933c-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="b933c-145">Library</span></span><br/> | <dl> <span data-ttu-id="b933c-146"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b933c-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b933c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b933c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b933c-148">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="b933c-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="b933c-149">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="b933c-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




