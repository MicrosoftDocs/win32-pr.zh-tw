---
title: 'DPI_AWARENESS_CONTEXT 處理 (windef .h) '
description: 識別視窗的感知內容。
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317276"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="7a694-103">DPI \_ 感知 \_ 內容控制碼</span><span class="sxs-lookup"><span data-stu-id="7a694-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="7a694-104">識別視窗的感知內容。</span><span class="sxs-lookup"><span data-stu-id="7a694-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a694-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a694-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="7a694-106">常數</span><span class="sxs-lookup"><span data-stu-id="7a694-106">Constants</span></span>

<span data-ttu-id="7a694-107">**DPI \_ 感知 \_ 內容未 \_ 察覺**</span><span class="sxs-lookup"><span data-stu-id="7a694-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="7a694-108">不知道 DPI。</span><span class="sxs-lookup"><span data-stu-id="7a694-108">DPI unaware.</span></span> <span data-ttu-id="7a694-109">此視窗不會針對 DPI 變更進行調整，而且一律會假設其比例因數為 100% (96 DPI) 。</span><span class="sxs-lookup"><span data-stu-id="7a694-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="7a694-110">系統會自動以任何其他 DPI 設定來調整它的規模。</span><span class="sxs-lookup"><span data-stu-id="7a694-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="7a694-111">**DPI \_ 感知 \_ 內容 \_ 系統 \_ 感知**</span><span class="sxs-lookup"><span data-stu-id="7a694-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="7a694-112">系統 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7a694-112">System DPI aware.</span></span> <span data-ttu-id="7a694-113">此視窗不會針對 DPI 變更進行調整。</span><span class="sxs-lookup"><span data-stu-id="7a694-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="7a694-114">它會查詢 DPI 一次，並在進程的存留期內使用該值。</span><span class="sxs-lookup"><span data-stu-id="7a694-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="7a694-115">如果 DPI 變更，進程將不會調整為新的 DPI 值。</span><span class="sxs-lookup"><span data-stu-id="7a694-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="7a694-116">當系統值的 DPI 變更時，系統會自動相應增加或減少系統的規模。</span><span class="sxs-lookup"><span data-stu-id="7a694-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="7a694-117">**\_ \_ \_ 感知每個 \_ 監視器 \_ 的 DPI 感知內容**</span><span class="sxs-lookup"><span data-stu-id="7a694-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="7a694-118">每個監視器 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7a694-118">Per monitor DPI aware.</span></span> <span data-ttu-id="7a694-119">此視窗會在建立時檢查 DPI，並在每次 DPI 變更時調整比例因數。</span><span class="sxs-lookup"><span data-stu-id="7a694-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="7a694-120">系統不會自動調整這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="7a694-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="7a694-121">**\_ \_ 每個監視器的 DPI 感知內容 \_ \_ \_ 感知 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="7a694-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="7a694-122">也稱為 **每個監視器 v2**。</span><span class="sxs-lookup"><span data-stu-id="7a694-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="7a694-123">優於原始的個別監視器 DPI 感知模式，可讓應用程式在每個最上層視窗上存取新的 DPI 相關縮放行為。</span><span class="sxs-lookup"><span data-stu-id="7a694-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="7a694-124">在 Windows 10 的建立者更新中提供每個監視器 v2，而且在舊版的作業系統上無法使用。</span><span class="sxs-lookup"><span data-stu-id="7a694-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="7a694-125">引進的其他行為如下：</span><span class="sxs-lookup"><span data-stu-id="7a694-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="7a694-126">**子視窗 DPI 變更通知** -在每個監視器 v2 內容中，整個視窗樹狀結構會在發生的任何 DPI 變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="7a694-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="7a694-127">**縮放非工作區** -所有視窗都會自動以 DPI 敏感性的方式繪製其非工作區。</span><span class="sxs-lookup"><span data-stu-id="7a694-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="7a694-128">不需要呼叫 [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) 。</span><span class="sxs-lookup"><span data-stu-id="7a694-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="7a694-129">**Win32 功能表的調整** -每個監視器 v2 內容中建立的所有 ntuser.man 功能表都會以每個監視器的方式調整。</span><span class="sxs-lookup"><span data-stu-id="7a694-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="7a694-130">**對話方塊縮放** -在每個監視器中建立的 Win32 對話方塊會自動回應 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="7a694-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="7a694-131">**改善 comctl32.dll 控制項的縮放比例** -各種 comctl32.dll 控制項都已改善每個監視器 v2 內容中的 DPI 縮放行為。</span><span class="sxs-lookup"><span data-stu-id="7a694-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="7a694-132">**改善的主題行為** -在每個監視器 v2 視窗的內容中開啟的 UxTheme 控制碼，將會以與該視窗相關聯的 DPI 來運作。</span><span class="sxs-lookup"><span data-stu-id="7a694-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="7a694-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="7a694-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="7a694-134">以 GDI 為基礎的內容改善品質的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7a694-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="7a694-135">這種模式的行為類似于 DPI_AWARENESS_CONTEXT_UNAWARE，但也可讓系統在高 DPI 監視器上顯示視窗時，自動改善文字轉譯品質和其他以 GDI 為基礎的基本類型。</span><span class="sxs-lookup"><span data-stu-id="7a694-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="7a694-136">如需更多詳細資訊，請參閱 [改善以 GDI 為基礎的桌面應用程式中的高 DPI 體驗](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)。</span><span class="sxs-lookup"><span data-stu-id="7a694-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="7a694-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED 于2018年10月的更新中引進 Windows 10 (也稱為1809版) 。</span><span class="sxs-lookup"><span data-stu-id="7a694-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="7a694-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a694-138">Requirements</span></span>

| <span data-ttu-id="7a694-139">需求</span><span class="sxs-lookup"><span data-stu-id="7a694-139">Requirement</span></span> | <span data-ttu-id="7a694-140">值</span><span class="sxs-lookup"><span data-stu-id="7a694-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="7a694-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a694-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7a694-142">Windows 10， \[ 僅限1607版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a694-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7a694-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a694-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7a694-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="7a694-144">None supported</span></span> <br/>  |
| <span data-ttu-id="7a694-145">標頭</span><span class="sxs-lookup"><span data-stu-id="7a694-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a694-146"><dt>windef。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a694-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7a694-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a694-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a694-148">**AreDpiAwarenessCoNtextsEqual**</span><span class="sxs-lookup"><span data-stu-id="7a694-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="7a694-149">**GetAwarenessFromDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-150">**GetDpiFromDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-151">**GetThreadDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-152">**GetWindowDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-153">**IsValidDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-154">**SetProcessDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="7a694-155">**SetThreadDpiAwarenessCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7a694-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
