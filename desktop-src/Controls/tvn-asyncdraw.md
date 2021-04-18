---
title: 'TVN_ASYNCDRAW (Commctrl 的通知碼) '
description: 當圖示或重迭的繪圖失敗時，由樹狀檢視控制項傳送到其父系。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965527"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="51f86-105">IZDEBSKI \_ ASYNCDRAW 通知碼</span><span class="sxs-lookup"><span data-stu-id="51f86-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="51f86-106">當圖示或重迭的繪圖失敗時，由樹狀檢視控制項傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="51f86-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="51f86-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="51f86-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="51f86-108">參數</span><span class="sxs-lookup"><span data-stu-id="51f86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f86-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51f86-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51f86-110">[**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="51f86-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="51f86-111">**NMTVASYNCDRAW** 結構包含繪製失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="51f86-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f86-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="51f86-112">Return value</span></span>

<span data-ttu-id="51f86-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="51f86-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f86-114">備註</span><span class="sxs-lookup"><span data-stu-id="51f86-114">Remarks</span></span>

<span data-ttu-id="51f86-115">樹狀檢視控制項必須有 [**tv \_ EX \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) 延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="51f86-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="51f86-116">請注意，這相當於清單視圖的 LVN \_ ASYNCDRAWN 旗標及其對應的樣式。</span><span class="sxs-lookup"><span data-stu-id="51f86-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="51f86-117">此控制項不會以非同步方式繪製。</span><span class="sxs-lookup"><span data-stu-id="51f86-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="51f86-118">在樹狀結構中，如果影像無法使用，則會在樹狀檢視控制項不同步將影像解壓縮的內容中使用非同步。</span><span class="sxs-lookup"><span data-stu-id="51f86-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="51f86-119"> (比方說，如果樹狀檢視控制項使用的是稀疏影像清單，則可能無法使用影像，因為影像可能會被卸載。 ) 相反地，當影像無法使用時，控制項會以 NMTVASYNCDRAW 結構傳送父代 IZDEBSKI ASYNCDRAW 通知，以同步方式要求父項要採取的動作 \_ 。 [](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw)</span><span class="sxs-lookup"><span data-stu-id="51f86-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="51f86-120">此結構的 **hr** 成員描述控制項繪製失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="51f86-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="51f86-121">電子暫止的 **hr** 結果 \_ 表示映射不會出現在所有 (映射需要解壓縮) 。</span><span class="sxs-lookup"><span data-stu-id="51f86-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="51f86-122">Success 表示影像存在，但不是必要的影像品質。</span><span class="sxs-lookup"><span data-stu-id="51f86-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="51f86-123">父系會設定結構的 **dwRetFlags** 成員，以通知控制項如何繼續。</span><span class="sxs-lookup"><span data-stu-id="51f86-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="51f86-124">例如，父代可能會傳回 **iRetImageIndex** 成員中的另一個影像，以便繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="51f86-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="51f86-125">在此情況下，父代會將 **dwRetFlags** 成員設定為 ADRF \_ DRAWIMAGE。</span><span class="sxs-lookup"><span data-stu-id="51f86-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="51f86-126">如果控制項找不到傳回的影像，但控制項可能會傳送另一個 IZDEBSKI \_ ASYNCDRAW 通知。</span><span class="sxs-lookup"><span data-stu-id="51f86-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="51f86-127">如果映射無法使用，則非同步概念是允許父系在背景進行解壓縮，讓解壓縮不會封鎖 UI 執行緒，也就是控制項所在的執行緒。</span><span class="sxs-lookup"><span data-stu-id="51f86-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="51f86-128">父系可能會將 ADRF \_ DRAWNOTHING 傳回給控制項，然後啟動背景執行緒以將圖示解壓縮。</span><span class="sxs-lookup"><span data-stu-id="51f86-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="51f86-129">一旦解壓縮之後，父系可能會在 treeview 控制項中使用宏 [**treeview \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)來設定圖示。</span><span class="sxs-lookup"><span data-stu-id="51f86-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="51f86-130">這會導致樹狀檢視使專案失效，最後使用影像清單中已解壓縮的影像重新繪製它。</span><span class="sxs-lookup"><span data-stu-id="51f86-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="51f86-131">下列程式碼範例（可作為較大程式的一部分）會顯示父代如何在控制項中處理此通知中的兩個可能傳回碼，以及決定控制項應採取的動作。</span><span class="sxs-lookup"><span data-stu-id="51f86-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="51f86-132">未顯示設定 **dwRetFlags** 。</span><span class="sxs-lookup"><span data-stu-id="51f86-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="51f86-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="51f86-133">Requirements</span></span>



| <span data-ttu-id="51f86-134">需求</span><span class="sxs-lookup"><span data-stu-id="51f86-134">Requirement</span></span> | <span data-ttu-id="51f86-135">值</span><span class="sxs-lookup"><span data-stu-id="51f86-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51f86-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51f86-136">Minimum supported client</span></span><br/> | <span data-ttu-id="51f86-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51f86-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51f86-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51f86-138">Minimum supported server</span></span><br/> | <span data-ttu-id="51f86-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51f86-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51f86-140">標頭</span><span class="sxs-lookup"><span data-stu-id="51f86-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f86-141"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="51f86-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





