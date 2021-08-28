---
description: 從 Windows Vista 開始，tablet pc 技術支援 tablet pc 上的觸控輸入，並具備觸控功能的數位化器。 這項支援包括增強的使用者介面，可協助您在使用手指進行輸入時，將 Windows 設為目標和命令。
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Windows Vista 中的觸控輸入支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b22130a7c731d49556db263d5c1d5565ef51aa103925969b35c98548a32d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335068"
---
# <a name="touch-input-support-in-windows-vista"></a>Windows Vista 中的觸控輸入支援

從 Windows Vista 開始，tablet pc 技術支援 tablet pc 上的觸控輸入，並具備觸控功能的數位化器。 這項支援包括增強的使用者介面，可協助您在使用手指進行輸入時，將 Windows 設為目標和命令。

## <a name="touch-digitizer-support"></a>Touch 數位化器支援

### <a name="pen-and-touch-input-not-exclusive"></a>畫筆和觸控輸入非獨佔

請勿假設 [**InkCollector**](inkcollector-class.md)、 [**InkOverlay**](inkoverlay-class.md)和 [**RealTimeStylus**](realtimestylus-class.md) 應用程式中的畫筆和觸控輸入互斥。

在 Windows Vista 中，當系統辨識畫筆時，會忽略觸控輸入。 也就是說，觸控筆觸會結束，且筆刷筆觸會開始。 因為未來可能會變更，所以您的程式碼不應假設畫筆和觸控輸入互斥。

### <a name="other-mouse-message-sources"></a>其他滑鼠訊息來源

即使使用者只是使用手指或畫筆進行互動，也有其他的滑鼠訊息來源。 來源包括 touchpads，以及要讓分層視窗後方的應用程式知道滑鼠正在移至應用程式上方的移動。

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>啟用和停用觸控輸入消費者介面

視應用程式的需求而定，您可能會想要啟用或停用觸控輸入使用者介面。 若要完成此動作，請攔截視窗程式中的作業系統視窗訊息，並修改 Windows 訊息。 覆寫應用程式中的 [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) 來攔截這些訊息。 下列 C \# 程式碼顯示如何啟用和停用觸控輸入使用者介面。 程式碼也會顯示如何使用相同的技術來停用按住不放手勢。 此方法也適用于停用手寫筆。


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows觸摸](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
