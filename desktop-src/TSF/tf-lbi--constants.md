---
title: 'TF_LBI_ 常數 (Ctfutb) '
description: TF \_ LBI \_ \ 常數會與 ITfLangBarItemSink OnUpdate 方法搭配使用，以指出已變更的語言列專案。
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966302"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="8abe4-103">TF \_ LBI \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="8abe4-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="8abe4-104">\**TF \_ LBI \_ \** _ 常數可與 [ITfLangBarItemSink：： OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)方法搭配使用，以指出已變更的語言列專案。</span><span class="sxs-lookup"><span data-stu-id="8abe4-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="8abe4-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="8abe4-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="8abe4-106">Description</span><span class="sxs-lookup"><span data-stu-id="8abe4-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="8abe4-107"><dt>_ \* TF \_LBI \_ 圖示 \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="8abe4-108">專案的圖示已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-108">The icon of the item has changed.</span></span> <span data-ttu-id="8abe4-109">Language bar 會呼叫 [ITfLangBarItemButton：： GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) 來回應此通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="8abe4-110"><dt>**TF \_LBI \_ 文本**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="8abe4-111">按鈕或點陣圖按鈕專案的文字已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="8abe4-112">語言列會呼叫 [ITfLangBarItemButton：： GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) 或 [ITfLangBarItemBitmapButton：： GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)（視何者而定），以回應這項通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="8abe4-113"><dt>**TF \_LBI \_ 工具提示**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="8abe4-114">專案的工具提示文字已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="8abe4-115">Language bar 會呼叫 [ITfLangBarItem：： GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) 來回應此通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="8abe4-116"><dt>**TF \_LBI \_ 點陣圖**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="8abe4-117">點陣圖或點陣圖按鈕專案的點陣圖已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="8abe4-118">語言列會呼叫 [ITfLangBarItemBitmap：:D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) 或 [ITfLangBarItemBitmapButton：:D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap)（視何者而定），以回應這項通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="8abe4-119"><dt>**TF \_LBI \_ 氣球**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="8abe4-120">氣球專案的資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-120">The information for a balloon item changed.</span></span> <span data-ttu-id="8abe4-121">Language bar 會呼叫 [ITfLangBarItemBalloon：： GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) 來回應此通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="8abe4-122"><dt>**TF \_LBI \_ 狀態**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="8abe4-123">專案狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="8abe4-123">The item status changed.</span></span> <span data-ttu-id="8abe4-124">Language bar 會呼叫 [ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) 來回應此通知。</span><span class="sxs-lookup"><span data-stu-id="8abe4-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="8abe4-125"><dt>**TF \_LBI \_ BMPALL**</dt> <dt>TF \_ LBI \_ 點陣圖 \| TF \_ LBI \_ 工具提示</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="8abe4-126">結合 TF \_ LBI \_ BITMAP 和 tf \_ LBI \_ 工具提示。</span><span class="sxs-lookup"><span data-stu-id="8abe4-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="8abe4-127"><dt>**TF \_LBI \_ BMPBTNALL**</dt> <dt>TF \_ LBI \_ BITMAP \| TF \_ LBI \_ TEXT \| TF \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="8abe4-128">結合 TF \_ LBI \_ BITMAP、tf \_ LBI \_ TEXT 和 tf \_ LBI \_ 工具提示。</span><span class="sxs-lookup"><span data-stu-id="8abe4-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="8abe4-129"><dt>**TF \_LBI \_ BTNALL**</dt> <dt>TF \_ LBI \_ 圖示 \| TF \_ LBI \_ TEXT \| TF \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="8abe4-130">結合 TF \_ LBI \_ 圖示、tf \_ LBI \_ TEXT 和 tf \_ LBI \_ 工具提示。</span><span class="sxs-lookup"><span data-stu-id="8abe4-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="8abe4-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="8abe4-131">Requirements</span></span>



| <span data-ttu-id="8abe4-132">需求</span><span class="sxs-lookup"><span data-stu-id="8abe4-132">Requirement</span></span> | <span data-ttu-id="8abe4-133">值</span><span class="sxs-lookup"><span data-stu-id="8abe4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8abe4-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8abe4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8abe4-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8abe4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8abe4-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8abe4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8abe4-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8abe4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8abe4-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8abe4-138">Redistributable</span></span><br/>          | <span data-ttu-id="8abe4-139">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="8abe4-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="8abe4-140">標頭</span><span class="sxs-lookup"><span data-stu-id="8abe4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8abe4-141"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8abe4-142">Idl</span><span class="sxs-lookup"><span data-stu-id="8abe4-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8abe4-143"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8abe4-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8abe4-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8abe4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8abe4-145">ITfLangBarItemSink：： OnUpdate</span><span class="sxs-lookup"><span data-stu-id="8abe4-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





