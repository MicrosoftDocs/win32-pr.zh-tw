---
description: 當電源管理事件發生時，系統會將訊息廣播至所有應用程式和可安裝的驅動程式。
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983630"
---
# <a name="wm_powerbroadcast-messages"></a>WM \_ POWERBROADCAST 訊息

當電源管理事件發生時，系統會將訊息廣播至所有應用程式和可安裝的驅動程式。 系統會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息來廣播這些事件，並將 *wParam* 參數設定為適當的電源管理事件。 例如， [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) 事件表示系統電源狀態變更。 您必須確保您的應用程式能夠正確地回應 **WM \_ POWERBROADCAST** 訊息。

系統會在暫停操作之前，立即廣播 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件。 這讓應用程式和驅動程式最後有機會為事件做好準備。 在許多情況下，系統會在不要求許可權的情況下廣播這些訊息。 例如，如果應用程式使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函式來強制暫停，就會發生這種情況。

系統作業還原後，系統會廣播 [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) 或 [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) 事件。 如果應用程式在暫停電腦之前收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件，它會收到 PBT \_ APMRESUMESUSPEND 事件。 否則，它會收到 PBT \_ APMRESUMECRITICAL 事件。

系統會將 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) 事件傳送至使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification)註冊特定事件的應用程式。 如需詳細資訊，請參閱 [註冊電源事件](registering-for-power-events.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> </dl>

 

 



