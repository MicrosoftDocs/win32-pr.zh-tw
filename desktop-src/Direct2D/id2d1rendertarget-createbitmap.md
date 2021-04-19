---
title: ID2D1RenderTarget CreateBitmap 方法
description: 建立 Direct2D 點陣圖。
ms.assetid: b45d353f-ae33-4110-b7c8-f14661017e0f
keywords:
- CreateBitmap 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4576b9111d9180b395527bad8b06ee3f9a8eef2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978409"
---
# <a name="id2d1rendertargetcreatebitmap-methods"></a><span data-ttu-id="69caf-104">ID2D1RenderTarget：： CreateBitmap 方法</span><span class="sxs-lookup"><span data-stu-id="69caf-104">ID2D1RenderTarget::CreateBitmap methods</span></span>

<span data-ttu-id="69caf-105">建立 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="69caf-105">Creates a Direct2D bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="69caf-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="69caf-106">Overload list</span></span>



| <span data-ttu-id="69caf-107">方法</span><span class="sxs-lookup"><span data-stu-id="69caf-107">Method</span></span>                                                                                                                                                                                                   | <span data-ttu-id="69caf-108">描述</span><span class="sxs-lookup"><span data-stu-id="69caf-108">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="69caf-109">[**CreateBitmap (D2D1 \_ SIZE \_ U、D2D1 \_ BITMAP \_ PROPERTIES&、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69caf-109">[**CreateBitmap(D2D1\_SIZE\_U,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span>                                | <span data-ttu-id="69caf-110">建立未初始化的 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="69caf-110">Creates an uninitialized Direct2D bitmap.</span></span> <br/>                          |
| <span data-ttu-id="69caf-111">[**CreateBitmap (D2D1 \_ SIZE \_ U、void \* 、UINT32、D2D1 \_ BITMAP \_ 屬性 \* 、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69caf-111">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES\*,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span> | <span data-ttu-id="69caf-112">從記憶體內部來源資料的指標建立 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="69caf-112">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span><br/>  |
| <span data-ttu-id="69caf-113">[**CreateBitmap (D2D1 \_ SIZE \_ U、void \* 、UINT32、D2D1 \_ BITMAP \_ 屬性&、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69caf-113">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span></span>  | <span data-ttu-id="69caf-114">從記憶體內部來源資料的指標建立 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="69caf-114">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="69caf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="69caf-115">Requirements</span></span>



| <span data-ttu-id="69caf-116">需求</span><span class="sxs-lookup"><span data-stu-id="69caf-116">Requirement</span></span> | <span data-ttu-id="69caf-117">值</span><span class="sxs-lookup"><span data-stu-id="69caf-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="69caf-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="69caf-118">Library</span></span><br/> | <dl> <span data-ttu-id="69caf-119"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69caf-119"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="69caf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="69caf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="69caf-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69caf-121"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69caf-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69caf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69caf-123">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="69caf-123">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

