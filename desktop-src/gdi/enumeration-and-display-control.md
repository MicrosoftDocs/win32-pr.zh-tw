---
description: 若要列舉電腦上的所有裝置，請呼叫 EnumDisplayDevices 函式。 傳回的資訊也會指出哪一個監視器是桌面的一部分。
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: 列舉和顯示控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026459"
---
# <a name="enumeration-and-display-control"></a>列舉和顯示控制項

若要列舉電腦上的所有裝置，請呼叫 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) 函式。 傳回的資訊也會指出哪一個監視器是桌面的一部分。

若要列舉桌面上與裁剪區域相交的裝置，請呼叫 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)。 這會將 HMONITOR 控制碼傳回給每個使用 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)的監視器。 若要列舉虛擬螢幕中的所有裝置，請使用 **EnumDisplayMonitors**。 如下列程式碼所示：


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



若要取得顯示裝置的相關資訊，請使用 [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) 或 [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)。

[**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa)函式是用來控制電腦上的顯示裝置。 它可以修改裝置的設定，例如指定監視器在虛擬桌面上的位置，以及變更任何顯示器的位深度。 一般來說，應用程式不會使用此函式。 若要以程式設計的方式將顯示監視器新增至多重監視器系統，請將 **dmFields** 設定為 DM \_ 定位，並為您要新增的監視指定位置 (dmPosition ) ，而這是與現有監視器之顯示區域中至少一個圖元連續的位置 **。** 若要卸離監視器，請將 **dmFields** 設定為 DM \_ 位置，並將 **DmPelsWidth** 和 **devmode. dmPelsHeight** 設定為零。

下列程式碼示範如何從桌面卸離所有次要顯示裝置：


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



針對每個顯示裝置，應用程式可以將資訊儲存在登錄中，以描述裝置的設定參數，以及位置參數。 應用程式也可以判斷哪些顯示器是桌面的一部分，而不是透過 \_ \_ 連接 \_ 到 \_ [**顯示 \_ 設備**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) 結構中桌面旗標的顯示裝置。 一旦所有設定資訊都儲存在登錄中，應用程式就可以再次呼叫 [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) ，以動態方式變更設定，而不需要重新開機。

 

 



