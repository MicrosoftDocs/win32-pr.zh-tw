---
title: 協助工具參數
description: 系統會維護一組協助工具參數，指出使用者是否有特殊需求或喜好設定需要應用程式變更其預設行為。
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f089b28d36ffa982ca6568996126a812263af9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966879"
---
# <a name="accessibility-parameters"></a>協助工具參數

系統會維護一組協助工具參數，指出使用者是否有特殊需求或喜好設定需要應用程式變更其預設行為。 使用者控制這些參數的狀態，通常是使用主控台中的輕鬆存取中心。 主控台可讓使用者自訂環境的應用程式或其他程式，可以使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來設定協助工具參數。

如果使用者變更這些參數，主控台傳送 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息。 應用程式應該會回應這則訊息，並使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 來判斷協助工具參數的狀態。 當存取範圍參數啟用時，應用程式應視需要修改其使用者介面，以配合使用者的喜好設定。

Windows 支援下列協助工具參數。



| 參數                                                                    | Description                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [High contrast](high-contrast-parameter.md)                                 | 指出應用程式應該在前景和背景視覺效果之間提供高對比。                                                                            |
| [鍵盤喜好設定](keyboard-preference-parameter.md)                     | 指出應用程式應該會顯示其他隱藏的鍵盤介面。                                                                                 |
| [螢幕助讀程式](screen-reader-parameter.md)                                 | 指出應用程式應該在以圖形方式呈現資訊的情況下，提供文字資訊。                                     |
| [顯示聲音 (和音訊描述旗標) ](showsounds-parameter.md) | 指出當應用程式使用音效傳達重要資訊，或是提供視覺元素的音訊描述時，也應該提供視覺效果或提示。 |
| [用戶端區域動畫](client-area-animation.md)                           | 指出應用程式應該遵守使用者喜好設定，以便在工作區中顯示動畫。                                                                       |
| [訊息持續時間](message-duration.md)                                     | 指出提供快顯通知的應用程式必須監視有關訊息持續時間的旗標，並調整其通知長度。                                  |



 

下列系統參數適用于協助工具應用程式。 如需詳細資訊，請參閱 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函數。



| 參數群組      | 參數                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 桌面參數   | SPI \_ GETWORKAREA、SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 輸入參數     | SPI \_ GETKEYBOARDCUES、SPI \_ GETKEYBOARDDELAY、SPI \_ GETKEYBOARDPREF，SPI \_ GETKEYBOARDSPEED，SPI \_ GETMESSAGEDURATION，SPI \_ GETMOUSE，SPI \_ GETMOUSEHOVERHEIGHT，SPI \_ GETMOUSEHOVERTIME，SPI \_ GETMOUSEHOVERWIDTH，SPI \_ GETMOUSESPEED，SPI \_ GETMOUSETRAILS，SPI GETSNAPTODEFBUTTON \_ ，SPI \_ GETWHEELSCROLLLINES， \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SPI SETDOUBLECLICKTIME，SPI SETDOUBLECLKHEIGHT，SPI SETDOUBLECLKWIDTH，SPI SETKEYBOARDCUES，SPI SETKEYBOARDDELAY，SPI SETKEYBOARDPREF，SPI SETKEYBOARDSPEED，SPI SETMOUSE，SPI SETMOUSEHOVERHEIGHT，SPI SETMOUSEHOVERTIME，SPI SETMOUSEHOVERWIDTH，SPI SETMOUSESPEED |
| UI 效果參數 | SPI \_ GETMENUUNDERLINES、SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 視窗參數    | SPI \_ GETCARETWIDTH、SPI \_ GETFOREGROUNDFLASHCOUNT、SPI \_ GETFOREGROUNDLOCKTIMEOUT、SPI \_ SETCARETWIDTH、SPI \_ SETDRAGHEIGHT、SPI \_ SETDRAGWIDTH、SPI \_ SETFOREGROUNDFLASHCOUNT、SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 協助工具功能](about-windows-accessibility-features.md)
</dt> </dl>

 

 