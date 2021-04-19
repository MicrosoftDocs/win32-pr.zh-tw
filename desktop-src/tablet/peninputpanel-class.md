---
description: PenInputPanel 物件可讓您輕鬆地將就地畫筆輸入新增至您的應用程式。
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: 'PenInputPanel 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975329"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="d660c-103">PenInputPanel 類別</span><span class="sxs-lookup"><span data-stu-id="d660c-103">PenInputPanel class</span></span>

<span data-ttu-id="d660c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d660c-104">\[Deprecated.</span></span> <span data-ttu-id="d660c-105">**PenInputPanel** 已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。\]</span><span class="sxs-lookup"><span data-stu-id="d660c-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="d660c-106">**PenInputPanel** 物件可讓您輕鬆地將就地畫筆輸入新增至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d660c-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="d660c-107">**PenInputPanel** 物件是以可附加的物件形式提供，可讓您將 Tablet PC 輸入面板功能新增至現有的控制項。</span><span class="sxs-lookup"><span data-stu-id="d660c-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="d660c-108">使用者介面大多是由目前的輸入語言所規定。</span><span class="sxs-lookup"><span data-stu-id="d660c-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="d660c-109">您可以選擇 **PenInputPanel** 物件的預設輸入方法，也就是手寫或鍵盤。</span><span class="sxs-lookup"><span data-stu-id="d660c-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="d660c-110">終端使用者可以使用使用者介面上的按鈕，在輸入方法之間切換。</span><span class="sxs-lookup"><span data-stu-id="d660c-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="d660c-111">**PenInputPanel** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d660c-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="d660c-112">列舉</span><span class="sxs-lookup"><span data-stu-id="d660c-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="d660c-113">事件</span><span class="sxs-lookup"><span data-stu-id="d660c-113">Events</span></span>](#events)
-   [<span data-ttu-id="d660c-114">介面</span><span class="sxs-lookup"><span data-stu-id="d660c-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="d660c-115">方法</span><span class="sxs-lookup"><span data-stu-id="d660c-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="d660c-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d660c-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="d660c-117">列舉</span><span class="sxs-lookup"><span data-stu-id="d660c-117">Enumerations</span></span>

<span data-ttu-id="d660c-118">**PenInputPanel** 類別具有這些列舉。</span><span class="sxs-lookup"><span data-stu-id="d660c-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="d660c-119">列舉型別</span><span class="sxs-lookup"><span data-stu-id="d660c-119">Enumeration</span></span>                    | <span data-ttu-id="d660c-120">描述</span><span class="sxs-lookup"><span data-stu-id="d660c-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d660c-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="d660c-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="d660c-122">定義 **PenInputPanel** 物件中目前可用的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="d660c-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="d660c-123">事件</span><span class="sxs-lookup"><span data-stu-id="d660c-123">Events</span></span>

<span data-ttu-id="d660c-124">**PenInputPanel** 類別具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="d660c-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="d660c-125">事件</span><span class="sxs-lookup"><span data-stu-id="d660c-125">Event</span></span>                                                  | <span data-ttu-id="d660c-126">描述</span><span class="sxs-lookup"><span data-stu-id="d660c-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d660c-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="d660c-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="d660c-128">在 **PenInputPanel** 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。</span><span class="sxs-lookup"><span data-stu-id="d660c-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="d660c-129">**PanelChanged**</span><span class="sxs-lookup"><span data-stu-id="d660c-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="d660c-130">在 **PenInputPanel** 物件于配置之間變更時發生。</span><span class="sxs-lookup"><span data-stu-id="d660c-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="d660c-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="d660c-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="d660c-132">在 **PenInputPanel** 物件移動時發生。</span><span class="sxs-lookup"><span data-stu-id="d660c-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="d660c-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="d660c-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="d660c-134">在 **PenInputPanel** 物件顯示或隱藏本身時發生。</span><span class="sxs-lookup"><span data-stu-id="d660c-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="d660c-135">介面</span><span class="sxs-lookup"><span data-stu-id="d660c-135">Interfaces</span></span>

<span data-ttu-id="d660c-136">**PenInputPanel** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="d660c-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="d660c-137">介面</span><span class="sxs-lookup"><span data-stu-id="d660c-137">Interface</span></span>          | <span data-ttu-id="d660c-138">描述</span><span class="sxs-lookup"><span data-stu-id="d660c-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="d660c-139">**IPenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="d660c-139">**IPenInputPanel**</span></span> | <span data-ttu-id="d660c-140">這個物件會實 **IPenInputPanel** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d660c-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d660c-141">方法</span><span class="sxs-lookup"><span data-stu-id="d660c-141">Methods</span></span>

<span data-ttu-id="d660c-142">**PenInputPanel** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d660c-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="d660c-143">方法</span><span class="sxs-lookup"><span data-stu-id="d660c-143">Method</span></span>                                                         | <span data-ttu-id="d660c-144">描述</span><span class="sxs-lookup"><span data-stu-id="d660c-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d660c-145">**CommitPendingInput**</span><span class="sxs-lookup"><span data-stu-id="d660c-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="d660c-146">將收集的筆墨傳送至辨識器，並張貼辨識結果。</span><span class="sxs-lookup"><span data-stu-id="d660c-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d660c-147">**EnableTsf**</span><span class="sxs-lookup"><span data-stu-id="d660c-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="d660c-148">當傳遞 **TRUE** 時， **PenInputPanel** 會嘗試透過文字服務架構 (TSF) ，將文字傳送至附加的控制項，並允許使用更正使用者介面。</span><span class="sxs-lookup"><span data-stu-id="d660c-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="d660c-149">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="d660c-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="d660c-150">將 **PenInputPanel** 物件的位置設定為靜態螢幕位置。</span><span class="sxs-lookup"><span data-stu-id="d660c-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="d660c-151">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="d660c-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="d660c-152">根據 Tablet PC 輸入面板設定來更新和還原 **PenInputPanel** 內容、自動放置畫筆輸入面板，以及將使用者介面設定為預設面板。</span><span class="sxs-lookup"><span data-stu-id="d660c-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d660c-153">屬性</span><span class="sxs-lookup"><span data-stu-id="d660c-153">Properties</span></span>

<span data-ttu-id="d660c-154">**PenInputPanel** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d660c-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="d660c-155">屬性</span><span class="sxs-lookup"><span data-stu-id="d660c-155">Property</span></span>                                                                  | <span data-ttu-id="d660c-156">存取類型</span><span class="sxs-lookup"><span data-stu-id="d660c-156">Access type</span></span>           | <span data-ttu-id="d660c-157">Description</span><span class="sxs-lookup"><span data-stu-id="d660c-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d660c-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="d660c-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="d660c-159">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-159">Read/write</span></span><br/> | <span data-ttu-id="d660c-160">取得或設定 **PenInputPanel** 物件所附加之控制項的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="d660c-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="d660c-161">**自動**</span><span class="sxs-lookup"><span data-stu-id="d660c-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="d660c-162">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-162">Read/write</span></span><br/> | <span data-ttu-id="d660c-163">取得或設定布林值，這個值會指定當使用畫筆設定焦點時，是否要顯示 **PenInputPanel** 物件。</span><span class="sxs-lookup"><span data-stu-id="d660c-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="d660c-164">**忙**</span><span class="sxs-lookup"><span data-stu-id="d660c-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="d660c-165">唯讀</span><span class="sxs-lookup"><span data-stu-id="d660c-165">Read-only</span></span><br/>  | <span data-ttu-id="d660c-166">取得布林值，這個值會指定 **PenInputPanel** 物件目前是否正在處理筆墨。</span><span class="sxs-lookup"><span data-stu-id="d660c-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="d660c-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="d660c-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="d660c-168">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-168">Read/write</span></span><br/> | <span data-ttu-id="d660c-169">取得或設定目前在 **PenInputPanel** 物件內用於輸入的面板類型。</span><span class="sxs-lookup"><span data-stu-id="d660c-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="d660c-170">**DefaultPanel**</span><span class="sxs-lookup"><span data-stu-id="d660c-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="d660c-171">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-171">Read/write</span></span><br/> | <span data-ttu-id="d660c-172">取得或設定哪一個面板類型是在 **PenInputPanel** 物件內用於輸入的預設面板類型。</span><span class="sxs-lookup"><span data-stu-id="d660c-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="d660c-173">**標記**</span><span class="sxs-lookup"><span data-stu-id="d660c-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="d660c-174">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-174">Read/write</span></span><br/> | <span data-ttu-id="d660c-175">取得或設定用於辨識的模擬程式字串名稱。</span><span class="sxs-lookup"><span data-stu-id="d660c-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="d660c-176">**高度**</span><span class="sxs-lookup"><span data-stu-id="d660c-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="d660c-177">唯讀</span><span class="sxs-lookup"><span data-stu-id="d660c-177">Read-only</span></span><br/>  | <span data-ttu-id="d660c-178">取得 **PenInputPanel** 物件在用戶端座標中的高度。</span><span class="sxs-lookup"><span data-stu-id="d660c-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d660c-179">**System.windows.controls.primitives.popup.horizontaloffset**</span><span class="sxs-lookup"><span data-stu-id="d660c-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="d660c-180">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-180">Read/write</span></span><br/> | <span data-ttu-id="d660c-181">取得或設定 **PenInputPanel** 物件的左邊緣與其附加之控制項的左邊緣之間的位移。</span><span class="sxs-lookup"><span data-stu-id="d660c-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="d660c-182">**離開**</span><span class="sxs-lookup"><span data-stu-id="d660c-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="d660c-183">唯讀</span><span class="sxs-lookup"><span data-stu-id="d660c-183">Read-only</span></span><br/>  | <span data-ttu-id="d660c-184">取得 **PenInputPanel** 物件左邊緣的水準或 X 軸位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="d660c-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="d660c-185">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="d660c-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="d660c-186">唯讀</span><span class="sxs-lookup"><span data-stu-id="d660c-186">Read-only</span></span><br/>  | <span data-ttu-id="d660c-187">取得 **PenInputPanel** 物件上邊緣的垂直軸（或 y 軸）位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="d660c-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="d660c-188">**System.windows.controls.primitives.popup.verticaloffset**</span><span class="sxs-lookup"><span data-stu-id="d660c-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="d660c-189">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-189">Read/write</span></span><br/> | <span data-ttu-id="d660c-190">取得或設定 **PenInputPanel** 物件的最接近水準邊緣與其附加之控制項最接近水準邊緣之間的位移。</span><span class="sxs-lookup"><span data-stu-id="d660c-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="d660c-191">**可見**</span><span class="sxs-lookup"><span data-stu-id="d660c-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="d660c-192">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d660c-192">Read/write</span></span><br/> | <span data-ttu-id="d660c-193">取得或設定值，這個值會指出是否可以看到 **PenInputPanel** 物件。</span><span class="sxs-lookup"><span data-stu-id="d660c-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="d660c-194">**寬度**</span><span class="sxs-lookup"><span data-stu-id="d660c-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="d660c-195">唯讀</span><span class="sxs-lookup"><span data-stu-id="d660c-195">Read-only</span></span><br/>  | <span data-ttu-id="d660c-196">取得用戶端座標中 **PenInputPanel** 物件的寬度。</span><span class="sxs-lookup"><span data-stu-id="d660c-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d660c-197">備註</span><span class="sxs-lookup"><span data-stu-id="d660c-197">Remarks</span></span>

<span data-ttu-id="d660c-198">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="d660c-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="d660c-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="d660c-199">Requirements</span></span>



| <span data-ttu-id="d660c-200">需求</span><span class="sxs-lookup"><span data-stu-id="d660c-200">Requirement</span></span> | <span data-ttu-id="d660c-201">值</span><span class="sxs-lookup"><span data-stu-id="d660c-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d660c-202">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d660c-202">Minimum supported client</span></span><br/> | <span data-ttu-id="d660c-203">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d660c-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d660c-204">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d660c-204">Minimum supported server</span></span><br/> | <span data-ttu-id="d660c-205">都不支援</span><span class="sxs-lookup"><span data-stu-id="d660c-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d660c-206">標頭</span><span class="sxs-lookup"><span data-stu-id="d660c-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="d660c-207"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d660c-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d660c-208">程式庫</span><span class="sxs-lookup"><span data-stu-id="d660c-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="d660c-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d660c-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d660c-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d660c-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d660c-211">使用 PenInputPanel 類別來設計輸入面板</span><span class="sxs-lookup"><span data-stu-id="d660c-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
