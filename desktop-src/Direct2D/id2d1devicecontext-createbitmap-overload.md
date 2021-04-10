---
title: ID2D1DeviceCoNtext CreateBitmap 方法
description: 建立可做為目標介面的點陣圖，以用來讀取回 CPU，或作為 DrawBitmap 和 ID2D1BitmapBrush Api 的來源。 此外，您可以將色彩內容資訊傳遞給點陣圖。
ms.assetid: D1896DEE-4464-48D7-8EFB-18E564E1F88D
keywords:
- CreateBitmap 方法 Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 6086aeef2ee36da9bd3b917ffdae07f3eb6312bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682493"
---
# <a name="id2d1devicecontextcreatebitmap-methods"></a><span data-ttu-id="a5b2e-105">ID2D1DeviceCoNtext：： CreateBitmap 方法</span><span class="sxs-lookup"><span data-stu-id="a5b2e-105">ID2D1DeviceContext::CreateBitmap methods</span></span>

<span data-ttu-id="a5b2e-106">建立可做為目標介面的點陣圖，以用來讀取回 CPU，或作為 [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) 和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) api 的來源。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-106">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="a5b2e-107">此外，您可以將色彩內容資訊傳遞給點陣圖。[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="a5b2e-107">In addition, color context information can be passed to the bitmap.[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>

### <a name="overload-list"></a><span data-ttu-id="a5b2e-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="a5b2e-108">Overload list</span></span>



| <span data-ttu-id="a5b2e-109">方法</span><span class="sxs-lookup"><span data-stu-id="a5b2e-109">Method</span></span>                                                                                                                                 | <span data-ttu-id="a5b2e-110">描述</span><span class="sxs-lookup"><span data-stu-id="a5b2e-110">Description</span></span>                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b2e-111">[**CreateBitmap (D2D1 \_ SIZE \_ U、void \* 、UINT32、D2D1 \_ BITMAP \_ PROPERTIES1、ID2D1Bitmap1 \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="a5b2e-111">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>  | <span data-ttu-id="a5b2e-112">建立可做為目標介面的點陣圖，以用來讀取回 CPU，或作為 [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) 和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) api 的來源。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-112">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="a5b2e-113">此外，您可以將色彩內容資訊傳遞給點陣圖。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-113">In addition, color context information can be passed to the bitmap.</span></span><br/> |
| <span data-ttu-id="a5b2e-114">[**CreateBitmap (D2D1 \_ SIZE \_ U、void \* 、UINT32、D2D1 \_ BITMAP \_ PROPERTIES1 \* 、ID2D1Bitmap1 \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="a5b2e-114">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1\*, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a5b2e-115">[**CreateBitmap (D2D1 \_ SIZE \_ U、void \* 、UINT32、D2D1 \_ BITMAP \_ PROPERTIES1&、ID2D1Bitmap1 \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="a5b2e-115">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1&, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="a5b2e-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5b2e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b2e-117">**ID2D1DeviceCoNtext**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-117">**ID2D1DeviceContext**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)
</dt> </dl>

 

