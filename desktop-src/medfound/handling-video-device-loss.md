---
description: 本主題說明在使用影片捕獲裝置時，如何偵測裝置遺失。
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: 處理影片裝置遺失
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6219518d3018aae5600e66387363bbd71e29e72b83174b370bf25377c8c6b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878950"
---
# <a name="handling-video-device-loss"></a>處理影片裝置遺失

本主題說明在使用影片捕獲裝置時，如何偵測裝置遺失。 它包含下列區段：

-   [註冊裝置通知](#register-for-device-notification)
-   [取得裝置的符號連結](#get-the-symbolic-link-of-the-device)
-   [處理 WM \_ DEVICECHANGE](/windows)
-   [取消註冊通知](#unregister-for-notification)
-   [相關主題](#related-topics)

## <a name="register-for-device-notification"></a>註冊裝置通知

從裝置開始捕獲之前，請先呼叫 [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) 函式來註冊裝置通知。 註冊 **KSCATEGORY \_ CAPTURE** 裝置類別，如下列程式碼所示。


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



## <a name="get-the-symbolic-link-of-the-device"></a>取得裝置的符號連結

列舉系統上的影片裝置，如 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)中所述。 從清單中選擇裝置，然後查詢 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ] 屬性的啟用物件，如下列程式碼所示。


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



## <a name="handle-wm_devicechange"></a>處理 WM \_ DEVICECHANGE

在您的訊息迴圈中，聆聽 [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) 訊息。 *LParam* message 參數是 [**開發 \_ 廣播 \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)結構的指標。


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



接下來，根據裝置的符號連結來比較裝置通知訊息，如下所示：

1.  檢查 [**DEV \_ 廣播 \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)結構的 **dbch \_ devicetype** 成員。 如果值是 **DBT \_ DEVTYP \_ DEVICEINTERFACE**，請將結構指標轉換成 [**開發 \_ 廣播 \_ DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) 結構。
2.  比較此結構的 **dbcc \_ 名稱** 成員與裝置的符號連結。


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



## <a name="unregister-for-notification"></a>取消註冊通知

在應用程式結束之前，呼叫 [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) 以取消註冊裝置通知/


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉影片捕獲裝置](enumerating-video-capture-devices.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 
