---
description: ID3DXBuffer 介面是用來做為資料緩衝區，在網格優化和載入作業期間儲存頂點、相鄰和材質資訊。
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: 'ID3DXBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975681"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="21062-103">ID3DXBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="21062-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="21062-104">ID3DXBuffer 介面是用來做為資料緩衝區，在網格優化和載入作業期間儲存頂點、相鄰和材質資訊。</span><span class="sxs-lookup"><span data-stu-id="21062-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="21062-105">緩衝區物件是用來傳回任意長度的資料。</span><span class="sxs-lookup"><span data-stu-id="21062-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="21062-106">此外，也會使用緩衝區物件，在組合頂點和圖元著色器的方法中傳回物件程式碼和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="21062-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="21062-107">成員</span><span class="sxs-lookup"><span data-stu-id="21062-107">Members</span></span>

<span data-ttu-id="21062-108">**ID3DXBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="21062-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21062-109">**ID3DXBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="21062-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="21062-110">方法</span><span class="sxs-lookup"><span data-stu-id="21062-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21062-111">方法</span><span class="sxs-lookup"><span data-stu-id="21062-111">Methods</span></span>

<span data-ttu-id="21062-112">**ID3DXBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="21062-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="21062-113">方法</span><span class="sxs-lookup"><span data-stu-id="21062-113">Method</span></span>                                                    | <span data-ttu-id="21062-114">描述</span><span class="sxs-lookup"><span data-stu-id="21062-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="21062-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="21062-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="21062-116">擷取緩衝區中資料的指標。</span><span class="sxs-lookup"><span data-stu-id="21062-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="21062-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="21062-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="21062-118">抓取緩衝區中資料的總大小。</span><span class="sxs-lookup"><span data-stu-id="21062-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21062-119">備註</span><span class="sxs-lookup"><span data-stu-id="21062-119">Remarks</span></span>

<span data-ttu-id="21062-120">**ID3DXBuffer** 介面是藉由呼叫 [**D3DXCreateBuffer**](d3dxcreatebuffer.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="21062-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="21062-121">LPD3DXBUFFER 型別定義為 **ID3DXBuffer** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="21062-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="21062-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="21062-122">Requirements</span></span>



| <span data-ttu-id="21062-123">需求</span><span class="sxs-lookup"><span data-stu-id="21062-123">Requirement</span></span> | <span data-ttu-id="21062-124">值</span><span class="sxs-lookup"><span data-stu-id="21062-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21062-125">標頭</span><span class="sxs-lookup"><span data-stu-id="21062-125">Header</span></span><br/>  | <dl> <span data-ttu-id="21062-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="21062-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21062-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="21062-127">Library</span></span><br/> | <dl> <span data-ttu-id="21062-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21062-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21062-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21062-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21062-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="21062-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
