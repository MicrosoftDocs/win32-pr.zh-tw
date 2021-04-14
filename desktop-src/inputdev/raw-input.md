---
title: 原始輸入
description: 本節說明系統如何提供原始輸入給您的應用程式，以及應用程式如何接收和處理該輸入。
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面，原始輸入
- 使用者輸入，原始輸入
- 捕獲使用者輸入，原始輸入
- 原始輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375172"
---
# <a name="raw-input"></a><span data-ttu-id="c3a73-108">原始輸入</span><span class="sxs-lookup"><span data-stu-id="c3a73-108">Raw Input</span></span>

<span data-ttu-id="c3a73-109">本節說明系統如何提供原始輸入給您的應用程式，以及應用程式如何接收和處理該輸入。</span><span class="sxs-lookup"><span data-stu-id="c3a73-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="c3a73-110">原始輸入有時稱為一般輸入。</span><span class="sxs-lookup"><span data-stu-id="c3a73-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="c3a73-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="c3a73-111">In This Section</span></span>



| <span data-ttu-id="c3a73-112">Name</span><span class="sxs-lookup"><span data-stu-id="c3a73-112">Name</span></span>                                           | <span data-ttu-id="c3a73-113">描述</span><span class="sxs-lookup"><span data-stu-id="c3a73-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3a73-114">關於原始輸入</span><span class="sxs-lookup"><span data-stu-id="c3a73-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="c3a73-115">討論裝置的使用者輸入，例如操縱杆、觸控式螢幕和麥克風。</span><span class="sxs-lookup"><span data-stu-id="c3a73-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="c3a73-116">使用原始輸入</span><span class="sxs-lookup"><span data-stu-id="c3a73-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="c3a73-117">提供與原始輸入相關之工作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="c3a73-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="c3a73-118">原始輸入參考</span><span class="sxs-lookup"><span data-stu-id="c3a73-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="c3a73-119">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="c3a73-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="c3a73-120">函式</span><span class="sxs-lookup"><span data-stu-id="c3a73-120">Functions</span></span>



| <span data-ttu-id="c3a73-121">Name</span><span class="sxs-lookup"><span data-stu-id="c3a73-121">Name</span></span>                                                                 | <span data-ttu-id="c3a73-122">描述</span><span class="sxs-lookup"><span data-stu-id="c3a73-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3a73-123">**DefRawInputProc**</span><span class="sxs-lookup"><span data-stu-id="c3a73-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="c3a73-124">呼叫預設的原始輸入程式，以提供應用程式未處理之任何原始輸入訊息的預設處理。</span><span class="sxs-lookup"><span data-stu-id="c3a73-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="c3a73-125">這個函式可確保處理每個訊息。</span><span class="sxs-lookup"><span data-stu-id="c3a73-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="c3a73-126">呼叫 [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)時所使用的參數，與視窗程式所收到的參數相同。</span><span class="sxs-lookup"><span data-stu-id="c3a73-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="c3a73-127">**GetRawInputBuffer**</span><span class="sxs-lookup"><span data-stu-id="c3a73-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="c3a73-128">執行原始輸入資料的緩衝讀取。</span><span class="sxs-lookup"><span data-stu-id="c3a73-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c3a73-129">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="c3a73-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="c3a73-130">從指定的裝置取得原始輸入。</span><span class="sxs-lookup"><span data-stu-id="c3a73-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c3a73-131">**GetRawInputDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="c3a73-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="c3a73-132">取得原始輸入裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c3a73-133">**GetRawInputDeviceList**</span><span class="sxs-lookup"><span data-stu-id="c3a73-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="c3a73-134">列舉附加至系統的原始輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="c3a73-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c3a73-135">**GetRegisteredRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="c3a73-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="c3a73-136">取得目前應用程式之原始輸入裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c3a73-137">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="c3a73-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="c3a73-138">註冊提供原始輸入資料的裝置。</span><span class="sxs-lookup"><span data-stu-id="c3a73-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="c3a73-139">巨集</span><span class="sxs-lookup"><span data-stu-id="c3a73-139">Macros</span></span>



| <span data-ttu-id="c3a73-140">Name</span><span class="sxs-lookup"><span data-stu-id="c3a73-140">Name</span></span>                                                            | <span data-ttu-id="c3a73-141">描述</span><span class="sxs-lookup"><span data-stu-id="c3a73-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3a73-142">**取得 \_ RAWINPUT 程式 \_ 代碼 \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="c3a73-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="c3a73-143">從 [**WM \_ 輸入**](wm-input.md)中的 *wParam* 取得輸入碼。</span><span class="sxs-lookup"><span data-stu-id="c3a73-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="c3a73-144">**NEXTRAWINPUTBLOCK**</span><span class="sxs-lookup"><span data-stu-id="c3a73-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="c3a73-145">取得 [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) 結構陣列中下一個結構的位置。</span><span class="sxs-lookup"><span data-stu-id="c3a73-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="c3a73-146">通知</span><span class="sxs-lookup"><span data-stu-id="c3a73-146">Notifications</span></span>



| <span data-ttu-id="c3a73-147">Name</span><span class="sxs-lookup"><span data-stu-id="c3a73-147">Name</span></span>                                                        | <span data-ttu-id="c3a73-148">描述</span><span class="sxs-lookup"><span data-stu-id="c3a73-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c3a73-149">**WM \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="c3a73-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="c3a73-150">傳送至正在取得原始輸入的視窗。</span><span class="sxs-lookup"><span data-stu-id="c3a73-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="c3a73-151">**WM \_ 輸入 \_ 設備 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="c3a73-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="c3a73-152">傳送至已註冊要接收原始輸入的視窗。</span><span class="sxs-lookup"><span data-stu-id="c3a73-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="c3a73-153">結構</span><span class="sxs-lookup"><span data-stu-id="c3a73-153">Structures</span></span>



| <span data-ttu-id="c3a73-154">Name</span><span class="sxs-lookup"><span data-stu-id="c3a73-154">Name</span></span>                                                            | <span data-ttu-id="c3a73-155">描述</span><span class="sxs-lookup"><span data-stu-id="c3a73-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3a73-156">**RAWHID**</span><span class="sxs-lookup"><span data-stu-id="c3a73-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="c3a73-157">描述來自人體介面裝置 (HID) 的原始輸入格式。</span><span class="sxs-lookup"><span data-stu-id="c3a73-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="c3a73-158">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="c3a73-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="c3a73-159">包含來自裝置的原始輸入。</span><span class="sxs-lookup"><span data-stu-id="c3a73-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="c3a73-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="c3a73-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="c3a73-161">定義原始輸入裝置的資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="c3a73-162">**RAWINPUTDEVICELIST**</span><span class="sxs-lookup"><span data-stu-id="c3a73-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="c3a73-163">包含原始輸入裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="c3a73-164">**RAWINPUTHEADER**</span><span class="sxs-lookup"><span data-stu-id="c3a73-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="c3a73-165">包含屬於原始輸入資料一部分的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="c3a73-166">**RAWKEYBOARD**</span><span class="sxs-lookup"><span data-stu-id="c3a73-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="c3a73-167">包含鍵盤狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="c3a73-168">**RAWMOUSE**</span><span class="sxs-lookup"><span data-stu-id="c3a73-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="c3a73-169">包含滑鼠狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3a73-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="c3a73-170">**RID \_ 裝置 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="c3a73-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="c3a73-171">定義來自任何裝置的原始輸入資料。</span><span class="sxs-lookup"><span data-stu-id="c3a73-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="c3a73-172">**RID \_ 裝置 \_ 資訊 \_ 隱藏**</span><span class="sxs-lookup"><span data-stu-id="c3a73-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="c3a73-173">定義來自指定之隱藏的原始輸入資料。</span><span class="sxs-lookup"><span data-stu-id="c3a73-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="c3a73-174">**RID \_ 裝置 \_ 資訊 \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="c3a73-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="c3a73-175">定義來自指定鍵盤的原始輸入資料。</span><span class="sxs-lookup"><span data-stu-id="c3a73-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="c3a73-176">**RID \_ 裝置 \_ 資訊 \_ 滑鼠**</span><span class="sxs-lookup"><span data-stu-id="c3a73-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="c3a73-177">定義來自指定滑鼠的原始輸入資料。</span><span class="sxs-lookup"><span data-stu-id="c3a73-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

