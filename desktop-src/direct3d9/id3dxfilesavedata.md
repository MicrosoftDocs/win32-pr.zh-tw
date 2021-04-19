---
description: 應用程式會使用 ID3DXFileSaveData 介面的方法，將資料物件新增為. x 檔案資料節點的子系。
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: 'ID3DXFileSaveData 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988589"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="d7219-103">ID3DXFileSaveData 介面</span><span class="sxs-lookup"><span data-stu-id="d7219-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="d7219-104">應用程式會使用 ID3DXFileSaveData 介面的方法，將資料物件新增為. x 檔案資料節點的子系。</span><span class="sxs-lookup"><span data-stu-id="d7219-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="d7219-105">成員</span><span class="sxs-lookup"><span data-stu-id="d7219-105">Members</span></span>

<span data-ttu-id="d7219-106">**ID3DXFileSaveData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d7219-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7219-107">**ID3DXFileSaveData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7219-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="d7219-108">方法</span><span class="sxs-lookup"><span data-stu-id="d7219-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7219-109">方法</span><span class="sxs-lookup"><span data-stu-id="d7219-109">Methods</span></span>

<span data-ttu-id="d7219-110">**ID3DXFileSaveData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d7219-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="d7219-111">方法</span><span class="sxs-lookup"><span data-stu-id="d7219-111">Method</span></span>                                                          | <span data-ttu-id="d7219-112">描述</span><span class="sxs-lookup"><span data-stu-id="d7219-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7219-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="d7219-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="d7219-114">將資料物件新增為 **ID3DXFileSaveData** 檔資料節點的子系。</span><span class="sxs-lookup"><span data-stu-id="d7219-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="d7219-115">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="d7219-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="d7219-116">將資料參考加入為這個 **ID3DXFileSaveData** 檔資料節點的子系。</span><span class="sxs-lookup"><span data-stu-id="d7219-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="d7219-117">資料參考會指向檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="d7219-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="d7219-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="d7219-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="d7219-119">抓取這個 **ID3DXFileSaveData** 檔資料節點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d7219-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="d7219-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="d7219-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="d7219-121">抓取這個 **ID3DXFileSaveData** 檔資料節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7219-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="d7219-122">**GetSave**</span><span class="sxs-lookup"><span data-stu-id="d7219-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="d7219-123">抓取這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 檔資料節點的指標。</span><span class="sxs-lookup"><span data-stu-id="d7219-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="d7219-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="d7219-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="d7219-125">抓取此檔案資料節點的範本識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7219-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d7219-126">備註</span><span class="sxs-lookup"><span data-stu-id="d7219-126">Remarks</span></span>

<span data-ttu-id="d7219-127">ID3DXFileSaveObject 介面的 GUID 是 IID \_ ID3DXFileSaveObject。</span><span class="sxs-lookup"><span data-stu-id="d7219-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="d7219-128">LPD3DXFileSaveData 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d7219-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="d7219-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7219-129">Requirements</span></span>



| <span data-ttu-id="d7219-130">需求</span><span class="sxs-lookup"><span data-stu-id="d7219-130">Requirement</span></span> | <span data-ttu-id="d7219-131">值</span><span class="sxs-lookup"><span data-stu-id="d7219-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7219-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d7219-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d7219-133"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7219-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d7219-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7219-134">Library</span></span><br/> | <dl> <span data-ttu-id="d7219-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7219-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d7219-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7219-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7219-137">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="d7219-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
