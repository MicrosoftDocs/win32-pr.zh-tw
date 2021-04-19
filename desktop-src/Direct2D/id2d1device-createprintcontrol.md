---
title: 'ID2D1Device CreatePrintControl 方法 (D2d1 \_ 1 .h) '
description: 建立 ID2D1PrintControl 物件，將儲存在 ID2D1CommandList 中的 Direct2D 基本專案轉換成固定頁面標記法。 然後，列印子系統會使用基本。
ms.assetid: C8860AEE-807A-435E-9F44-B50545320EDA
keywords:
- CreatePrintControl 方法 Direct2D
topic_type:
- apiref
api_location:
- d2d1_1.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ec8705d73f40fc967b3247aaf81caebcade47b02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985984"
---
# <a name="id2d1devicecreateprintcontrol-methods"></a><span data-ttu-id="261e8-105">ID2D1Device：： CreatePrintControl 方法</span><span class="sxs-lookup"><span data-stu-id="261e8-105">ID2D1Device::CreatePrintControl methods</span></span>

<span data-ttu-id="261e8-106">建立 [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)物件，將儲存在 [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)中的 [Direct2D](/windows/desktop/direct2d/direct2d-portal)基本專案轉換成固定頁面標記法。</span><span class="sxs-lookup"><span data-stu-id="261e8-106">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="261e8-107">然後，列印子系統會使用基本。</span><span class="sxs-lookup"><span data-stu-id="261e8-107">The print sub-system then consumes the primitives.</span></span>

### <a name="overload-list"></a><span data-ttu-id="261e8-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="261e8-108">Overload list</span></span>



| <span data-ttu-id="261e8-109">方法</span><span class="sxs-lookup"><span data-stu-id="261e8-109">Method</span></span>                                                                                                                                                                           | <span data-ttu-id="261e8-110">描述</span><span class="sxs-lookup"><span data-stu-id="261e8-110">Description</span></span>                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="261e8-111">[**CreatePrintControl (IWICImagingFactory \* 、IPrintDocumentPackageTarget \* 、D2D1 \_ PRINT \_ 控制項 \_ 屬性 \* 、ID2D1PrintControl \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="261e8-111">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES\*, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span></span> | <span data-ttu-id="261e8-112">建立 [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)物件，將儲存在 [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)中的 [Direct2D](/windows/desktop/direct2d/direct2d-portal)基本專案轉換成固定頁面標記法。</span><span class="sxs-lookup"><span data-stu-id="261e8-112">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="261e8-113">然後，列印子系統會使用基本。</span><span class="sxs-lookup"><span data-stu-id="261e8-113">The print sub-system then consumes the primitives.</span></span><br/> |
| <span data-ttu-id="261e8-114">[**CreatePrintControl (IWICImagingFactory \* 、IPrintDocumentPackageTarget \* 、D2D1 \_ PRINT \_ 控制項 \_ 屬性&、ID2D1PrintControl \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="261e8-114">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES&, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span></span>    | <span data-ttu-id="261e8-115">建立 [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)物件，將儲存在 [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)中的 [Direct2D](/windows/desktop/direct2d/direct2d-portal)基本專案轉換成固定頁面標記法。</span><span class="sxs-lookup"><span data-stu-id="261e8-115">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="261e8-116">然後，列印子系統會使用基本。</span><span class="sxs-lookup"><span data-stu-id="261e8-116">The print sub-system then consumes the primitives.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="261e8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="261e8-117">Requirements</span></span>



| <span data-ttu-id="261e8-118">需求</span><span class="sxs-lookup"><span data-stu-id="261e8-118">Requirement</span></span> | <span data-ttu-id="261e8-119">值</span><span class="sxs-lookup"><span data-stu-id="261e8-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="261e8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="261e8-120">Header</span></span><br/> | <dl> <span data-ttu-id="261e8-121"><dt>D2d1 \_ 1. h</dt></span><span class="sxs-lookup"><span data-stu-id="261e8-121"><dt>D2d1\_1.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261e8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="261e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261e8-123">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="261e8-123">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
</dt> </dl>

<span data-ttu-id="261e8-124">�</span><span class="sxs-lookup"><span data-stu-id="261e8-124">�</span></span>

<span data-ttu-id="261e8-125">�</span><span class="sxs-lookup"><span data-stu-id="261e8-125">�</span></span>
