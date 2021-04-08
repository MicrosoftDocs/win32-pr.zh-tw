---
description: 影像意圖常數會指定影像所代表的資料類型。
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: '影像意圖常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943587"
---
# <a name="image-intent-constants"></a><span data-ttu-id="00851-103">影像意圖常數</span><span class="sxs-lookup"><span data-stu-id="00851-103">Image Intent Constants</span></span>

<span data-ttu-id="00851-104">影像意圖常數會指定影像所代表的資料類型。</span><span class="sxs-lookup"><span data-stu-id="00851-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="00851-105">[ [**WIA \_ ip 的 \_ 當前 \_ 意圖**](-wia-wiaitempropscanneritem.md) 掃描器] 屬性會使用這些旗標。</span><span class="sxs-lookup"><span data-stu-id="00851-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="00851-106">若要提供意圖，請使用 OR 運算子結合預期的影像類型旗標與預期的大小/品質旗標。</span><span class="sxs-lookup"><span data-stu-id="00851-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="00851-107">WIA \_ 意圖「 \_ 無」不應與任何其他旗標合併。</span><span class="sxs-lookup"><span data-stu-id="00851-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="00851-108">請注意，影像不能同時為灰階和彩色。</span><span class="sxs-lookup"><span data-stu-id="00851-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="00851-109">以下是有效的影像意圖常數：</span><span class="sxs-lookup"><span data-stu-id="00851-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="00851-110">預定的影像類型旗標</span><span class="sxs-lookup"><span data-stu-id="00851-110">Intended image type flags</span></span>           | <span data-ttu-id="00851-111">Description</span><span class="sxs-lookup"><span data-stu-id="00851-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="00851-112">WIA \_ 意圖 \_ 無</span><span class="sxs-lookup"><span data-stu-id="00851-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="00851-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="00851-113">Default value.</span></span> <span data-ttu-id="00851-114">請勿預設設定任何屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="00851-115">WIA \_ 意圖 \_ 影像 \_ 類型 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="00851-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="00851-116">色彩內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="00851-117">WIA \_ 意圖 \_ 影像 \_ 類型 \_ 灰階</span><span class="sxs-lookup"><span data-stu-id="00851-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="00851-118">灰階內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="00851-119">WIA \_ 意圖 \_ 影像 \_ 類型 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="00851-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="00851-120">文字內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="00851-121">WIA \_ 意圖 \_ 影像 \_ 類型 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="00851-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="00851-122">所有影像類型旗標的遮罩。</span><span class="sxs-lookup"><span data-stu-id="00851-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="00851-123">預定的影像大小/品質旗標</span><span class="sxs-lookup"><span data-stu-id="00851-123">Intended image size/quality flags</span></span> | <span data-ttu-id="00851-124">Description</span><span class="sxs-lookup"><span data-stu-id="00851-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="00851-125">WIA \_ 意圖 \_ 最小化 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="00851-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="00851-126">用來將影像大小降至最低的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="00851-127">WIA \_ 意圖 \_ 最大化 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="00851-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="00851-128">將影像品質最大化的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="00851-129">WIA \_ 意圖 \_ 大小 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="00851-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="00851-130">所有大小/品質旗標的遮罩。</span><span class="sxs-lookup"><span data-stu-id="00851-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="00851-131">WIA \_ 意圖 \_ 最佳 \_ 預覽</span><span class="sxs-lookup"><span data-stu-id="00851-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="00851-132">指定最佳品質預覽。</span><span class="sxs-lookup"><span data-stu-id="00851-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="00851-133">下列清單顯示 C/c + + 常數名稱，後面接著以括弧括住的對應名稱（用於腳本處理）。</span><span class="sxs-lookup"><span data-stu-id="00851-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="00851-134">腳本名稱是來自 WiaIntent 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="00851-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="00851-135">請注意，並非所有常數都可透過腳本來使用。</span><span class="sxs-lookup"><span data-stu-id="00851-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="00851-136">常數/值</span><span class="sxs-lookup"><span data-stu-id="00851-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="00851-137">Description</span><span class="sxs-lookup"><span data-stu-id="00851-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="00851-138"><dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 色彩**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="00851-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="00851-139">色彩內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="00851-140"><dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 灰階**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="00851-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="00851-141">灰階內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="00851-142"><dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 文字**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="00851-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="00851-143">文字內容的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="00851-144"><dt>**WIA \_意圖 \_ 最小化 \_ 大小**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="00851-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="00851-145">用來將影像大小降至最低的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="00851-146"><dt>**WIA \_意圖 \_ 最大化 \_ 品質**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="00851-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="00851-147">將影像品質最大化的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="00851-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="00851-148"><dt>**WIA \_意圖 \_ 最適合 \_ 預覽**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="00851-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="00851-149">指定最佳品質預覽。</span><span class="sxs-lookup"><span data-stu-id="00851-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="00851-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="00851-150">Requirements</span></span>



| <span data-ttu-id="00851-151">需求</span><span class="sxs-lookup"><span data-stu-id="00851-151">Requirement</span></span> | <span data-ttu-id="00851-152">值</span><span class="sxs-lookup"><span data-stu-id="00851-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00851-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00851-153">Minimum supported client</span></span><br/> | <span data-ttu-id="00851-154">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00851-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="00851-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00851-155">Minimum supported server</span></span><br/> | <span data-ttu-id="00851-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00851-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00851-157">標頭</span><span class="sxs-lookup"><span data-stu-id="00851-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="00851-158"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="00851-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




