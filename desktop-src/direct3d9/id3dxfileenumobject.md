---
description: 應用程式會使用 ID3DXFileEnumObject 介面的方法，迴圈流覽檔案中的子檔案資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得子物件。
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: 'ID3DXFileEnumObject 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946153"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="19724-103">ID3DXFileEnumObject 介面</span><span class="sxs-lookup"><span data-stu-id="19724-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="19724-104">應用程式會使用 ID3DXFileEnumObject 介面的方法，迴圈流覽檔案中的子檔案資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得子物件。</span><span class="sxs-lookup"><span data-stu-id="19724-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="19724-105">成員</span><span class="sxs-lookup"><span data-stu-id="19724-105">Members</span></span>

<span data-ttu-id="19724-106">**ID3DXFileEnumObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="19724-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19724-107">**ID3DXFileEnumObject** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19724-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="19724-108">方法</span><span class="sxs-lookup"><span data-stu-id="19724-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19724-109">方法</span><span class="sxs-lookup"><span data-stu-id="19724-109">Methods</span></span>

<span data-ttu-id="19724-110">**ID3DXFileEnumObject** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="19724-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="19724-111">方法</span><span class="sxs-lookup"><span data-stu-id="19724-111">Method</span></span>                                                                  | <span data-ttu-id="19724-112">描述</span><span class="sxs-lookup"><span data-stu-id="19724-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="19724-113">**System.windows.media.visualtreehelper.getchild**</span><span class="sxs-lookup"><span data-stu-id="19724-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="19724-114">抓取這個檔案資料物件中的子物件。</span><span class="sxs-lookup"><span data-stu-id="19724-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="19724-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="19724-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="19724-116">抓取這個檔案資料物件中的子物件數目。</span><span class="sxs-lookup"><span data-stu-id="19724-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="19724-117">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="19724-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="19724-118">抓取具有指定之 GUID 的資料物件。</span><span class="sxs-lookup"><span data-stu-id="19724-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="19724-119">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="19724-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="19724-120">抓取具有指定名稱的資料物件。</span><span class="sxs-lookup"><span data-stu-id="19724-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="19724-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="19724-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="19724-122">抓取 [**ID3DXFile**](id3dxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="19724-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="19724-123">備註</span><span class="sxs-lookup"><span data-stu-id="19724-123">Remarks</span></span>

<span data-ttu-id="19724-124">ID3DXFileEnumObject 介面的 GUID 是 IID \_ ID3DXFileEnumObject。</span><span class="sxs-lookup"><span data-stu-id="19724-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="19724-125">LPD3DXFILEENUMOBJECT 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="19724-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="19724-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="19724-126">Requirements</span></span>



| <span data-ttu-id="19724-127">需求</span><span class="sxs-lookup"><span data-stu-id="19724-127">Requirement</span></span> | <span data-ttu-id="19724-128">值</span><span class="sxs-lookup"><span data-stu-id="19724-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19724-129">標頭</span><span class="sxs-lookup"><span data-stu-id="19724-129">Header</span></span><br/>  | <dl> <span data-ttu-id="19724-130"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="19724-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="19724-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="19724-131">Library</span></span><br/> | <dl> <span data-ttu-id="19724-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19724-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="19724-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19724-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19724-134">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="19724-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
