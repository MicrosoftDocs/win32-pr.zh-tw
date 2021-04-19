---
title: 使用原始輸入
description: 本章節包含與原始輸入相關之工作的範例程式碼。
ms.assetid: e078e13c-06b8-4440-9d37-78c344b587e9
keywords:
- 使用者輸入，原始輸入
- 捕獲使用者輸入，原始輸入
- 原始輸入
- 緩衝讀取原始輸入
- 原始輸入的標準讀取
- 註冊原始輸入
- 讀取原始輸入
- 搖桿原始輸入
- 遊戲台原始輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637137481fd930214beb04d2c75a7a2921d8b5fa
ms.sourcegitcommit: ae1241c7d27e0bd128dfa40ca0b4187728b2a9e0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2021
ms.locfileid: "106983269"
---
# <a name="using-raw-input"></a><span data-ttu-id="3271c-112">使用原始輸入</span><span class="sxs-lookup"><span data-stu-id="3271c-112">Using Raw Input</span></span>

<span data-ttu-id="3271c-113">本節包含下列用途的範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="3271c-113">This section includes sample code for the following purposes:</span></span>

-   [<span data-ttu-id="3271c-114">註冊原始輸入</span><span class="sxs-lookup"><span data-stu-id="3271c-114">Registering for Raw Input</span></span>](#registering-for-raw-input)
    -   [<span data-ttu-id="3271c-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="3271c-115">Example 1</span></span>](#example-1)
    -   [<span data-ttu-id="3271c-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="3271c-116">Example 2</span></span>](#example-2)
-   [<span data-ttu-id="3271c-117">執行原始輸入的標準讀取</span><span class="sxs-lookup"><span data-stu-id="3271c-117">Performing a Standard Read of Raw Input</span></span>](#performing-a-standard-read-of-raw-input)
-   [<span data-ttu-id="3271c-118">執行原始輸入的緩衝讀取</span><span class="sxs-lookup"><span data-stu-id="3271c-118">Performing a Buffered Read of Raw Input</span></span>](#performing-a-buffered-read-of-raw-input)

## <a name="registering-for-raw-input"></a><span data-ttu-id="3271c-119">註冊原始輸入</span><span class="sxs-lookup"><span data-stu-id="3271c-119">Registering for Raw Input</span></span>

### <a name="example-1"></a><span data-ttu-id="3271c-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="3271c-120">Example 1</span></span>

<span data-ttu-id="3271c-121">在此範例中，應用程式會從遊戲控制器指定原始輸入 (遊戲台和操縱杆) ，以及電話語音使用量頁面以外的所有裝置，但只會接聽電腦。</span><span class="sxs-lookup"><span data-stu-id="3271c-121">In this sample, an application specifies the raw input from game controllers (both game pads and joysticks) and all devices off the telephony usage page except answering machines.</span></span>

```cpp
RAWINPUTDEVICE Rid[4];
        
Rid[0].usUsagePage = 0x01;          // HID_USAGE_PAGE_GENERIC
Rid[0].usUsage = 0x05;              // HID_USAGE_GENERIC_GAMEPAD
Rid[0].dwFlags = 0;                 // adds game pad
Rid[0].hwndTarget = 0;

Rid[1].usUsagePage = 0x01;          // HID_USAGE_PAGE_GENERIC
Rid[1].usUsage = 0x04;              // HID_USAGE_GENERIC_JOYSTICK
Rid[1].dwFlags = 0;                 // adds joystick
Rid[1].hwndTarget = 0;

Rid[2].usUsagePage = 0x0B;          // HID_USAGE_PAGE_TELEPHONY
Rid[2].usUsage = 0x00; 
Rid[2].dwFlags = RIDEV_PAGEONLY;    // adds all devices from telephony page
Rid[2].hwndTarget = 0;

Rid[3].usUsagePage = 0x0B;          // HID_USAGE_PAGE_TELEPHONY
Rid[3].usUsage = 0x02;              // HID_USAGE_TELEPHONY_ANSWERING_MACHINE
Rid[3].dwFlags = RIDEV_EXCLUDE;     // excludes answering machines
Rid[3].hwndTarget = 0;

if (RegisterRawInputDevices(Rid, 4, sizeof(Rid[0])) == FALSE)
{
    //registration failed. Call GetLastError for the cause of the error.
}
```

### <a name="example-2"></a><span data-ttu-id="3271c-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="3271c-122">Example 2</span></span>

<span data-ttu-id="3271c-123">在此範例中，應用程式需要鍵盤和滑鼠的原始輸入，但想要忽略  [舊版鍵盤](keyboard-input-notifications.md) 和 [滑鼠視窗訊息](mouse-input-notifications.md) (這會來自相同的鍵盤和滑鼠) 。</span><span class="sxs-lookup"><span data-stu-id="3271c-123">In this sample, an application wants raw input from the keyboard and mouse but wants to ignore  [legacy keyboard](keyboard-input-notifications.md) and [mouse window messages](mouse-input-notifications.md) (which would come from the same keyboard and mouse).</span></span>

```cpp
RAWINPUTDEVICE Rid[2];
        
Rid[0].usUsagePage = 0x01;          // HID_USAGE_PAGE_GENERIC
Rid[0].usUsage = 0x02;              // HID_USAGE_GENERIC_MOUSE
Rid[0].dwFlags = RIDEV_NOLEGACY;    // adds mouse and also ignores legacy mouse messages
Rid[0].hwndTarget = 0;

Rid[1].usUsagePage = 0x01;          // HID_USAGE_PAGE_GENERIC
Rid[1].usUsage = 0x06;              // HID_USAGE_GENERIC_KEYBOARD
Rid[1].dwFlags = RIDEV_NOLEGACY;    // adds keyboard and also ignores legacy keyboard messages
Rid[1].hwndTarget = 0;

if (RegisterRawInputDevices(Rid, 2, sizeof(Rid[0])) == FALSE)
{
    //registration failed. Call GetLastError for the cause of the error
}
```

## <a name="performing-a-standard-read-of-raw-input"></a><span data-ttu-id="3271c-124">執行原始輸入的標準讀取</span><span class="sxs-lookup"><span data-stu-id="3271c-124">Performing a Standard Read of Raw Input</span></span>

<span data-ttu-id="3271c-125">此範例示範應用程式如何執行未緩衝的 (或標準) 從鍵盤或滑鼠人類介面裝置 (隱藏) 讀取原始輸入，然後從裝置印出各種資訊。</span><span class="sxs-lookup"><span data-stu-id="3271c-125">This sample shows how an application does an unbuffered (or standard) read of raw input from either a keyboard or mouse Human Interface Device (HID) and then prints out various information from the device.</span></span>

```cpp
case WM_INPUT: 
{
    UINT dwSize;

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, NULL, &dwSize, sizeof(RAWINPUTHEADER));
    LPBYTE lpb = new BYTE[dwSize];
    if (lpb == NULL) 
    {
        return 0;
    } 

    if (GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER)) != dwSize)
         OutputDebugString (TEXT("GetRawInputData does not return correct size !\n")); 

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEKEYBOARD) 
    {
        hResult = StringCchPrintf(szTempOutput, STRSAFE_MAX_CCH,
            TEXT(" Kbd: make=%04x Flags:%04x Reserved:%04x ExtraInformation:%08x, msg=%04x VK=%04x \n"), 
            raw->data.keyboard.MakeCode, 
            raw->data.keyboard.Flags, 
            raw->data.keyboard.Reserved, 
            raw->data.keyboard.ExtraInformation, 
            raw->data.keyboard.Message, 
            raw->data.keyboard.VKey);
        if (FAILED(hResult))
        {
        // TODO: write error handler
        }
        OutputDebugString(szTempOutput);
    }
    else if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        hResult = StringCchPrintf(szTempOutput, STRSAFE_MAX_CCH,
            TEXT("Mouse: usFlags=%04x ulButtons=%04x usButtonFlags=%04x usButtonData=%04x ulRawButtons=%04x lLastX=%04x lLastY=%04x ulExtraInformation=%04x\r\n"), 
            raw->data.mouse.usFlags, 
            raw->data.mouse.ulButtons, 
            raw->data.mouse.usButtonFlags, 
            raw->data.mouse.usButtonData, 
            raw->data.mouse.ulRawButtons, 
            raw->data.mouse.lLastX, 
            raw->data.mouse.lLastY, 
            raw->data.mouse.ulExtraInformation);

        if (FAILED(hResult))
        {
        // TODO: write error handler
        }
        OutputDebugString(szTempOutput);
    } 

    delete[] lpb; 
    return 0;
} 
```

## <a name="performing-a-buffered-read-of-raw-input"></a><span data-ttu-id="3271c-126">執行原始輸入的緩衝讀取</span><span class="sxs-lookup"><span data-stu-id="3271c-126">Performing a Buffered Read of Raw Input</span></span>

<span data-ttu-id="3271c-127">這個範例會示範應用程式如何從一般隱藏的原始輸入緩衝區讀取。</span><span class="sxs-lookup"><span data-stu-id="3271c-127">This sample shows how an application does a buffered read of raw input from a generic HID.</span></span>

```cpp
case MSG_GETRIBUFFER: // Private message
    {
    UINT cbSize;
    Sleep(1000);

    VERIFY(GetRawInputBuffer(NULL, &cbSize, sizeof(RAWINPUTHEADER)) == 0);
    cbSize *= 16; // up to 16 messages
    Log(_T("Allocating %d bytes"), cbSize);
    PRAWINPUT pRawInput = (PRAWINPUT)malloc(cbSize);
    if (pRawInput == NULL)
    {
        Log(_T("Not enough memory"));
        return;
    }

    for (;;)
    {
        UINT cbSizeT = cbSize;
        UINT nInput = GetRawInputBuffer(pRawInput, &cbSizeT, sizeof(RAWINPUTHEADER));
        Log(_T("nInput = %d"), nInput);
        if (nInput == 0)
        {
            break;
        }

        ASSERT(nInput > 0);
        PRAWINPUT* paRawInput = (PRAWINPUT*)malloc(sizeof(PRAWINPUT) * nInput);
        if (paRawInput == NULL)
        {
            Log(_T("paRawInput NULL"));
            break;
        }

        PRAWINPUT pri = pRawInput;
        for (UINT i = 0; i < nInput; ++i)
        {
            Log(_T(" input[%d] = @%p"), i, pri);
            paRawInput[i] = pri;
            pri = NEXTRAWINPUTBLOCK(pri);
        }

        free(paRawInput);
    }
    free(pRawInput);
}
```
