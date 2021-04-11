---
description: 應用程式會使用 ID3DXFileData 介面的方法來建立或存取資料物件的直屬階層。 範本限制會決定階層。
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: 'ID3DXFileData 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196340"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="c5088-104">ID3DXFileData 介面</span><span class="sxs-lookup"><span data-stu-id="c5088-104">ID3DXFileData interface</span></span>

<span data-ttu-id="c5088-105">應用程式會使用 ID3DXFileData 介面的方法來建立或存取資料物件的直屬階層。</span><span class="sxs-lookup"><span data-stu-id="c5088-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="c5088-106">範本限制會決定階層。</span><span class="sxs-lookup"><span data-stu-id="c5088-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="c5088-107">成員</span><span class="sxs-lookup"><span data-stu-id="c5088-107">Members</span></span>

<span data-ttu-id="c5088-108">**ID3DXFileData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c5088-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c5088-109">**ID3DXFileData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c5088-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="c5088-110">方法</span><span class="sxs-lookup"><span data-stu-id="c5088-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c5088-111">方法</span><span class="sxs-lookup"><span data-stu-id="c5088-111">Methods</span></span>

<span data-ttu-id="c5088-112">**ID3DXFileData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c5088-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="c5088-113">方法</span><span class="sxs-lookup"><span data-stu-id="c5088-113">Method</span></span>                                            | <span data-ttu-id="c5088-114">描述</span><span class="sxs-lookup"><span data-stu-id="c5088-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5088-115">**System.windows.media.visualtreehelper.getchild**</span><span class="sxs-lookup"><span data-stu-id="c5088-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="c5088-116">抓取這個檔案資料物件中的子物件。</span><span class="sxs-lookup"><span data-stu-id="c5088-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="c5088-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="c5088-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="c5088-118">捕獲此檔案資料物件中的子係數目。</span><span class="sxs-lookup"><span data-stu-id="c5088-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="c5088-119">**GetEnum**</span><span class="sxs-lookup"><span data-stu-id="c5088-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="c5088-120">抓取這個檔案資料物件中的列舉物件。</span><span class="sxs-lookup"><span data-stu-id="c5088-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="c5088-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="c5088-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="c5088-122">抓取此檔案資料物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5088-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="c5088-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="c5088-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="c5088-124">抓取這個檔案資料物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5088-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="c5088-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="c5088-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="c5088-126">抓取此檔案資料物件中的範本識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5088-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="c5088-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="c5088-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="c5088-128">指出此檔案資料物件是否為指向另一個子資料物件的參考物件。</span><span class="sxs-lookup"><span data-stu-id="c5088-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="c5088-129">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="c5088-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="c5088-130">存取. x 檔案資料。</span><span class="sxs-lookup"><span data-stu-id="c5088-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="c5088-131">**Unlock**</span><span class="sxs-lookup"><span data-stu-id="c5088-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="c5088-132">結束 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md)所傳回之 *ppData* 指標的存留期。</span><span class="sxs-lookup"><span data-stu-id="c5088-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5088-133">備註</span><span class="sxs-lookup"><span data-stu-id="c5088-133">Remarks</span></span>

<span data-ttu-id="c5088-134">範本所允許的資料類型稱為選擇性成員。</span><span class="sxs-lookup"><span data-stu-id="c5088-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="c5088-135">選用的成員並不是必要的，但物件可能會遺失重要資訊。</span><span class="sxs-lookup"><span data-stu-id="c5088-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="c5088-136">這些選用的成員會儲存為數據物件的子系。</span><span class="sxs-lookup"><span data-stu-id="c5088-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="c5088-137">子系可以是其他資料物件或較早資料物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c5088-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="c5088-138">ID3DXFileData 介面的 GUID 是 IID \_ ID3DXFileData。</span><span class="sxs-lookup"><span data-stu-id="c5088-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="c5088-139">LPD3DXFILEDATA 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c5088-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="c5088-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5088-140">Requirements</span></span>



| <span data-ttu-id="c5088-141">需求</span><span class="sxs-lookup"><span data-stu-id="c5088-141">Requirement</span></span> | <span data-ttu-id="c5088-142">值</span><span class="sxs-lookup"><span data-stu-id="c5088-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5088-143">標頭</span><span class="sxs-lookup"><span data-stu-id="c5088-143">Header</span></span><br/>  | <dl> <span data-ttu-id="c5088-144"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5088-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c5088-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5088-145">Library</span></span><br/> | <dl> <span data-ttu-id="c5088-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5088-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c5088-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5088-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5088-148">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="c5088-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
