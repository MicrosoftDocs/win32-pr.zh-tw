---
description: 應用程式會使用 IDirectXFile 介面的方法來建立 IDirectXFileEnumObject 和 IDirectXFileSaveObject 介面的實例，以及註冊範本。 已取代。
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: 'IDirectXFile 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854060"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="62faa-104">IDirectXFile 介面</span><span class="sxs-lookup"><span data-stu-id="62faa-104">IDirectXFile interface</span></span>

<span data-ttu-id="62faa-105">應用程式會使用 IDirectXFile 介面的方法來建立 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 和 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 介面的實例，以及註冊範本。</span><span class="sxs-lookup"><span data-stu-id="62faa-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="62faa-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="62faa-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="62faa-107">成員</span><span class="sxs-lookup"><span data-stu-id="62faa-107">Members</span></span>

<span data-ttu-id="62faa-108">**IDirectXFile** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="62faa-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62faa-109">**IDirectXFile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62faa-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="62faa-110">方法</span><span class="sxs-lookup"><span data-stu-id="62faa-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62faa-111">方法</span><span class="sxs-lookup"><span data-stu-id="62faa-111">Methods</span></span>

<span data-ttu-id="62faa-112">**IDirectXFile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="62faa-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="62faa-113">方法</span><span class="sxs-lookup"><span data-stu-id="62faa-113">Method</span></span>                                                       | <span data-ttu-id="62faa-114">描述</span><span class="sxs-lookup"><span data-stu-id="62faa-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="62faa-115">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="62faa-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="62faa-116">建立列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="62faa-116">Creates an enumerator object.</span></span> <span data-ttu-id="62faa-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="62faa-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="62faa-118">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="62faa-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="62faa-119">建立儲存物件。</span><span class="sxs-lookup"><span data-stu-id="62faa-119">Creates a save object.</span></span> <span data-ttu-id="62faa-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="62faa-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="62faa-121">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="62faa-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="62faa-122">註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="62faa-122">Registers custom templates.</span></span> <span data-ttu-id="62faa-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="62faa-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="62faa-124">備註</span><span class="sxs-lookup"><span data-stu-id="62faa-124">Remarks</span></span>

<span data-ttu-id="62faa-125">IDirectXFile 介面 (GUID) 的全域唯一識別碼為 IID \_ IDirectXFile。</span><span class="sxs-lookup"><span data-stu-id="62faa-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="62faa-126">IDirectXFile 介面是藉由呼叫 [**DirectXFileCreate**](directxfilecreate.md) 函數來取得。</span><span class="sxs-lookup"><span data-stu-id="62faa-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="62faa-127">LPDIRECTXFILE 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="62faa-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="62faa-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="62faa-128">Requirements</span></span>



| <span data-ttu-id="62faa-129">需求</span><span class="sxs-lookup"><span data-stu-id="62faa-129">Requirement</span></span> | <span data-ttu-id="62faa-130">值</span><span class="sxs-lookup"><span data-stu-id="62faa-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62faa-131">標頭</span><span class="sxs-lookup"><span data-stu-id="62faa-131">Header</span></span><br/>  | <dl> <span data-ttu-id="62faa-132"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="62faa-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="62faa-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="62faa-133">Library</span></span><br/> | <dl> <span data-ttu-id="62faa-134"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62faa-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62faa-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62faa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62faa-136">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="62faa-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
