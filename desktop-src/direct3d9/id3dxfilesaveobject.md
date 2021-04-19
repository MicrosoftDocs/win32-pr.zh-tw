---
description: 應用程式會使用 ID3DXFileSaveObject 介面的方法，將. x 檔案寫入至磁片，以及加入和儲存資料物件和範本。
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: 'ID3DXFileSaveObject 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976481"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="13012-103">ID3DXFileSaveObject 介面</span><span class="sxs-lookup"><span data-stu-id="13012-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="13012-104">應用程式會使用 ID3DXFileSaveObject 介面的方法，將. x 檔案寫入至磁片，以及加入和儲存資料物件和範本。</span><span class="sxs-lookup"><span data-stu-id="13012-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="13012-105">成員</span><span class="sxs-lookup"><span data-stu-id="13012-105">Members</span></span>

<span data-ttu-id="13012-106">**ID3DXFileSaveObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="13012-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="13012-107">**ID3DXFileSaveObject** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13012-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="13012-108">方法</span><span class="sxs-lookup"><span data-stu-id="13012-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13012-109">方法</span><span class="sxs-lookup"><span data-stu-id="13012-109">Methods</span></span>

<span data-ttu-id="13012-110">**ID3DXFileSaveObject** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="13012-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="13012-111">方法</span><span class="sxs-lookup"><span data-stu-id="13012-111">Method</span></span>                                                      | <span data-ttu-id="13012-112">描述</span><span class="sxs-lookup"><span data-stu-id="13012-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13012-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="13012-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="13012-114">將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件的子系。</span><span class="sxs-lookup"><span data-stu-id="13012-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="13012-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="13012-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="13012-116">取得建立這個 **ID3DXFileSaveObject** 物件之物件的 [**ID3DXFile**](id3dxfile.md)介面。</span><span class="sxs-lookup"><span data-stu-id="13012-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="13012-117">**儲存**</span><span class="sxs-lookup"><span data-stu-id="13012-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="13012-118">將資料物件和其子系儲存至磁片上的. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="13012-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="13012-119">備註</span><span class="sxs-lookup"><span data-stu-id="13012-119">Remarks</span></span>

<span data-ttu-id="13012-120">每個檔案都不需要範本。</span><span class="sxs-lookup"><span data-stu-id="13012-120">Templates are not required in every file.</span></span> <span data-ttu-id="13012-121">例如，您可以將所有範本放入單一的. x 檔案中，而不是在每個. x 檔案中複製它們。</span><span class="sxs-lookup"><span data-stu-id="13012-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="13012-122">ID3DXFileSaveObject 介面的取得方式是呼叫 [**ID3DXFile：： CreateSaveObject**](id3dxfile--createsaveobject.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="13012-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="13012-123">ID3DXFileSaveObject 介面 (GUID) 的全域唯一識別碼為 IID \_ ID3DXFileSaveObject。</span><span class="sxs-lookup"><span data-stu-id="13012-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="13012-124">LPD3DXFILESAVEOBJECT 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="13012-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="13012-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="13012-125">Requirements</span></span>



| <span data-ttu-id="13012-126">需求</span><span class="sxs-lookup"><span data-stu-id="13012-126">Requirement</span></span> | <span data-ttu-id="13012-127">值</span><span class="sxs-lookup"><span data-stu-id="13012-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13012-128">標頭</span><span class="sxs-lookup"><span data-stu-id="13012-128">Header</span></span><br/>  | <dl> <span data-ttu-id="13012-129"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="13012-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="13012-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="13012-130">Library</span></span><br/> | <dl> <span data-ttu-id="13012-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13012-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="13012-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13012-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13012-133">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="13012-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
