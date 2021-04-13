---
title: 新增和修改事件
description: 新增和修改事件
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301444"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="54849-109">新增和修改事件</span><span class="sxs-lookup"><span data-stu-id="54849-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="54849-110">您必須提供 \_ 當使用者變更屬性頁編輯方塊中的文字時，所發生的 EN 變更事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="54849-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="54849-111">這些事件處理常式具有只在 [屬性頁] **對話方塊中啟用** [套用] 的簡單執行。</span><span class="sxs-lookup"><span data-stu-id="54849-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="54849-112">修改縮放因數事件處理常式</span><span class="sxs-lookup"><span data-stu-id="54849-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="54849-113">您必須變更外掛程式嚮導為縮放比例編輯方塊提供的現有事件處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="54849-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="54849-114">您應該在三個位置中，將名稱從 OnChangeScale 變更為 OnChangeDelay：</span><span class="sxs-lookup"><span data-stu-id="54849-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="54849-115">在 EchoPropPage 中，變更 message map 宏區段中的名稱。</span><span class="sxs-lookup"><span data-stu-id="54849-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="54849-116">以下列程式碼取代將縮放比例變更事件對應至 OnChangeScale 方法的程式程式碼：</span><span class="sxs-lookup"><span data-stu-id="54849-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="54849-117">在 EchoPropPage 中，變更原型為 OnChangeScale 函式之程式程式碼中的名稱：</span><span class="sxs-lookup"><span data-stu-id="54849-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="54849-118">在 EchoPropPage .cpp 中，變更函式標頭中的名稱：</span><span class="sxs-lookup"><span data-stu-id="54849-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="54849-119">新增潮濕混合事件處理常式</span><span class="sxs-lookup"><span data-stu-id="54849-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="54849-120">您可以輕鬆地加入 \_ 附加至 IDC \_ WETMIX 編輯方塊控制項之 EN 變更事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="54849-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="54849-121">從對話方塊資源編輯器：</span><span class="sxs-lookup"><span data-stu-id="54849-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="54849-122">以滑鼠右鍵按一下 IDC \_ WETMIX 編輯方塊，然後選擇 [ **事件**]。</span><span class="sxs-lookup"><span data-stu-id="54849-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="54849-123">[新的 Windows 訊息和事件處理常式] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="54849-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="54849-124">在 [ **要處理的類別或物件** ] 方塊中，按一下 [IDC WETMIX] 編輯方塊資源的名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="54849-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="54849-125">在 [ **新的 Windows 訊息/事件** ] 方塊中，按一下 [EN \_ 變更] 以選取它。</span><span class="sxs-lookup"><span data-stu-id="54849-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="54849-126">按一下 [ **加入處理常式**]。</span><span class="sxs-lookup"><span data-stu-id="54849-126">Click **Add Handler**.</span></span> <span data-ttu-id="54849-127">[加入成員函數] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="54849-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="54849-128">在 [ **成員** 函式名稱] 方塊中，輸入名稱 OnChangeWetmix。</span><span class="sxs-lookup"><span data-stu-id="54849-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="54849-129">按一下 **[確定** ] 以關閉 [加入成員函式] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="54849-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="54849-130">按一下 **[確定** ] 返回對話方塊資源編輯器。</span><span class="sxs-lookup"><span data-stu-id="54849-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="54849-131">Visual C++ 會自動將訊息對應和事件處理常式函式的程式碼加入至 EchoPropPage .h。</span><span class="sxs-lookup"><span data-stu-id="54849-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="54849-132">它所插入的程式碼會提供 TODO 批註，您可以在其中新增函式標頭中的實作為。</span><span class="sxs-lookup"><span data-stu-id="54849-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="54849-133">這與 Windows Media Player 外掛程式 Wizard 範例程式碼所使用的樣式稍有不同，但卻是可接受的。</span><span class="sxs-lookup"><span data-stu-id="54849-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="54849-134">您是否想要在標頭檔中撰寫您的執行，或將其移至 EchoPropPage。 .cpp 由您決定。</span><span class="sxs-lookup"><span data-stu-id="54849-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="54849-135">無論是哪一種情況，執行都只需要一行額外的程式碼，即可在 [屬性頁] 對話方塊 **中啟用 [** 套用]。</span><span class="sxs-lookup"><span data-stu-id="54849-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="54849-136">將這行程式碼插入函式傳回的行之前：</span><span class="sxs-lookup"><span data-stu-id="54849-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="54849-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="54849-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54849-138">**修改 Echo 範例屬性頁**</span><span class="sxs-lookup"><span data-stu-id="54849-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




