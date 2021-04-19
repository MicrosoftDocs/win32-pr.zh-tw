---
description: 本主題說明在使用影片捕獲裝置時，如何偵測裝置遺失。
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: 處理影片裝置遺失
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993009"
---
# <a name="handling-video-device-loss"></a><span data-ttu-id="0f881-103">處理影片裝置遺失</span><span class="sxs-lookup"><span data-stu-id="0f881-103">Handling Video Device Loss</span></span>

<span data-ttu-id="0f881-104">本主題說明在使用影片捕獲裝置時，如何偵測裝置遺失。</span><span class="sxs-lookup"><span data-stu-id="0f881-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="0f881-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="0f881-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="0f881-106">註冊裝置通知</span><span class="sxs-lookup"><span data-stu-id="0f881-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="0f881-107">取得裝置的符號連結</span><span class="sxs-lookup"><span data-stu-id="0f881-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="0f881-108">處理 WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="0f881-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="0f881-109">取消註冊通知</span><span class="sxs-lookup"><span data-stu-id="0f881-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="0f881-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f881-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="0f881-111">註冊裝置通知</span><span class="sxs-lookup"><span data-stu-id="0f881-111">Register For Device Notification</span></span>

<span data-ttu-id="0f881-112">從裝置開始捕獲之前，請先呼叫 [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) 函式來註冊裝置通知。</span><span class="sxs-lookup"><span data-stu-id="0f881-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="0f881-113">註冊 **KSCATEGORY \_ CAPTURE** 裝置類別，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="0f881-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="0f881-114">取得裝置的符號連結</span><span class="sxs-lookup"><span data-stu-id="0f881-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="0f881-115">列舉系統上的影片裝置，如 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="0f881-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="0f881-116">從清單中選擇裝置，然後查詢 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ] 屬性的啟用物件，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="0f881-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a><span data-ttu-id="0f881-117">處理 WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="0f881-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="0f881-118">在您的訊息迴圈中，聆聽 [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0f881-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="0f881-119">*LParam* message 參數是 [**開發 \_ 廣播 \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0f881-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



<span data-ttu-id="0f881-120">接下來，根據裝置的符號連結來比較裝置通知訊息，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0f881-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="0f881-121">檢查 [**DEV \_ 廣播 \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)結構的 **dbch \_ devicetype** 成員。</span><span class="sxs-lookup"><span data-stu-id="0f881-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="0f881-122">如果值是 **DBT \_ DEVTYP \_ DEVICEINTERFACE**，請將結構指標轉換成 [**開發 \_ 廣播 \_ DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) 結構。</span><span class="sxs-lookup"><span data-stu-id="0f881-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="0f881-123">比較此結構的 **dbcc \_ 名稱** 成員與裝置的符號連結。</span><span class="sxs-lookup"><span data-stu-id="0f881-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a><span data-ttu-id="0f881-124">取消註冊通知</span><span class="sxs-lookup"><span data-stu-id="0f881-124">Unregister For Notification</span></span>

<span data-ttu-id="0f881-125">在應用程式結束之前，呼叫 [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) 以取消註冊裝置通知/</span><span class="sxs-lookup"><span data-stu-id="0f881-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="0f881-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f881-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f881-127">列舉影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="0f881-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="0f881-128">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="0f881-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
