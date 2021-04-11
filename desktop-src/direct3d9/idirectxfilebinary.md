---
description: 應用程式會使用 IDirectXFileBinary 介面的方法來讀取和取出二進位資料的相關資訊。 已取代。
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: 'IDirectXFileBinary 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196220"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="52eac-104">IDirectXFileBinary 介面</span><span class="sxs-lookup"><span data-stu-id="52eac-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="52eac-105">應用程式會使用 IDirectXFileBinary 介面的方法來讀取和取出二進位資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="52eac-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="52eac-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="52eac-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="52eac-107">成員</span><span class="sxs-lookup"><span data-stu-id="52eac-107">Members</span></span>

<span data-ttu-id="52eac-108">**IDirectXFileBinary** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。</span><span class="sxs-lookup"><span data-stu-id="52eac-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="52eac-109">**IDirectXFileBinary** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="52eac-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="52eac-110">方法</span><span class="sxs-lookup"><span data-stu-id="52eac-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52eac-111">方法</span><span class="sxs-lookup"><span data-stu-id="52eac-111">Methods</span></span>

<span data-ttu-id="52eac-112">**IDirectXFileBinary** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="52eac-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="52eac-113">方法</span><span class="sxs-lookup"><span data-stu-id="52eac-113">Method</span></span>                                                 | <span data-ttu-id="52eac-114">描述</span><span class="sxs-lookup"><span data-stu-id="52eac-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52eac-115">**GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="52eac-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="52eac-116">抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="52eac-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="52eac-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="52eac-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="52eac-118">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="52eac-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="52eac-119">捕獲二進位資料的大小。</span><span class="sxs-lookup"><span data-stu-id="52eac-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="52eac-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="52eac-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="52eac-121">**讀**</span><span class="sxs-lookup"><span data-stu-id="52eac-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="52eac-122">讀取二進位資料。</span><span class="sxs-lookup"><span data-stu-id="52eac-122">Reads the binary data.</span></span> <span data-ttu-id="52eac-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="52eac-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="52eac-124">備註</span><span class="sxs-lookup"><span data-stu-id="52eac-124">Remarks</span></span>

<span data-ttu-id="52eac-125">IDirectXFileBinary 介面的 GUID 是 IID \_ IDirectXFileBinary。</span><span class="sxs-lookup"><span data-stu-id="52eac-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="52eac-126">LPDIRECTXFileBinary 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="52eac-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="52eac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="52eac-127">Requirements</span></span>



| <span data-ttu-id="52eac-128">需求</span><span class="sxs-lookup"><span data-stu-id="52eac-128">Requirement</span></span> | <span data-ttu-id="52eac-129">值</span><span class="sxs-lookup"><span data-stu-id="52eac-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52eac-130">標頭</span><span class="sxs-lookup"><span data-stu-id="52eac-130">Header</span></span><br/>  | <dl> <span data-ttu-id="52eac-131"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="52eac-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="52eac-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="52eac-132">Library</span></span><br/> | <dl> <span data-ttu-id="52eac-133"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52eac-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52eac-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52eac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52eac-135">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="52eac-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="52eac-136">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="52eac-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




