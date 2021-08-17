---
description: '\_當新的裝置或媒體 (（例如 CD 或 DVD) ）新增並變成可用，以及移除現有的裝置或媒體時，Windows 會將一組預設的 WM DEVICECHANGE 訊息傳送給所有最上層 Windows。'
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: 偵測媒體插入或移除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3f6d579ed654ae2d2f77d00f70b88dc1441d03bbce59c0f8cb39ca6800c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318348"
---
# <a name="detecting-media-insertion-or-removal"></a>偵測媒體插入或移除

當新的裝置或媒體 (（例如 CD 或 DVD) ）新增並變成可用，以及移除現有的裝置或媒體時，Windows 會將一組預設的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息傳送給所有最上層 Windows。 您不需要註冊來接收這些預設訊息。 如需預設傳送訊息的詳細資訊，請參閱 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 中的「備註」一節。 下列程式碼範例中的訊息會在預設訊息中。

> [!Note]  
> Windows 只會將 CD 或 DVD 媒體事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息傳送到在 active 主控台會話中執行的應用程式所擁有的最上層視窗。 在遠端桌面會話中執行的應用程式所擁有的最上層視窗，不會收到 CD 或 DVD 媒體事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息。

 

每個 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息都有相關聯的事件可描述變更，以及提供有關變更之詳細資訊的結構。 此結構包含事件獨立的標頭、 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)，後面接著事件相依的成員。 事件相依的成員描述要套用事件的裝置。 若要使用此結構，應用程式必須先判斷事件種類和裝置類型。 然後，他們可以使用正確的結構來採取適當的動作。

當使用者將新的 CD 或 DVD 插入磁片磁碟機時，應用程式會收到具有 [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息。 應用程式必須檢查事件，以確保抵達的裝置類型為磁片區 (**dbch \_ devicetype** 成員是 **DBT \_ DEVTYP \_ volume**) 而且變更會影響媒體 (**dbcv \_ 旗標** 成員是 **DBTF \_ 媒體**) 。

當使用者從磁片磁碟機移除 CD 或 DVD 時，應用程式會收到具有 [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)事件的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息。 同樣地，應用程式必須檢查事件，以確定要移除的裝置是磁片區，且變更會影響媒體。

下列程式碼示範如何檢查 CD 或 DVD 的插入或移除。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置事件](device-events.md)
</dt> </dl>

 

 



