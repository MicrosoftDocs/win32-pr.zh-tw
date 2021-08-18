---
description: 裝置管理中會使用下列功能。
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: 裝置管理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a648fb5141d9efa977e573e3b0abb32fe6c504f11647a2dc392e9838da63ca6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956897"
---
# <a name="device-management-functions"></a>裝置管理函式

裝置管理中會使用下列功能。



| 函式                                                             | 描述                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | 將控制程式代碼直接傳送到指定的設備磁碟機。                           |
| [**InstallNewDevice**](installnewdevice.md)                         | 安裝新的裝置。 系統會提示使用者選取裝置。                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | 註冊視窗將接收通知的裝置或裝置類型。 |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | 關閉指定的裝置通知控制碼。                                      |



 

下列功能適用于 CD-ROM 和 DVD 光碟機。



| 函式                                                               | 描述                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | 停用指定 CD-ROM 或 DVD 光碟機的數位播放。                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | 啟用指定 CD-ROM 或 DVD 光碟機的數位播放。                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | 判斷指定的 CD-ROM 或 DVD 光碟機是否已啟用數位播放。               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | 判斷指定的 CD-ROM 或 DVD 光碟機是否有已知良好的數位播放。 |
| [**DvdLauncher**](dvdlauncher.md)                                     | 確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。                       |



 

 

 
