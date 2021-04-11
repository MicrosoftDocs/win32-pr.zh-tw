---
description: MXDC \_ S0 \_ 頁面 \_ 列舉列舉是用來指定可與 XPS 檔中的頁面相關聯的資源類型，以及可由 Microsoft XPS 檔轉換器 (MXDC) 到其輸出的處理或傳遞的資源類型。
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: 'MXDC_S0_PAGE_ENUMS 列舉 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849211"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="4b5f6-103">MXDC \_ S0 \_ 頁面 \_ 列舉列舉</span><span class="sxs-lookup"><span data-stu-id="4b5f6-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="4b5f6-104">**MXDC \_ S0 \_ 頁面 \_** 列舉列舉是用來指定可與 XPS 檔中的頁面相關聯的資源類型，以及可由 MICROSOFT XPS 檔轉換器 (MXDC) 到其輸出的處理或傳遞的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b5f6-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="4b5f6-106">常數</span><span class="sxs-lookup"><span data-stu-id="4b5f6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4b5f6-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC \_ 資源 \_ TTF**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-108">TrueType 或 OpenType 字型。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ 資源 \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-110">JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="4b5f6-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ 資源 \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-112">PNG 影像。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ 資源 \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-114">TIFF 影像。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ 資源 \_ WDP**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-116">Windows Media 相片影像。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC \_ 資源 \_ 字典**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-118">應傳遞給 MXDC 未處理之輸出的遠端資源字典。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC \_ 資源 \_ ICC \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-120">應傳遞給 MXDC 未處理之輸出的 ICC 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC \_ 資源 \_ JPEG \_ 縮圖**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-122">應傳遞給 MXDC 未處理之輸出的 JPEG 縮圖。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC \_ 資源 \_ PNG \_ 縮圖**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-124">應該傳遞給 MXDC 未處理之輸出的 PNG 縮圖。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="4b5f6-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ 資源 \_ 上限**</span><span class="sxs-lookup"><span data-stu-id="4b5f6-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="4b5f6-126">驗證的最大資源計數。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b5f6-127">備註</span><span class="sxs-lookup"><span data-stu-id="4b5f6-127">Remarks</span></span>

<span data-ttu-id="4b5f6-128">此列舉主要是用來做為 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](mxdcxpss0pageresource.md)結構的 **dwResourceType** 成員。</span><span class="sxs-lookup"><span data-stu-id="4b5f6-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5f6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b5f6-129">Requirements</span></span>



| <span data-ttu-id="4b5f6-130">需求</span><span class="sxs-lookup"><span data-stu-id="4b5f6-130">Requirement</span></span> | <span data-ttu-id="4b5f6-131">值</span><span class="sxs-lookup"><span data-stu-id="4b5f6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5f6-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b5f6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5f6-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b5f6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4b5f6-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b5f6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5f6-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b5f6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b5f6-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4b5f6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b5f6-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4b5f6-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




