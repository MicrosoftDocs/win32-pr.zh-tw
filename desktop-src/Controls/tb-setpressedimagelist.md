---
title: 'TB_SETPRESSEDIMAGELIST 訊息 (Commctrl .h) '
description: 設定工具列用來顯示處於已按下狀態之按鈕的影像清單。
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- TB_SETPRESSEDIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509488"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="c5964-104">TB \_ SETPRESSEDIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="c5964-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="c5964-105">設定工具列用來顯示處於已按下狀態之按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5964-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5964-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5964-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5964-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5964-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5964-108">影像清單的索引。</span><span class="sxs-lookup"><span data-stu-id="c5964-108">The index of the image list.</span></span> <span data-ttu-id="c5964-109">如果您只使用一個影像清單，請將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="c5964-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="c5964-110">如需使用多個影像清單的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c5964-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="c5964-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5964-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5964-112">要設定之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5964-112">Handle to the image list to set.</span></span> <span data-ttu-id="c5964-113">如果此參數為 **Null**，則不會在按鈕中顯示任何影像。</span><span class="sxs-lookup"><span data-stu-id="c5964-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5964-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5964-114">Return value</span></span>

<span data-ttu-id="c5964-115">傳回影像清單的控制碼，此控制碼先前可用來顯示其按下狀態下的按鈕，如果先前未設定這類影像清單，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c5964-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5964-116">備註</span><span class="sxs-lookup"><span data-stu-id="c5964-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5964-117">您的應用程式會負責在工具列損毀之後釋放影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5964-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="c5964-118">**Tb 的 \_ SETPRESSEDIMAGELIST** 訊息無法與 [**tb \_ ADDBITMAP**](tb-addbitmap.md)結合。</span><span class="sxs-lookup"><span data-stu-id="c5964-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="c5964-119">它也不能與以 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)建立的工具列搭配使用，它會在內部呼叫 **TB 的 \_ ADDBITMAP** 。</span><span class="sxs-lookup"><span data-stu-id="c5964-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="c5964-120">當您使用 **CreateToolbarEx** 建立工具列或使用 **TB \_ ADDBITMAP** 來加入影像時，工具列會在內部管理影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5964-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="c5964-121">嘗試以 **TB \_ SETPRESSEDIMAGELIST** 進行修改，會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="c5964-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="c5964-122">按鈕影像不需要來自相同的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5964-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="c5964-123">若要針對您的工具列按鈕影像使用多個影像清單：</span><span class="sxs-lookup"><span data-stu-id="c5964-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="c5964-124">藉由使用 *wParam* 將 [**CCM \_ SETVERSION**](ccm-setversion.md)訊息傳送給工具列控制項，以啟用多個影像清單， () 設定為5的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c5964-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="c5964-125">針對您想要使用的每個影像清單，將 [工具列] 控制項傳送至 [ **TB] \_ SETPRESSEDIMAGELIST** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c5964-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="c5964-126">將 *wParam* 設定為將用來識別清單的應用程式定義 *wParam* 值。</span><span class="sxs-lookup"><span data-stu-id="c5964-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="c5964-127">將 *lParam* 設定為清單的 HIMAGELIST 控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5964-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="c5964-128">針對每個按鈕，將按鈕 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iBitmap** 成員設定為 MAKELONG (*iIndex*， *iImageID*) 。</span><span class="sxs-lookup"><span data-stu-id="c5964-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="c5964-129">*IImageID* 值是在步驟2中定義的適當影像清單的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5964-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="c5964-130">*IIndex* 值是該清單中特定影像的索引。</span><span class="sxs-lookup"><span data-stu-id="c5964-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="c5964-131">藉由將工具列控制項傳送至 TB 的 [**\_ ADDBUTTONS**](tb-addbuttons.md) 訊息來新增按鈕。</span><span class="sxs-lookup"><span data-stu-id="c5964-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="c5964-132">下列程式碼片段說明如何將五個按鈕加入至工具列，其中包含三個不同影像清單中的影像。</span><span class="sxs-lookup"><span data-stu-id="c5964-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="c5964-133">對多個映射清單的支援會透過 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息啟用。</span><span class="sxs-lookup"><span data-stu-id="c5964-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="c5964-134">然後，會設定並指派識別碼為0-2 的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5964-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="c5964-135">按鈕是從影像清單中指派影像，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5964-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="c5964-136">按鈕0是來自影像清單零 (ahim \[ 0 \]) 索引為1。</span><span class="sxs-lookup"><span data-stu-id="c5964-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="c5964-137">按鈕1是來自影像清單一 (ahim \[ 1 \]) 索引為1。</span><span class="sxs-lookup"><span data-stu-id="c5964-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="c5964-138">按鈕2是來自影像清單兩 (ahim \[ 2 \]) 索引為1。</span><span class="sxs-lookup"><span data-stu-id="c5964-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="c5964-139">按鈕3是來自影像清單零 (ahim \[ 0 \]) ，索引為2。</span><span class="sxs-lookup"><span data-stu-id="c5964-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="c5964-140">按鈕4來自 [影像清單 1] (ahim \[ 1 \]) 索引為3。</span><span class="sxs-lookup"><span data-stu-id="c5964-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="c5964-141">最後，按鈕會新增至具有 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 訊息的工具列控制項。</span><span class="sxs-lookup"><span data-stu-id="c5964-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="c5964-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5964-142">Requirements</span></span>



| <span data-ttu-id="c5964-143">需求</span><span class="sxs-lookup"><span data-stu-id="c5964-143">Requirement</span></span> | <span data-ttu-id="c5964-144">值</span><span class="sxs-lookup"><span data-stu-id="c5964-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5964-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5964-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c5964-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5964-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5964-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5964-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c5964-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5964-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5964-149">標頭</span><span class="sxs-lookup"><span data-stu-id="c5964-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5964-150"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5964-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5964-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5964-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5964-152">**參考**</span><span class="sxs-lookup"><span data-stu-id="c5964-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5964-153">**TB \_ GETPRESSEDIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="c5964-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="c5964-154">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="c5964-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c5964-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5964-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

