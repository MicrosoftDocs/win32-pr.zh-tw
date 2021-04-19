---
title: 'TF_SFT_ 常數 (Ctfutb) '
description: TF \_ SFT \_ \ 常數指定浮動語言列的顯示設定。
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965910"
---
# <a name="tf_sft_-constants"></a><span data-ttu-id="8a584-103">TF \_ SFT \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="8a584-103">TF\_SFT\_\* Constants</span></span>

<span data-ttu-id="8a584-104">\**TF \_ SFT \_ \** _ 常數指定浮動語言列的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="8a584-104">The \**TF\_SFT\_\** _ constants specify display settings of a floating language bar.</span></span>



| <span data-ttu-id="8a584-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="8a584-105">Constant/value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="8a584-106">Description</span><span class="sxs-lookup"><span data-stu-id="8a584-106">Description</span></span>                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <span data-ttu-id="8a584-107"><dt>_ \* TF \_SFT \_ SHOWNORMAL \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-107"><dt>_\*TF\_SFT\_SHOWNORMAL\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                        | <span data-ttu-id="8a584-108">將語言列顯示為浮動視窗。</span><span class="sxs-lookup"><span data-stu-id="8a584-108">Display the language bar as a floating window.</span></span> <span data-ttu-id="8a584-109">這個常數無法與 TF \_ sft \_ DOCK、tf \_ sft \_ 最小化、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數合併使用。</span><span class="sxs-lookup"><span data-stu-id="8a584-109">This constant cannot be combined with the TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span><br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <span data-ttu-id="8a584-110"><dt>**TF \_SFT \_ DOCK**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-110"><dt>**TF\_SFT\_DOCK**</dt> <dt>0x00000002</dt></span></span> </dl>                                                          | <span data-ttu-id="8a584-111">將語言列停駐在自己的工作窗格中。</span><span class="sxs-lookup"><span data-stu-id="8a584-111">Dock the language bar in its own task pane.</span></span> <span data-ttu-id="8a584-112">這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ sft \_ 最小化、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數結合。</span><span class="sxs-lookup"><span data-stu-id="8a584-112">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_MINIMIZED, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span> <span data-ttu-id="8a584-113">僅適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="8a584-113">Available only on Windows XP.</span></span><br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <span data-ttu-id="8a584-114"><dt>**TF \_SFT \_ 最小化**</dt>的 <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-114"><dt>**TF\_SFT\_MINIMIZED**</dt> <dt>0x00000004</dt></span></span> </dl>                                           | <span data-ttu-id="8a584-115">將語言列顯示為系統匣中的單一圖示。</span><span class="sxs-lookup"><span data-stu-id="8a584-115">Display the language bar as a single icon in the system tray.</span></span> <span data-ttu-id="8a584-116">這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、TF \_ sft \_ HIDDEN 或 tf \_ sft \_ DESKBAND 常數結合。</span><span class="sxs-lookup"><span data-stu-id="8a584-116">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_HIDDEN, or TF\_SFT\_DESKBAND constants.</span></span> <span data-ttu-id="8a584-117">在 Windows XP 中，請改用 TF \_ SFT \_ DESKBAND。</span><span class="sxs-lookup"><span data-stu-id="8a584-117">In Windows XP, use TF\_SFT\_DESKBAND instead.</span></span><br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <span data-ttu-id="8a584-118"><dt>**TF \_SFT \_ 隱藏**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-118"><dt>**TF\_SFT\_HIDDEN**</dt> <dt>0x00000008</dt></span></span> </dl>                                                    | <span data-ttu-id="8a584-119">隱藏語言列。</span><span class="sxs-lookup"><span data-stu-id="8a584-119">Hide the language bar.</span></span> <span data-ttu-id="8a584-120">這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、tf \_ sft 的 \_ 最小化或 tf \_ sft \_ DESKBAND 常數結合。</span><span class="sxs-lookup"><span data-stu-id="8a584-120">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, or TF\_SFT\_DESKBAND constants.</span></span><br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <span data-ttu-id="8a584-121"><dt>**TF \_SFT \_ NOTRANSPARENCY**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-121"><dt>**TF\_SFT\_NOTRANSPARENCY**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="8a584-122">讓語言行不透明。</span><span class="sxs-lookup"><span data-stu-id="8a584-122">Make the language bar opaque.</span></span><br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <span data-ttu-id="8a584-123"><dt>**TF \_SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-123"><dt>**TF\_SFT\_LOWTRANSPARENCY**</dt> <dt>0x00000020</dt></span></span> </dl>                         | <span data-ttu-id="8a584-124">將語言列設為部分透明。</span><span class="sxs-lookup"><span data-stu-id="8a584-124">Make the language bar partially transparent.</span></span> <span data-ttu-id="8a584-125">僅適用于 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8a584-125">Available only on Windows 2000 or later.</span></span><br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <span data-ttu-id="8a584-126"><dt>**TF \_SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-126"><dt>**TF\_SFT\_HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt></span></span> </dl>                      | <span data-ttu-id="8a584-127">將語言列設為高度透明。</span><span class="sxs-lookup"><span data-stu-id="8a584-127">Make the language bar highly transparent.</span></span> <span data-ttu-id="8a584-128">僅適用于 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8a584-128">Available only on Windows 2000 or later.</span></span><br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <span data-ttu-id="8a584-129"><dt>**TF \_SFT \_ 標籤**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-129"><dt>**TF\_SFT\_LABELS**</dt> <dt>0x00000080</dt></span></span> </dl>                                                    | <span data-ttu-id="8a584-130">顯示語言列圖示旁邊的文字標籤。</span><span class="sxs-lookup"><span data-stu-id="8a584-130">Display text labels next to language bar icons.</span></span><br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <span data-ttu-id="8a584-131"><dt>**TF \_SFT \_ NOLABELS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-131"><dt>**TF\_SFT\_NOLABELS**</dt> <dt>0x00000100</dt></span></span> </dl>                                              | <span data-ttu-id="8a584-132">隱藏語言橫條圖示文字標籤。</span><span class="sxs-lookup"><span data-stu-id="8a584-132">Hide language bar icon text labels.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <span data-ttu-id="8a584-133"><dt>**TF \_SFT \_ EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-133"><dt>**TF\_SFT\_EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt></span></span> </dl>       | <span data-ttu-id="8a584-134">當語言列最小化時，在工作列上顯示文字服務圖示。</span><span class="sxs-lookup"><span data-stu-id="8a584-134">Display text service icons on the taskbar when the language bar is minimized.</span></span><br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <span data-ttu-id="8a584-135"><dt>**TF \_SFT \_ NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-135"><dt>**TF\_SFT\_NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="8a584-136">當語言列最小化時，隱藏工作列上的文字服務圖示。</span><span class="sxs-lookup"><span data-stu-id="8a584-136">Hide text service icons on the taskbar when the language bar is minimized.</span></span><br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <span data-ttu-id="8a584-137"><dt>**TF \_SFT \_ DESKBAND**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-137"><dt>**TF\_SFT\_DESKBAND**</dt> <dt>0x00000800</dt></span></span> </dl>                                              | <span data-ttu-id="8a584-138">將語言列停駐于系統工作列的 righthand 結尾 (系統匣/時鐘) 的正下方。</span><span class="sxs-lookup"><span data-stu-id="8a584-138">Dock the language bar in the righthand end of the system task bar (immediately left of the system tray/clock).</span></span> <span data-ttu-id="8a584-139">這個常數無法與 TF \_ sft \_ SHOWNORMAL、tf \_ SFT \_ DOCK、tf \_ sft 的 \_ 最小化，或 tf \_ sft \_ 隱藏的常數合併。</span><span class="sxs-lookup"><span data-stu-id="8a584-139">This constant cannot be combined with the TF\_SFT\_SHOWNORMAL, TF\_SFT\_DOCK, TF\_SFT\_MINIMIZED, or TF\_SFT\_HIDDEN constants.</span></span> <span data-ttu-id="8a584-140">僅適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="8a584-140">Available only on Windows XP.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8a584-141">備註</span><span class="sxs-lookup"><span data-stu-id="8a584-141">Remarks</span></span>

<span data-ttu-id="8a584-142">[ITfLangBarMgr：： ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)方法會設定一或多個常數的邏輯 **OR** 運算結果，以指定語言列專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="8a584-142">The [ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) method sets the result of a logical **OR** operation on one or more of these constants to specify the attributes of the language bar item.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a584-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a584-143">Requirements</span></span>



| <span data-ttu-id="8a584-144">需求</span><span class="sxs-lookup"><span data-stu-id="8a584-144">Requirement</span></span> | <span data-ttu-id="8a584-145">值</span><span class="sxs-lookup"><span data-stu-id="8a584-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a584-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a584-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8a584-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a584-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8a584-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a584-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8a584-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a584-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a584-150">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a584-150">Redistributable</span></span><br/>          | <span data-ttu-id="8a584-151">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="8a584-151">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="8a584-152">標頭</span><span class="sxs-lookup"><span data-stu-id="8a584-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a584-153"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-153"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a584-154">Idl</span><span class="sxs-lookup"><span data-stu-id="8a584-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a584-155"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a584-155"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a584-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a584-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a584-157">ITfLangBarMgr::ShowFloating</span><span class="sxs-lookup"><span data-stu-id="8a584-157">ITfLangBarMgr::ShowFloating</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





