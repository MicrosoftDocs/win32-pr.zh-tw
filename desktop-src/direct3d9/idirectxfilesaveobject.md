---
description: 應用程式會使用 IDirectXFileSaveObject 介面的方法來建立資料物件，以及儲存範本和資料物件。
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: 'IDirectXFileSaveObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982005"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="193c8-103">IDirectXFileSaveObject 介面</span><span class="sxs-lookup"><span data-stu-id="193c8-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="193c8-104">應用程式會使用 IDirectXFileSaveObject 介面的方法來建立資料物件，以及儲存範本和資料物件。</span><span class="sxs-lookup"><span data-stu-id="193c8-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="193c8-105">請注意，每個檔案都不需要範本。</span><span class="sxs-lookup"><span data-stu-id="193c8-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="193c8-106">例如，您可以將所有範本放入單一 Microsoft DirectX 檔案中，而不是在每個 DirectX 檔案中複製它們。</span><span class="sxs-lookup"><span data-stu-id="193c8-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="193c8-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="193c8-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="193c8-108">成員</span><span class="sxs-lookup"><span data-stu-id="193c8-108">Members</span></span>

<span data-ttu-id="193c8-109">**IDirectXFileSaveObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="193c8-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="193c8-110">**IDirectXFileSaveObject** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="193c8-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="193c8-111">方法</span><span class="sxs-lookup"><span data-stu-id="193c8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="193c8-112">方法</span><span class="sxs-lookup"><span data-stu-id="193c8-112">Methods</span></span>

<span data-ttu-id="193c8-113">**IDirectXFileSaveObject** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="193c8-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="193c8-114">方法</span><span class="sxs-lookup"><span data-stu-id="193c8-114">Method</span></span>                                                               | <span data-ttu-id="193c8-115">描述</span><span class="sxs-lookup"><span data-stu-id="193c8-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="193c8-116">**CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="193c8-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="193c8-117">建立資料物件。</span><span class="sxs-lookup"><span data-stu-id="193c8-117">Creates a data object.</span></span> <span data-ttu-id="193c8-118">已取代。</span><span class="sxs-lookup"><span data-stu-id="193c8-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="193c8-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="193c8-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="193c8-120">將資料物件和其子系儲存至 DirectX 檔案。</span><span class="sxs-lookup"><span data-stu-id="193c8-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="193c8-121">已取代。</span><span class="sxs-lookup"><span data-stu-id="193c8-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="193c8-122">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="193c8-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="193c8-123">將範本儲存至 DirectX 檔案。</span><span class="sxs-lookup"><span data-stu-id="193c8-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="193c8-124">已取代。</span><span class="sxs-lookup"><span data-stu-id="193c8-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="193c8-125">備註</span><span class="sxs-lookup"><span data-stu-id="193c8-125">Remarks</span></span>

<span data-ttu-id="193c8-126">IDirectXFileSaveObject 介面 (GUID) 的全域唯一識別碼為 **IID \_ IDirectXFileSaveObject**。</span><span class="sxs-lookup"><span data-stu-id="193c8-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="193c8-127">**IDirectXFileSaveObject** 介面的取得方式是呼叫 [**IDirectXFile：： CreateSaveObject**](idirectxfile--createsaveobject.md)方法。</span><span class="sxs-lookup"><span data-stu-id="193c8-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="193c8-128">**LPDIRECTXFILESAVEOBJECT** 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="193c8-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="193c8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="193c8-129">Requirements</span></span>



| <span data-ttu-id="193c8-130">需求</span><span class="sxs-lookup"><span data-stu-id="193c8-130">Requirement</span></span> | <span data-ttu-id="193c8-131">值</span><span class="sxs-lookup"><span data-stu-id="193c8-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="193c8-132">標頭</span><span class="sxs-lookup"><span data-stu-id="193c8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="193c8-133"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="193c8-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="193c8-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="193c8-134">Library</span></span><br/> | <dl> <span data-ttu-id="193c8-135"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="193c8-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="193c8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="193c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193c8-137">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="193c8-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
