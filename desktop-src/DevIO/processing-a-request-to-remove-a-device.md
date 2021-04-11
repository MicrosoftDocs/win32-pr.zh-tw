---
description: '\_當系統中的功能決定移除指定的裝置時，應用程式會收到 DBT DEVICEQUERYREMOVE 裝置事件。'
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: 處理移除裝置的要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110688"
---
# <a name="processing-a-request-to-remove-a-device"></a><span data-ttu-id="6f362-103">處理移除裝置的要求</span><span class="sxs-lookup"><span data-stu-id="6f362-103">Processing a Request to Remove a Device</span></span>

<span data-ttu-id="6f362-104">當系統中的功能決定移除指定的裝置時，應用程式會收到 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="6f362-104">An application receives a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event when a feature in the system has decided to remove a specified device.</span></span> <span data-ttu-id="6f362-105">當應用程式收到此事件時，它應該判斷它是否使用指定的裝置，並取消或準備移除。</span><span class="sxs-lookup"><span data-stu-id="6f362-105">When the application receives this event, it should determine whether it is using the specified device and either cancel or prepare for the removal.</span></span>

<span data-ttu-id="6f362-106">在下列範例中，應用程式會將開啟的控制碼 hFile 維持在檔案名所代表的檔案或裝置上。</span><span class="sxs-lookup"><span data-stu-id="6f362-106">In the following example, an application maintains an open handle, hFile, to the file or device represented by FileName.</span></span> <span data-ttu-id="6f362-107">應用程式會藉由呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 函式，在基礎裝置上註冊裝置事件通知，方法是使用 **DBT \_ DEVTYP \_ 控制碼** 類型通知篩選器，並在篩選的 **dbch \_ 控制碼** 成員中指定 hFile 變數。</span><span class="sxs-lookup"><span data-stu-id="6f362-107">The application registers for device event notification on the underlying device by calling the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function, using a **DBT\_DEVTYP\_HANDLE** type notification filter and specifying the hFile variable in the **dbch\_handle** member of the filter.</span></span>

<span data-ttu-id="6f362-108">應用程式會藉由關閉要移除之裝置的開啟檔案控制代碼，來處理 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="6f362-108">The application processes the [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event by closing the open file handle to the device that is to be removed.</span></span> <span data-ttu-id="6f362-109">在取消移除此裝置的事件中，應用程式會處理 [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) 裝置事件，以重新開啟裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6f362-109">In the event that removal of this device is canceled, the application processes the [DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) device event to reopen the handle to the device.</span></span> <span data-ttu-id="6f362-110">從系統移除裝置之後，應用程式會藉由取消登錄裝置的通知控制碼，並關閉仍在裝置上開啟的任何控制碼，來處理 [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) 和 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="6f362-110">After the device has been removed from the system, the application processes the [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) device events by unregistering its notification handle for the device and closing any handles that are still open to the device.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="6f362-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f362-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f362-112">裝置事件種類</span><span class="sxs-lookup"><span data-stu-id="6f362-112">Device Event Types</span></span>](device-event-types.md)
</dt> </dl>

 

 



