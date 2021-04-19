---
description: 應用程式會使用 ID3DXFile 介面的方法來建立 ID3DXFileEnumObject 和 ID3DXFileSaveObject 介面的實例，以及註冊範本。
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: 'ID3DXFile 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000605"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="c7682-103">ID3DXFile 介面</span><span class="sxs-lookup"><span data-stu-id="c7682-103">ID3DXFile interface</span></span>

<span data-ttu-id="c7682-104">應用程式會使用 ID3DXFile 介面的方法來建立 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 和 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的實例，以及註冊範本。</span><span class="sxs-lookup"><span data-stu-id="c7682-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="c7682-105">成員</span><span class="sxs-lookup"><span data-stu-id="c7682-105">Members</span></span>

<span data-ttu-id="c7682-106">**ID3DXFile** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c7682-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c7682-107">**ID3DXFile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7682-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="c7682-108">方法</span><span class="sxs-lookup"><span data-stu-id="c7682-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c7682-109">方法</span><span class="sxs-lookup"><span data-stu-id="c7682-109">Methods</span></span>

<span data-ttu-id="c7682-110">**ID3DXFile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c7682-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="c7682-111">方法</span><span class="sxs-lookup"><span data-stu-id="c7682-111">Method</span></span>                                                            | <span data-ttu-id="c7682-112">描述</span><span class="sxs-lookup"><span data-stu-id="c7682-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7682-113">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="c7682-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="c7682-114">建立將讀取 x.x 檔案的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="c7682-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="c7682-115">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="c7682-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="c7682-116">建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。</span><span class="sxs-lookup"><span data-stu-id="c7682-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="c7682-117">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="c7682-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="c7682-118">在給定 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的情況下註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c7682-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="c7682-119">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="c7682-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="c7682-120">註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c7682-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c7682-121">備註</span><span class="sxs-lookup"><span data-stu-id="c7682-121">Remarks</span></span>

<span data-ttu-id="c7682-122">ID3DXFile 物件也包含本機範本存放區。</span><span class="sxs-lookup"><span data-stu-id="c7682-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="c7682-123">此本機儲存體只能使用 [**ID3DXFile：： RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) 和 [**ID3DXFile：： RegisterTemplates**](id3dxfile--registertemplates.md) 方法新增至。</span><span class="sxs-lookup"><span data-stu-id="c7682-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="c7682-124">使用 [**ID3DXFile：： CreateEnumObject**](id3dxfile--createenumobject.md)和 [**ID3DXFile：： CreateSaveObject**](id3dxfile--createsaveobject.md)建立的 [**ID3DXFileEnumObject**](id3dxfileenumobject.md)和 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)物件也會利用父 ID3DXFile 物件的範本存放區。</span><span class="sxs-lookup"><span data-stu-id="c7682-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="c7682-125">ID3DXFile 介面是藉由呼叫 [**D3DXFileCreate**](d3dxfilecreate.md) 函數來取得。</span><span class="sxs-lookup"><span data-stu-id="c7682-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="c7682-126">ID3DXFile 介面 (GUID) 的全域唯一識別碼為 IID \_ ID3DXFile。</span><span class="sxs-lookup"><span data-stu-id="c7682-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="c7682-127">LPD3DXFILE 型別定義為 ID3DXFile 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c7682-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="c7682-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7682-128">Requirements</span></span>



| <span data-ttu-id="c7682-129">需求</span><span class="sxs-lookup"><span data-stu-id="c7682-129">Requirement</span></span> | <span data-ttu-id="c7682-130">值</span><span class="sxs-lookup"><span data-stu-id="c7682-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7682-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c7682-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c7682-132"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7682-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c7682-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7682-133">Library</span></span><br/> | <dl> <span data-ttu-id="c7682-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7682-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7682-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7682-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7682-136">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="c7682-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
