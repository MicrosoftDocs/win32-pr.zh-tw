---
title: 指標訊息旗標
description: 各種指標宏所使用的值 (查看宏) 。
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995580"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="b7c8a-103">指標訊息旗標</span><span class="sxs-lookup"><span data-stu-id="b7c8a-103">Pointer Message Flags</span></span>

<span data-ttu-id="b7c8a-104">各種指標宏所使用的值 (查看 [宏](macros.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="b7c8a-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7c8a-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-107">表示新指標的抵達。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7c8a-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-110">指出此指標持續存在。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="b7c8a-111">如果未設定此旗標，則表示指標具有左方偵測範圍。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="b7c8a-112">只有當滑鼠停留指標離開偵測範圍時，才會設定這個旗標 (**POINTER_FLAG_UPDATE** 設定) ，或是當與視窗介面的指標離開偵測範圍 (**POINTER_FLAG_UP** 設定為) 時。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b7c8a-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-115">指出此指標與數位板介面相同。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="b7c8a-116">如果未設定此旗標，則會指出滑鼠停留指標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7c8a-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-119">指出主要動作，類似于按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="b7c8a-120">當觸控指標與數位板介面聯繫時，會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="b7c8a-121">當畫筆指標與數位板介面聯繫時，如果未按下任何按鈕，就會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="b7c8a-122">當滑鼠左鍵關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="b7c8a-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-125">表示第二個動作，類似滑鼠向下按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="b7c8a-126">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-127">當畫筆指標與數位板介面一起使用時，會設定此旗標，並按下畫筆圓筒按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="b7c8a-128">當滑鼠右鍵關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="b7c8a-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-131">類似滑鼠滾輪按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="b7c8a-132">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-133">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-134">當滑鼠滾輪按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b7c8a-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-137">類似于第一個擴充的滑鼠 (XButton1) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="b7c8a-138">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-139">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-140">當第一個擴充的滑鼠 (XBUTTON1) 按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="b7c8a-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-143">類似于第二個擴充的滑鼠 (XButton2) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="b7c8a-144">觸控指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-145">畫筆指標不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="b7c8a-146">當第二個擴充的滑鼠 (XBUTTON2) 按鈕關閉時，滑鼠指標會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="b7c8a-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-149">指出此指標已指定為主要指標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="b7c8a-150">主要指標是單一指標，可在非主要指標可用的動作之外執行動作。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="b7c8a-151">例如，當主要指標與視窗的介面接觸時，它可能會將 WM_POINTERACTI加值稅E 訊息傳送給視窗，以提供啟動的機會。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="b7c8a-152">主要指標是從系統上所有目前使用者的互動中識別 (滑鼠、觸控、畫筆等) 。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="b7c8a-153">因此，主要指標可能不會與您的應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="b7c8a-154">多點觸控互動中的第一個連絡人會設定為主要指標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="b7c8a-155">識別主要指標之後，必須先提起所有連絡人，才能將新的連絡人識別為主要指標。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="b7c8a-156">針對不處理指標輸入的應用程式，只有主要指標的事件會升級為滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="b7c8a-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-159">信賴度是來自來源裝置的建議，這是指指標是否代表預期或意外的互動，這與意外互動 (的 PT_TOUCH 指標（例如，與掌上的) 可以觸發輸入）特別相關。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="b7c8a-160">此旗標的存在表示來源裝置有很高的信賴度，此輸入是預期互動的一部分。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c8a-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="b7c8a-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7c8a-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="b7c8a-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="b7c8a-163">指出指標以異常的方式脫離，例如當系統收到指標的無效輸入，或是具有作用中指標的裝置突然離開時。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="b7c8a-164">如果接收輸入的應用程式是在執行這項作業的位置，則應該將互動視為未完成，並反轉任何相關指標的影響。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7c8a-165">備註</span><span class="sxs-lookup"><span data-stu-id="b7c8a-165">Remarks</span></span>

<span data-ttu-id="b7c8a-166">XBUTTON1 和 XBUTTON2 是許多滑鼠裝置上使用的其他按鈕。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="b7c8a-167">它們會傳回與標準滑鼠按鍵相同的資料。</span><span class="sxs-lookup"><span data-stu-id="b7c8a-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c8a-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7c8a-168">Requirements</span></span>



| <span data-ttu-id="b7c8a-169">需求</span><span class="sxs-lookup"><span data-stu-id="b7c8a-169">Requirement</span></span> | <span data-ttu-id="b7c8a-170">值</span><span class="sxs-lookup"><span data-stu-id="b7c8a-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c8a-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7c8a-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c8a-172">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7c8a-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7c8a-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7c8a-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c8a-174">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7c8a-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7c8a-175">標頭</span><span class="sxs-lookup"><span data-stu-id="b7c8a-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c8a-176"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c8a-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c8a-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7c8a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c8a-178">常數</span><span class="sxs-lookup"><span data-stu-id="b7c8a-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="b7c8a-179">巨集</span><span class="sxs-lookup"><span data-stu-id="b7c8a-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





