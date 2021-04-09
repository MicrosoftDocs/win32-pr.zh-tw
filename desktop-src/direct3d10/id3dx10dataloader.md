---
description: ID3DX10ThreadPump 介面用來以非同步方式載入資料的資料載入物件。
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: 'ID3DX10DataLoader 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946112"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="13d0e-103">ID3DX10DataLoader 介面</span><span class="sxs-lookup"><span data-stu-id="13d0e-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="13d0e-104">[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)用來以非同步方式載入資料的資料載入物件。</span><span class="sxs-lookup"><span data-stu-id="13d0e-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="13d0e-105">成員</span><span class="sxs-lookup"><span data-stu-id="13d0e-105">Members</span></span>

<span data-ttu-id="13d0e-106">**ID3DX10DataLoader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="13d0e-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="13d0e-107">**ID3DX10DataLoader** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13d0e-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="13d0e-108">方法</span><span class="sxs-lookup"><span data-stu-id="13d0e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13d0e-109">方法</span><span class="sxs-lookup"><span data-stu-id="13d0e-109">Methods</span></span>

<span data-ttu-id="13d0e-110">**ID3DX10DataLoader** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="13d0e-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="13d0e-111">方法</span><span class="sxs-lookup"><span data-stu-id="13d0e-111">Method</span></span>                                             | <span data-ttu-id="13d0e-112">描述</span><span class="sxs-lookup"><span data-stu-id="13d0e-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13d0e-113">**解 壓縮**</span><span class="sxs-lookup"><span data-stu-id="13d0e-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="13d0e-114">用來解壓縮編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="13d0e-114">Used to decompress encoded data.</span></span> <span data-ttu-id="13d0e-115">這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。</span><span class="sxs-lookup"><span data-stu-id="13d0e-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="13d0e-116">從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="13d0e-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="13d0e-117">**摧毀**</span><span class="sxs-lookup"><span data-stu-id="13d0e-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="13d0e-118">在工作專案完成後， [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來終結載入器。</span><span class="sxs-lookup"><span data-stu-id="13d0e-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="13d0e-119">**載入**</span><span class="sxs-lookup"><span data-stu-id="13d0e-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="13d0e-120">由 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來從磁片載入資料。</span><span class="sxs-lookup"><span data-stu-id="13d0e-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="13d0e-121">備註</span><span class="sxs-lookup"><span data-stu-id="13d0e-121">Remarks</span></span>

<span data-ttu-id="13d0e-122">可以繼承這個物件，並重新定義其成員。</span><span class="sxs-lookup"><span data-stu-id="13d0e-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="13d0e-123">這麼做可讓您自訂 API 以載入和解壓縮您自己的自訂檔案格式。</span><span class="sxs-lookup"><span data-stu-id="13d0e-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d0e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="13d0e-124">Requirements</span></span>



| <span data-ttu-id="13d0e-125">需求</span><span class="sxs-lookup"><span data-stu-id="13d0e-125">Requirement</span></span> | <span data-ttu-id="13d0e-126">值</span><span class="sxs-lookup"><span data-stu-id="13d0e-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13d0e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="13d0e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="13d0e-128"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="13d0e-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="13d0e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="13d0e-129">Library</span></span><br/> | <dl> <span data-ttu-id="13d0e-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13d0e-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d0e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13d0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d0e-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="13d0e-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
