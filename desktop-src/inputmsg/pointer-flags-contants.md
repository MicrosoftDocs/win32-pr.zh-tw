---
title: 指標旗標
description: 可以出現在 POINTER_INFO 結構的 pointerFlags 欄位中的值。
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686115"
---
# <a name="pointer-flags"></a><span data-ttu-id="2762a-103">指標旗標</span><span class="sxs-lookup"><span data-stu-id="2762a-103">Pointer Flags</span></span>

<span data-ttu-id="2762a-104">可以出現在 [**POINTER_INFO**](/previous-versions/windows/desktop/api)結構的 **pointerFlags** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="2762a-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="2762a-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="2762a-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2762a-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-107">預設</span><span class="sxs-lookup"><span data-stu-id="2762a-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="2762a-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2762a-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2762a-110">表示新指標的抵達。</span><span class="sxs-lookup"><span data-stu-id="2762a-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="2762a-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2762a-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="2762a-113">指出此指標持續存在。</span><span class="sxs-lookup"><span data-stu-id="2762a-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="2762a-114">如果未設定此旗標，則表示指標具有左方偵測範圍。</span><span class="sxs-lookup"><span data-stu-id="2762a-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="2762a-115">只有當滑鼠停留指標離開偵測範圍時，才會設定這個旗標 (**POINTER_FLAG_UPDATE** 設定) ，或是當與視窗介面的指標離開偵測範圍 (**POINTER_FLAG_UP** 設定為) 時。</span><span class="sxs-lookup"><span data-stu-id="2762a-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="2762a-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2762a-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="2762a-118">指出此指標與數位板介面相同。</span><span class="sxs-lookup"><span data-stu-id="2762a-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="2762a-119">如果未設定此旗標，則會指出滑鼠停留指標。</span><span class="sxs-lookup"><span data-stu-id="2762a-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2762a-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2762a-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2762a-122">指出主要動作，類似于按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="2762a-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="2762a-123">當觸控指標與數位板介面聯繫時，會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="2762a-124">當畫筆指標與數位板介面聯繫時，如果未按下任何按鈕，就會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="2762a-125">當滑鼠左鍵關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2762a-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2762a-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="2762a-128">表示第二個動作，類似滑鼠向下按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="2762a-129">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-130">當畫筆指標與數位板介面一起使用時，會設定此旗標，並按下畫筆圓筒按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="2762a-131">當滑鼠右鍵關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2762a-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2762a-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="2762a-134">類似滑鼠滾輪按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="2762a-135">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-136">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-137">當滑鼠滾輪按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2762a-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2762a-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="2762a-140">類似于第一個擴充的滑鼠 (XButton1) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="2762a-141">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-142">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-143">當第一個擴充的滑鼠 (XBUTTON1) 按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2762a-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="2762a-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="2762a-146">類似于第二個擴充的滑鼠 (XButton2) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="2762a-147">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-148">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="2762a-149">當第二個擴充的滑鼠 (XBUTTON2) 按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="2762a-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="2762a-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="2762a-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-152">指出此指標已指定為主要指標。</span><span class="sxs-lookup"><span data-stu-id="2762a-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="2762a-153">主要指標是單一指標，可在非主要指標可用的動作之外執行動作。</span><span class="sxs-lookup"><span data-stu-id="2762a-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="2762a-154">例如，當主要指標與視窗的介面接觸時，它可能會將 [**WM_POINTERACTI加值稅E**](wm-pointeractivate.md) 訊息傳送給視窗，以提供啟動的機會。</span><span class="sxs-lookup"><span data-stu-id="2762a-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="2762a-155">主要指標是從系統上所有目前使用者的互動中識別 (滑鼠、觸控、畫筆等) 。</span><span class="sxs-lookup"><span data-stu-id="2762a-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="2762a-156">因此，主要指標可能不會與您的應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="2762a-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="2762a-157">多點觸控互動中的第一個連絡人會設定為主要指標。</span><span class="sxs-lookup"><span data-stu-id="2762a-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="2762a-158">識別主要指標之後，必須先提起所有連絡人，才能將新的連絡人識別為主要指標。</span><span class="sxs-lookup"><span data-stu-id="2762a-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="2762a-159">針對不處理指標輸入的應用程式，只有主要指標的事件會升級為滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="2762a-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="2762a-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="2762a-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-162">信賴度是來自來源裝置的建議，這是指指標是否代表預期或意外的互動，這與意外互動 (的 PT_TOUCH 指標（例如，與掌上的) 可以觸發輸入）特別相關。</span><span class="sxs-lookup"><span data-stu-id="2762a-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="2762a-163">此旗標的存在表示來源裝置有很高的信賴度，此輸入是預期互動的一部分。</span><span class="sxs-lookup"><span data-stu-id="2762a-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="2762a-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="2762a-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-166">指出指標以異常的方式脫離，例如當系統收到指標的無效輸入，或是具有作用中指標的裝置突然離開時。</span><span class="sxs-lookup"><span data-stu-id="2762a-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="2762a-167">如果接收輸入的應用程式是在執行這項作業的位置，則應該將互動視為未完成，並反轉任何相關指標的影響。</span><span class="sxs-lookup"><span data-stu-id="2762a-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="2762a-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2762a-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-170">指出此指標已轉換為關閉狀態;也就是說，它會與數位板介面建立聯繫。</span><span class="sxs-lookup"><span data-stu-id="2762a-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="2762a-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2762a-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-173">指出這是不包含指標狀態變更的簡單更新。</span><span class="sxs-lookup"><span data-stu-id="2762a-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="2762a-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="2762a-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-176">指出這個指標轉換成 up 狀態;亦即，與數位板介面的聯繫已結束。</span><span class="sxs-lookup"><span data-stu-id="2762a-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="2762a-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2762a-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-179">指出與滑鼠滾輪相關聯的輸入。</span><span class="sxs-lookup"><span data-stu-id="2762a-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="2762a-180">針對滑鼠指標，這相當於滑鼠滾輪的動作 ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2762a-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="2762a-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="2762a-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-183">表示與指標 h 滾輪相關聯的輸入。</span><span class="sxs-lookup"><span data-stu-id="2762a-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="2762a-184">若是滑鼠指標，這相當於滑鼠水準滾輪的動作 ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2762a-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="2762a-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="2762a-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-187">指出此指標是由與) 其他專案相關聯的 (所捕捉，而原始元素已遺失 capture (請參閱 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2762a-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2762a-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="2762a-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2762a-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="2762a-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="2762a-190">指出這個指標有相關聯的轉換。</span><span class="sxs-lookup"><span data-stu-id="2762a-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2762a-191">備註</span><span class="sxs-lookup"><span data-stu-id="2762a-191">Remarks</span></span>

<span data-ttu-id="2762a-192">XBUTTON1 和 XBUTTON2 是許多滑鼠裝置上使用的其他按鈕。</span><span class="sxs-lookup"><span data-stu-id="2762a-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="2762a-193">它們會傳回與標準滑鼠按鍵相同的資料。</span><span class="sxs-lookup"><span data-stu-id="2762a-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="2762a-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="2762a-194">Requirements</span></span>



| <span data-ttu-id="2762a-195">需求</span><span class="sxs-lookup"><span data-stu-id="2762a-195">Requirement</span></span> | <span data-ttu-id="2762a-196">值</span><span class="sxs-lookup"><span data-stu-id="2762a-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2762a-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2762a-197">Minimum supported client</span></span><br/> | <span data-ttu-id="2762a-198">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2762a-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2762a-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2762a-199">Minimum supported server</span></span><br/> | <span data-ttu-id="2762a-200">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2762a-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2762a-201">標頭</span><span class="sxs-lookup"><span data-stu-id="2762a-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="2762a-202"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="2762a-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2762a-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2762a-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2762a-204">常數</span><span class="sxs-lookup"><span data-stu-id="2762a-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="2762a-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="2762a-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="2762a-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="2762a-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

