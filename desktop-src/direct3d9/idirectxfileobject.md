---
description: 應用程式會使用 IDirectXFileObject 介面的方法，來取得 Microsoft DirectX 檔案物件的相關資訊。 已取代。
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: 'IDirectXFileObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986505"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="099cb-104">IDirectXFileObject 介面</span><span class="sxs-lookup"><span data-stu-id="099cb-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="099cb-105">應用程式會使用 IDirectXFileObject 介面的方法，來取得 Microsoft DirectX 檔案物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="099cb-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="099cb-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="099cb-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="099cb-107">成員</span><span class="sxs-lookup"><span data-stu-id="099cb-107">Members</span></span>

<span data-ttu-id="099cb-108">**IDirectXFileObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="099cb-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="099cb-109">**IDirectXFileObject** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="099cb-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="099cb-110">方法</span><span class="sxs-lookup"><span data-stu-id="099cb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="099cb-111">方法</span><span class="sxs-lookup"><span data-stu-id="099cb-111">Methods</span></span>

<span data-ttu-id="099cb-112">**IDirectXFileObject** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="099cb-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="099cb-113">方法</span><span class="sxs-lookup"><span data-stu-id="099cb-113">Method</span></span>                                         | <span data-ttu-id="099cb-114">描述</span><span class="sxs-lookup"><span data-stu-id="099cb-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="099cb-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="099cb-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="099cb-116">抓取識別 DirectX 檔案物件的 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="099cb-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="099cb-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="099cb-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="099cb-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="099cb-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="099cb-119">捕獲 DirectX 檔案物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="099cb-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="099cb-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="099cb-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="099cb-121">備註</span><span class="sxs-lookup"><span data-stu-id="099cb-121">Remarks</span></span>

<span data-ttu-id="099cb-122">IDirectXFileObject 介面的 GUID 是 IID \_ IDirectXFileObject。</span><span class="sxs-lookup"><span data-stu-id="099cb-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="099cb-123">LPDIRECTXFILEOBJECT 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="099cb-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="099cb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="099cb-124">Requirements</span></span>



| <span data-ttu-id="099cb-125">需求</span><span class="sxs-lookup"><span data-stu-id="099cb-125">Requirement</span></span> | <span data-ttu-id="099cb-126">值</span><span class="sxs-lookup"><span data-stu-id="099cb-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="099cb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="099cb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="099cb-128"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="099cb-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="099cb-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="099cb-129">Library</span></span><br/> | <dl> <span data-ttu-id="099cb-130"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="099cb-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099cb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="099cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099cb-132">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="099cb-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
