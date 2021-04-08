---
description: ID3DX10ThreadPump 介面使用的資料處理物件，以非同步方式處理載入的資料。
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: 'ID3DX10DataProcessor 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854096"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="7fc70-103">ID3DX10DataProcessor 介面</span><span class="sxs-lookup"><span data-stu-id="7fc70-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="7fc70-104">[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)使用的資料處理物件，以非同步方式處理載入的資料。</span><span class="sxs-lookup"><span data-stu-id="7fc70-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="7fc70-105">成員</span><span class="sxs-lookup"><span data-stu-id="7fc70-105">Members</span></span>

<span data-ttu-id="7fc70-106">**ID3DX10DataProcessor** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7fc70-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7fc70-107">**ID3DX10DataProcessor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7fc70-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="7fc70-108">方法</span><span class="sxs-lookup"><span data-stu-id="7fc70-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7fc70-109">方法</span><span class="sxs-lookup"><span data-stu-id="7fc70-109">Methods</span></span>

<span data-ttu-id="7fc70-110">**ID3DX10DataProcessor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7fc70-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="7fc70-111">方法</span><span class="sxs-lookup"><span data-stu-id="7fc70-111">Method</span></span>                                                                | <span data-ttu-id="7fc70-112">描述</span><span class="sxs-lookup"><span data-stu-id="7fc70-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fc70-113">**CreateDeviceObject**</span><span class="sxs-lookup"><span data-stu-id="7fc70-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="7fc70-114">建立裝置物件。</span><span class="sxs-lookup"><span data-stu-id="7fc70-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="7fc70-115">**摧毀**</span><span class="sxs-lookup"><span data-stu-id="7fc70-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="7fc70-116">在工作專案完成後， [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來終結處理器。</span><span class="sxs-lookup"><span data-stu-id="7fc70-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="7fc70-117">**處理序**</span><span class="sxs-lookup"><span data-stu-id="7fc70-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="7fc70-118">處理一些資料。</span><span class="sxs-lookup"><span data-stu-id="7fc70-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7fc70-119">備註</span><span class="sxs-lookup"><span data-stu-id="7fc70-119">Remarks</span></span>

<span data-ttu-id="7fc70-120">可以繼承這個物件，並重新定義其成員。</span><span class="sxs-lookup"><span data-stu-id="7fc70-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="7fc70-121">這麼做可讓您自訂 API 來處理您自己的自訂檔案格式。</span><span class="sxs-lookup"><span data-stu-id="7fc70-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc70-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fc70-122">Requirements</span></span>



| <span data-ttu-id="7fc70-123">需求</span><span class="sxs-lookup"><span data-stu-id="7fc70-123">Requirement</span></span> | <span data-ttu-id="7fc70-124">值</span><span class="sxs-lookup"><span data-stu-id="7fc70-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc70-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7fc70-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7fc70-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc70-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fc70-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="7fc70-127">Library</span></span><br/> | <dl> <span data-ttu-id="7fc70-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc70-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc70-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc70-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc70-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="7fc70-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
