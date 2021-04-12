---
title: 'WM_GESTURE 訊息 (Winuser .h) '
description: 傳遞筆勢的相關資訊。
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384938"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="a609b-104">WM \_ 手勢訊息</span><span class="sxs-lookup"><span data-stu-id="a609b-104">WM\_GESTURE message</span></span>

<span data-ttu-id="a609b-105">傳遞筆勢的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a609b-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="a609b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a609b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a609b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a609b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a609b-108">提供識別手勢命令和筆勢特定引數值的資訊。</span><span class="sxs-lookup"><span data-stu-id="a609b-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="a609b-109">這項資訊與在 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構的 **ullArguments** 成員中傳遞的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="a609b-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a609b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a609b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a609b-111">提供識別手勢命令和筆勢特定引數值之資訊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a609b-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="a609b-112">這項資訊是透過呼叫 [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)來取出。</span><span class="sxs-lookup"><span data-stu-id="a609b-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a609b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a609b-113">Return value</span></span>

<span data-ttu-id="a609b-114">如果應用程式處理此訊息，它應該會傳回0。</span><span class="sxs-lookup"><span data-stu-id="a609b-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="a609b-115">如果應用程式未處理訊息，則必須呼叫 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="a609b-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="a609b-116">未這樣做會導致應用程式流失記憶體，因為觸控輸入控點將不會關閉，且不會釋放相關聯的進程記憶體。</span><span class="sxs-lookup"><span data-stu-id="a609b-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a609b-117">備註</span><span class="sxs-lookup"><span data-stu-id="a609b-117">Remarks</span></span>

<span data-ttu-id="a609b-118">下表列出支援的手勢命令。</span><span class="sxs-lookup"><span data-stu-id="a609b-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="a609b-119">手勢識別碼</span><span class="sxs-lookup"><span data-stu-id="a609b-119">Gesture ID</span></span>            | <span data-ttu-id="a609b-120">值 (*dwID*) </span><span class="sxs-lookup"><span data-stu-id="a609b-120">Value (*dwID*)</span></span> | <span data-ttu-id="a609b-121">Description</span><span class="sxs-lookup"><span data-stu-id="a609b-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a609b-122">**GID \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="a609b-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="a609b-123">1</span><span class="sxs-lookup"><span data-stu-id="a609b-123">1</span></span>              | <span data-ttu-id="a609b-124">表示正在開始泛型手勢。</span><span class="sxs-lookup"><span data-stu-id="a609b-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="a609b-125">**GID \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="a609b-125">**GID\_END**</span></span>          | <span data-ttu-id="a609b-126">2</span><span class="sxs-lookup"><span data-stu-id="a609b-126">2</span></span>              | <span data-ttu-id="a609b-127">指出泛型手勢結束。</span><span class="sxs-lookup"><span data-stu-id="a609b-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a609b-128">**GID \_ 縮放**</span><span class="sxs-lookup"><span data-stu-id="a609b-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="a609b-129">3</span><span class="sxs-lookup"><span data-stu-id="a609b-129">3</span></span>              | <span data-ttu-id="a609b-130">表示縮放開始、縮放移動或縮放停用。</span><span class="sxs-lookup"><span data-stu-id="a609b-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="a609b-131">第一個 **GID \_ zoom** 命令訊息會開始縮放，但不會造成任何縮放。</span><span class="sxs-lookup"><span data-stu-id="a609b-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="a609b-132">第二個 **gid \_ zoom** 命令會觸發相對於第一個 **gid \_ 縮放** 中所含狀態的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="a609b-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="a609b-133">**GID \_ 平移**</span><span class="sxs-lookup"><span data-stu-id="a609b-133">**GID\_PAN**</span></span>          | <span data-ttu-id="a609b-134">4</span><span class="sxs-lookup"><span data-stu-id="a609b-134">4</span></span>              | <span data-ttu-id="a609b-135">表示移動流覽或平移開始。</span><span class="sxs-lookup"><span data-stu-id="a609b-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="a609b-136">第一個 **GID \_ pan** 命令表示平移開始，但不會執行任何移動。</span><span class="sxs-lookup"><span data-stu-id="a609b-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="a609b-137">使用第二個 **GID \_ PAN** 命令訊息，應用程式將會開始移動。</span><span class="sxs-lookup"><span data-stu-id="a609b-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="a609b-138">**GID \_ 旋轉**</span><span class="sxs-lookup"><span data-stu-id="a609b-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="a609b-139">5</span><span class="sxs-lookup"><span data-stu-id="a609b-139">5</span></span>              | <span data-ttu-id="a609b-140">表示旋轉移動或旋轉開始。</span><span class="sxs-lookup"><span data-stu-id="a609b-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="a609b-141">第一個 **GID \_ 旋轉** 命令訊息表示旋轉移動或旋轉開始，但不會旋轉。</span><span class="sxs-lookup"><span data-stu-id="a609b-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="a609b-142">第二個 **gid \_ 輪替** 命令訊息將會觸發相對於第一個 **GID \_ 旋轉** 所含狀態的旋轉作業。</span><span class="sxs-lookup"><span data-stu-id="a609b-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="a609b-143">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="a609b-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="a609b-144">6</span><span class="sxs-lookup"><span data-stu-id="a609b-144">6</span></span>              | <span data-ttu-id="a609b-145">表示雙向點一下手勢。</span><span class="sxs-lookup"><span data-stu-id="a609b-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a609b-146">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="a609b-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="a609b-147">7</span><span class="sxs-lookup"><span data-stu-id="a609b-147">7</span></span>              | <span data-ttu-id="a609b-148">表示按下和點擊手勢。</span><span class="sxs-lookup"><span data-stu-id="a609b-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="a609b-149">為了啟用舊版支援，必須使用 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)轉送具有 **GID \_ BEGIN** 和 **gid \_ END** 手勢命令的訊息。</span><span class="sxs-lookup"><span data-stu-id="a609b-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="a609b-150">下表指出在 *lParam* 和 *wParam* 參數中傳遞的手勢引數。</span><span class="sxs-lookup"><span data-stu-id="a609b-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="a609b-151">手勢識別碼</span><span class="sxs-lookup"><span data-stu-id="a609b-151">Gesture ID</span></span>            | <span data-ttu-id="a609b-152">手勢</span><span class="sxs-lookup"><span data-stu-id="a609b-152">Gesture</span></span>        | <span data-ttu-id="a609b-153">*ullArgument*</span><span class="sxs-lookup"><span data-stu-id="a609b-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="a609b-154">[**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)結構中的 *ptsLocation*</span><span class="sxs-lookup"><span data-stu-id="a609b-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a609b-155">**GID \_ 縮放**</span><span class="sxs-lookup"><span data-stu-id="a609b-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="a609b-156">放大/縮小</span><span class="sxs-lookup"><span data-stu-id="a609b-156">Zoom In/Out</span></span>    | <span data-ttu-id="a609b-157">表示兩個點之間的距離。</span><span class="sxs-lookup"><span data-stu-id="a609b-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="a609b-158">指出縮放的中心。</span><span class="sxs-lookup"><span data-stu-id="a609b-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="a609b-159">**GID \_ 平移**</span><span class="sxs-lookup"><span data-stu-id="a609b-159">**GID\_PAN**</span></span>          | <span data-ttu-id="a609b-160">移動瀏覽</span><span class="sxs-lookup"><span data-stu-id="a609b-160">Pan</span></span>            | <span data-ttu-id="a609b-161">表示兩個點之間的距離。</span><span class="sxs-lookup"><span data-stu-id="a609b-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="a609b-162">表示平移的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a609b-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="a609b-163">**GID \_ 旋轉**</span><span class="sxs-lookup"><span data-stu-id="a609b-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="a609b-164">旋轉 (pivot) </span><span class="sxs-lookup"><span data-stu-id="a609b-164">Rotate (pivot)</span></span> | <span data-ttu-id="a609b-165">如果已設定 **GF \_ 開始** 旗標，則表示旋轉的角度。</span><span class="sxs-lookup"><span data-stu-id="a609b-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="a609b-166">否則，這是自旋轉開始之後的角度變化。</span><span class="sxs-lookup"><span data-stu-id="a609b-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="a609b-167">這會經過簽署，以指出旋轉的方向。</span><span class="sxs-lookup"><span data-stu-id="a609b-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="a609b-168">使用 [**gid \_ \_ \_ 從 \_ 引數旋轉角度**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) 和 [**gid \_ 將 \_ 角度旋轉 \_ 為 \_ 引數**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) 宏，以取得和設定角度值。</span><span class="sxs-lookup"><span data-stu-id="a609b-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="a609b-169">這表示旋轉的中心，也就是目標物件周圍旋轉的靜止點。</span><span class="sxs-lookup"><span data-stu-id="a609b-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="a609b-170">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="a609b-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="a609b-171">雙手指點</span><span class="sxs-lookup"><span data-stu-id="a609b-171">Two-finger Tap</span></span> | <span data-ttu-id="a609b-172">表示兩個手指之間的距離。</span><span class="sxs-lookup"><span data-stu-id="a609b-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a609b-173">表示雙手指的中心。</span><span class="sxs-lookup"><span data-stu-id="a609b-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="a609b-174">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="a609b-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="a609b-175">點一下</span><span class="sxs-lookup"><span data-stu-id="a609b-175">Press and Tap</span></span>  | <span data-ttu-id="a609b-176">指出第一個手指和第二個手指之間的差異。</span><span class="sxs-lookup"><span data-stu-id="a609b-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="a609b-177">此值會儲存在 **點** 結構中 *ullArgument* 的較低32位。</span><span class="sxs-lookup"><span data-stu-id="a609b-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="a609b-178">指出第一個手指關閉的位置。</span><span class="sxs-lookup"><span data-stu-id="a609b-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="a609b-179">所有距離和位置都是以實體畫面座標來提供。</span><span class="sxs-lookup"><span data-stu-id="a609b-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="a609b-180">*DwID* 和 *ullArgument* 參數只應視為隨附于 GID \_ \* 命令，而且應用程式不應加以修改。</span><span class="sxs-lookup"><span data-stu-id="a609b-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a609b-181">範例</span><span class="sxs-lookup"><span data-stu-id="a609b-181">Examples</span></span>

<span data-ttu-id="a609b-182">下列程式碼說明如何取得與此訊息相關聯的手勢特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a609b-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="a609b-183">您應該一律將未處理的訊息轉送至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) ，並應針對您在呼叫 [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle)時所處理的訊息關閉手勢輸入控制碼。</span><span class="sxs-lookup"><span data-stu-id="a609b-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="a609b-184">在此範例中，將隱藏預設的軌跡處理常式行為，因為每個手勢案例中的 TOUCHINPUT 控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="a609b-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="a609b-185">如果您移除了上述程式碼中未處理訊息的案例，則預設的軌跡處理常式會在預設案例中轉送至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="a609b-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="a609b-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="a609b-186">Requirements</span></span>



| <span data-ttu-id="a609b-187">需求</span><span class="sxs-lookup"><span data-stu-id="a609b-187">Requirement</span></span> | <span data-ttu-id="a609b-188">值</span><span class="sxs-lookup"><span data-stu-id="a609b-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a609b-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a609b-189">Minimum supported client</span></span><br/> | <span data-ttu-id="a609b-190">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a609b-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a609b-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a609b-191">Minimum supported server</span></span><br/> | <span data-ttu-id="a609b-192">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a609b-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="a609b-193">標頭</span><span class="sxs-lookup"><span data-stu-id="a609b-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="a609b-194"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a609b-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a609b-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a609b-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a609b-196">通知</span><span class="sxs-lookup"><span data-stu-id="a609b-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a609b-197">Windows Touch 手勢程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a609b-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

