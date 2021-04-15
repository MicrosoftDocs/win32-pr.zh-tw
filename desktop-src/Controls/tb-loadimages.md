---
title: 'TB_LOADIMAGES 訊息 (Commctrl .h) '
description: 將系統定義的按鈕影像載入工具列控制項的影像清單。
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES message Windows 控制項
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466224"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="9db61-104">TB \_ LOADIMAGES 訊息</span><span class="sxs-lookup"><span data-stu-id="9db61-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="9db61-105">將系統定義的按鈕影像載入工具列控制項的影像清單。</span><span class="sxs-lookup"><span data-stu-id="9db61-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="9db61-106">參數</span><span class="sxs-lookup"><span data-stu-id="9db61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9db61-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9db61-108">系統定義之按鈕影像清單的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9db61-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="9db61-109">這個參數可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9db61-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="9db61-110">值</span><span class="sxs-lookup"><span data-stu-id="9db61-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="9db61-111">意義</span><span class="sxs-lookup"><span data-stu-id="9db61-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="9db61-112"><dt>**.IDB \_ >HIST \_ 大型 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="9db61-113">以大尺寸 Windows 檔案總管點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="9db61-114"><dt>**.IDB \_ >HIST \_ 小型 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="9db61-115">以小規模 Windows 檔案總管點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="9db61-116"><dt>**.IDB \_ STD \_ 大型 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="9db61-117">大小較大的標準點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="9db61-118"><dt>**.IDB \_ STD \_ SMALL \_ COLOR**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="9db61-119">小型的標準點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="9db61-120"><dt>**.IDB \_ 視圖 \_ 大型 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="9db61-121">以大尺寸觀看點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="9db61-122"><dt>**.IDB \_ 視圖 \_ 小 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="9db61-123">以小尺寸觀看點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="9db61-124"><dt>**\_>HIST \_ 一般的 .IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="9db61-125">Windows 檔案總管處於正常狀態的移動按鈕和我的最愛點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="9db61-126"><dt>**\_>HIST \_ 熱的 .IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="9db61-127">以作用中狀態 Windows 檔案總管行進按鈕和我的最愛點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="9db61-128"><dt>**\_ \_ 已停用 .IDB >HIST**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="9db61-129">Windows 檔案總管移動按鈕和 [我的最愛] 點陣圖處於停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9db61-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="9db61-130"><dt>**已 \_ 按下的 .IDB >HIST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="9db61-131">Windows 檔案總管按下狀態下的移動按鈕和我的最愛點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9db61-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="9db61-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9db61-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9db61-133">實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="9db61-133">Instance handle.</span></span> <span data-ttu-id="9db61-134">此參數必須設定為 HINST \_ COMMCTRL。</span><span class="sxs-lookup"><span data-stu-id="9db61-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db61-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="9db61-135">Return value</span></span>

<span data-ttu-id="9db61-136">影像清單中的影像計數。</span><span class="sxs-lookup"><span data-stu-id="9db61-136">The count of images in the image list.</span></span> <span data-ttu-id="9db61-137">如果工具列沒有影像清單，或現有的影像清單是空的，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="9db61-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db61-138">備註</span><span class="sxs-lookup"><span data-stu-id="9db61-138">Remarks</span></span>

<span data-ttu-id="9db61-139">當您在傳送 [**TB \_ ADDBUTTONS**](tb-addbuttons.md)訊息之前準備 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構時，必須使用適當的映射索引值。</span><span class="sxs-lookup"><span data-stu-id="9db61-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="9db61-140">如需這些預設點陣圖的影像索引值清單，請參閱 [工具列標準按鈕影像索引值](toolbar-standard-button-image-index-values.md)。</span><span class="sxs-lookup"><span data-stu-id="9db61-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9db61-141">範例</span><span class="sxs-lookup"><span data-stu-id="9db61-141">Examples</span></span>

<span data-ttu-id="9db61-142">下列範例程式碼會載入系統標準的小型色彩影像。</span><span class="sxs-lookup"><span data-stu-id="9db61-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="9db61-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="9db61-143">Requirements</span></span>



| <span data-ttu-id="9db61-144">需求</span><span class="sxs-lookup"><span data-stu-id="9db61-144">Requirement</span></span> | <span data-ttu-id="9db61-145">值</span><span class="sxs-lookup"><span data-stu-id="9db61-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9db61-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9db61-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9db61-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9db61-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9db61-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9db61-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9db61-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9db61-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9db61-150">標頭</span><span class="sxs-lookup"><span data-stu-id="9db61-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db61-151"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9db61-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db61-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9db61-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db61-153">**TB \_ ADDBITMAP**</span><span class="sxs-lookup"><span data-stu-id="9db61-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





