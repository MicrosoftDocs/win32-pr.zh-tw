---
description: '\_當新的裝置或媒體 (（例如 CD 或 DVD) 新增並變成可用，以及移除現有的裝置或媒體時），windows 會將一組預設的 WM DEVICECHANGE 訊息傳送給所有最上層 windows。'
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: 偵測媒體插入或移除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116053"
---
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="50a2f-103">偵測媒體插入或移除</span><span class="sxs-lookup"><span data-stu-id="50a2f-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="50a2f-104">當新的裝置或媒體 (（例如 CD 或 DVD) 新增並變成可用，以及移除現有的裝置或媒體時），windows 會將一組預設的 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息傳送給所有最上層 windows。</span><span class="sxs-lookup"><span data-stu-id="50a2f-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="50a2f-105">您不需要註冊來接收這些預設訊息。</span><span class="sxs-lookup"><span data-stu-id="50a2f-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="50a2f-106">如需預設傳送訊息的詳細資訊，請參閱 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="50a2f-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="50a2f-107">下列程式碼範例中的訊息會在預設訊息中。</span><span class="sxs-lookup"><span data-stu-id="50a2f-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="50a2f-108">Windows 只會將 CD 或 DVD 媒體事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息傳送到在 active 主控台會話中執行的應用程式所擁有的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="50a2f-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="50a2f-109">在遠端桌面會話中執行的應用程式所擁有的最上層視窗，不會收到 CD 或 DVD 媒體事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="50a2f-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="50a2f-110">每個 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息都有相關聯的事件可描述變更，以及提供有關變更之詳細資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="50a2f-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="50a2f-111">此結構包含事件獨立的標頭、 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)，後面接著事件相依的成員。</span><span class="sxs-lookup"><span data-stu-id="50a2f-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="50a2f-112">事件相依的成員描述要套用事件的裝置。</span><span class="sxs-lookup"><span data-stu-id="50a2f-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="50a2f-113">若要使用此結構，應用程式必須先判斷事件種類和裝置類型。</span><span class="sxs-lookup"><span data-stu-id="50a2f-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="50a2f-114">然後，他們可以使用正確的結構來採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="50a2f-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="50a2f-115">當使用者將新的 CD 或 DVD 插入磁片磁碟機時，應用程式會收到具有 [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="50a2f-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="50a2f-116">應用程式必須檢查事件，以確保抵達的裝置類型為磁片區 (**dbch \_ devicetype** 成員是 **DBT \_ DEVTYP \_ volume**) 而且變更會影響媒體 (**dbcv \_ 旗標** 成員是 **DBTF \_ 媒體**) 。</span><span class="sxs-lookup"><span data-stu-id="50a2f-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="50a2f-117">當使用者從磁片磁碟機移除 CD 或 DVD 時，應用程式會收到具有 [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="50a2f-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="50a2f-118">同樣地，應用程式必須檢查事件，以確定要移除的裝置是磁片區，且變更會影響媒體。</span><span class="sxs-lookup"><span data-stu-id="50a2f-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="50a2f-119">下列程式碼示範如何檢查 CD 或 DVD 的插入或移除。</span><span class="sxs-lookup"><span data-stu-id="50a2f-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a><span data-ttu-id="50a2f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="50a2f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50a2f-121">裝置事件</span><span class="sxs-lookup"><span data-stu-id="50a2f-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



