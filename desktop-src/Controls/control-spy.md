---
title: 控制 Spy 2.0 版
description: Control Spy 是一種工具，可協助開發人員瞭解一般控制項如何將樣式套用至這些控制項，以及它們如何回應訊息和通知。
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024260"
---
# <a name="control-spy-v20"></a><span data-ttu-id="2be7a-103">控制 Spy 2.0 版</span><span class="sxs-lookup"><span data-stu-id="2be7a-103">Control Spy v2.0</span></span>

<span data-ttu-id="2be7a-104">Control Spy 是協助開發人員瞭解通用控制項的工具：如何將樣式套用至這些控制項，以及它們如何回應訊息和通知。</span><span class="sxs-lookup"><span data-stu-id="2be7a-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="2be7a-105">您可以使用 Control Spy 來立即查看不同的樣式如何影響每個控制項的行為和外觀，也可以透過傳送訊息來變更每個控制項的狀態。</span><span class="sxs-lookup"><span data-stu-id="2be7a-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="2be7a-106">有兩個版本的 Control Spy 可供使用，一個用於 [Comctl32.dll 5.X 版](common-control-versions.md) ，另一個用於 Comctl32.dll 6.0 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="2be7a-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="2be7a-107">ControlSpyV6.exe 有內建的應用程式資訊清單，因此它會使用較新的主題控制項。</span><span class="sxs-lookup"><span data-stu-id="2be7a-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="2be7a-108">ControlSpyV5.exe 沒有這個資訊清單，因此預設為較舊的版本。</span><span class="sxs-lookup"><span data-stu-id="2be7a-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="2be7a-109">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="2be7a-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2be7a-110">概觀</span><span class="sxs-lookup"><span data-stu-id="2be7a-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="2be7a-111">樣式</span><span class="sxs-lookup"><span data-stu-id="2be7a-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="2be7a-112">訊息</span><span class="sxs-lookup"><span data-stu-id="2be7a-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="2be7a-113">大小/色彩</span><span class="sxs-lookup"><span data-stu-id="2be7a-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="2be7a-114">哪裡可以取得 Control Spy</span><span class="sxs-lookup"><span data-stu-id="2be7a-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="2be7a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="2be7a-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="2be7a-116">概觀</span><span class="sxs-lookup"><span data-stu-id="2be7a-116">Overview</span></span>

<span data-ttu-id="2be7a-117">Control Spy 會將選取的通用控制項裝載在其應用程式視窗的中央。</span><span class="sxs-lookup"><span data-stu-id="2be7a-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="2be7a-118">您可以從視窗左側的清單方塊中選取不同的控制項，來變更顯示的控制項。</span><span class="sxs-lookup"><span data-stu-id="2be7a-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="2be7a-119">控制項所收到的訊息或通知，將會列在視窗的右側。</span><span class="sxs-lookup"><span data-stu-id="2be7a-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="2be7a-120">您可以使用 [接收到的 **訊息** 和 **收到的通知** ] 核取方塊來啟用或停用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2be7a-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="2be7a-121">下圖顯示「控制項 Spy」應用程式。</span><span class="sxs-lookup"><span data-stu-id="2be7a-121">The following image shows the Control Spy application.</span></span>

![控制 spy 視窗](images/controlspy-main.png)

<span data-ttu-id="2be7a-123">在視窗底部，有數個索引標籤會呈現更多功能。</span><span class="sxs-lookup"><span data-stu-id="2be7a-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="2be7a-124">樣式</span><span class="sxs-lookup"><span data-stu-id="2be7a-124">Styles</span></span>

<span data-ttu-id="2be7a-125">[ **樣式** ] 索引標籤可讓您變更控制項目前的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="2be7a-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="2be7a-126">選取或取消選取任何列出的樣式，然後按一下 [套用 **] 按鈕來** 變更所顯示控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="2be7a-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="2be7a-127">或者，您可以使用 [ **重新** 建立] 按鈕，以選取的樣式來建立新的控制項。</span><span class="sxs-lookup"><span data-stu-id="2be7a-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="2be7a-128">[ **重設** ] 按鈕會將控制項傳回到預設樣式。</span><span class="sxs-lookup"><span data-stu-id="2be7a-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="2be7a-129">索引標籤下方的 **複製樣式** 和 **複製 ExStyle** 按鈕會將選取的樣式常數複製到剪貼簿，作為位或 (\|) 分隔清單。</span><span class="sxs-lookup"><span data-stu-id="2be7a-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="2be7a-130">您可以將此清單直接貼到 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 的呼叫中，以在您自己的應用程式中以相同的樣式提供控制項。</span><span class="sxs-lookup"><span data-stu-id="2be7a-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="2be7a-131">下圖顯示按鈕控制項的 [ **樣式** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2be7a-131">The following image shows the **Styles** tab for a button control.</span></span>

![控制 spy 樣式索引標籤](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="2be7a-133">訊息</span><span class="sxs-lookup"><span data-stu-id="2be7a-133">Messages</span></span>

<span data-ttu-id="2be7a-134">[ **訊息** ] 索引標籤可讓您將幾乎任何訊息傳送至控制項。</span><span class="sxs-lookup"><span data-stu-id="2be7a-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="2be7a-135">從清單方塊中選取訊息之後，您就可以輸入資料，而該資料會以 *wParam* 和 *lParam* 參數的形式傳送至 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="2be7a-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="2be7a-136">當您按一下 [ **傳送**] 之後，訊息會傳送至控制項，而且任何結果都會顯示在索引標籤底部的文字方塊中。</span><span class="sxs-lookup"><span data-stu-id="2be7a-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="2be7a-137">下圖顯示選取特定訊息時的 [訊息] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2be7a-137">The following image shows the messages tab when a particular message is selected.</span></span>

![控制 spy 訊息索引標籤](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="2be7a-139">大小/色彩</span><span class="sxs-lookup"><span data-stu-id="2be7a-139">Size/Color</span></span>

<span data-ttu-id="2be7a-140">[ **大小]/[色彩** ] 索引標籤可以用來變更控制項的大小，以及其背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="2be7a-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="2be7a-141">哪裡可以取得 Control Spy</span><span class="sxs-lookup"><span data-stu-id="2be7a-141">Where to Get Control Spy</span></span>

<span data-ttu-id="2be7a-142">您可以從 MSDN 下載 [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) 。</span><span class="sxs-lookup"><span data-stu-id="2be7a-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="2be7a-143">這兩個版本都包含在下載中。</span><span class="sxs-lookup"><span data-stu-id="2be7a-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2be7a-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="2be7a-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2be7a-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="2be7a-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2be7a-146">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="2be7a-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="2be7a-147">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="2be7a-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 