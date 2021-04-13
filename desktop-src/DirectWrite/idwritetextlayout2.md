---
title: IDWriteTextLayout2 介面
description: 表示經過完整分析和格式化之後的一段文字。 |IDWriteTextLayout2 介面
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- IDWriteTextLayout2 介面直接寫入
- IDWriteTextLayout2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322288"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="3e9fc-106">IDWriteTextLayout2 介面</span><span class="sxs-lookup"><span data-stu-id="3e9fc-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="3e9fc-107">表示經過完整分析和格式化之後的一段文字。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="3e9fc-108">成員</span><span class="sxs-lookup"><span data-stu-id="3e9fc-108">Members</span></span>

<span data-ttu-id="3e9fc-109">**IDWriteTextLayout2** 介面繼承自 [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="3e9fc-110">**IDWriteTextLayout2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e9fc-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="3e9fc-111">方法</span><span class="sxs-lookup"><span data-stu-id="3e9fc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e9fc-112">方法</span><span class="sxs-lookup"><span data-stu-id="3e9fc-112">Methods</span></span>

<span data-ttu-id="3e9fc-113">**IDWriteTextLayout2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="3e9fc-114">方法</span><span class="sxs-lookup"><span data-stu-id="3e9fc-114">Method</span></span>                                                                                | <span data-ttu-id="3e9fc-115">描述</span><span class="sxs-lookup"><span data-stu-id="3e9fc-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e9fc-116">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="3e9fc-117">取得目前的字型 fallback 物件。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="3e9fc-118">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="3e9fc-119">取得最後一行中的最後一個單字是否換行。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="3e9fc-120">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="3e9fc-121">抓取格式化字串的整體計量。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="3e9fc-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="3e9fc-123">取得字元與邊界邊緣的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="3e9fc-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="3e9fc-125">使用垂直閱讀方向時，取得字型的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="3e9fc-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="3e9fc-127">將自訂字型回套用至版面配置。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="3e9fc-128">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="3e9fc-129">設定是否要包裝最後一行的最後一個字組。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="3e9fc-130">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="3e9fc-131">設定字型與邊界邊緣的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="3e9fc-132">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="3e9fc-133">使用垂直閱讀方向時，請設定字型的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="3e9fc-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e9fc-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e9fc-134">Requirements</span></span>



| <span data-ttu-id="3e9fc-135">需求</span><span class="sxs-lookup"><span data-stu-id="3e9fc-135">Requirement</span></span> | <span data-ttu-id="3e9fc-136">值</span><span class="sxs-lookup"><span data-stu-id="3e9fc-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9fc-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e9fc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9fc-138">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e9fc-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="3e9fc-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e9fc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9fc-140">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e9fc-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3e9fc-141">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="3e9fc-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="3e9fc-142">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e9fc-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="3e9fc-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e9fc-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e9fc-144"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e9fc-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3e9fc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3e9fc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e9fc-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e9fc-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3e9fc-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e9fc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9fc-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="3e9fc-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

