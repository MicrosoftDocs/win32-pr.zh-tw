---
title: 提供 RDP 用戶端安全性
description: 遠端桌面 ActiveX 控制項物件的某些屬性會限制為特定 Internet Explorer URL 安全性區域。
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdcfbc2b26363ff7f13ed15b3486249aab804cd1bde418f60d71db918f25567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940612"
---
# <a name="providing-for-rdp-client-security"></a>提供 RDP 用戶端安全性

為了讓用戶端免于受到可能無法信任的伺服器的攻擊，遠端桌面 ActiveX control 物件的某些屬性會限制為特定 Internet Explorer URL 安全性區域。 這表示，當流覽 web 的使用者存取頁面，而且頁面的 URL 安全性區域與流覽 web 的電腦不同時，會停用這些屬性。 這些受限制的屬性可使用 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面和 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面來存取，並可在下列 Internet Explorer URL 安全性區域中取得：

-   我的電腦
-   近端內部網路
-   信任的網站

這些區域會在這些區域中停用：

-   網際網路
-   限制的網站

如果您在遠端桌面服務 web 應用程式中呼叫這些受限制的屬性，您應該呼叫 [**IMsTscAx：： get \_ SecuredSettings**](imstscax-securedsettings.md)和 [**IMsTscAx：： Get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)來存取受保護的設定屬性。

**IMsTscSecuredSettings** 介面所存取的受限制屬性如下：

-   [**StartProgram**](imstscsecuredsettings-startprogram.md)。 這個屬性會指定將在連接時啟動的程式。
-   [**WorkDir**](imstscsecuredsettings-workdir.md)。 這個屬性會指定 [**StartProgram**](imstscsecuredsettings-startprogram.md)中指定之程式的工作目錄。
-   [**全螢幕**](imstscsecuredsettings-fullscreen.md)。 這個屬性會指定連接時的控制項狀態是處於全螢幕模式或視窗模式。 如果這個屬性的值為 **TRUE**，將會以全螢幕模式開啟連接。 雖然使用 [ **全** 螢幕] 屬性僅限於先前所列的 Internet Explorer URL 安全性區域，但是在連線之後，使用者隨時都可以按 [全螢幕模式] [快速鍵](terminal-services-shortcut-keys.md) 組合，變更為全螢幕模式 (CTRL + ALT + BREAK) 。

**IMsRdpClientSecuredSettings** 介面所存取的屬性如下：

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)。 這個屬性會指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)。 這個屬性會指定套用 Windows 機碼組合的方式和時間;例如，ALT + TAB。

下列腳本會在連接時啟動 Microsoft Notepad.exe。 在呼叫 [**IMsTscAx：：連線**](imstscax-connect.md)方法之前，請先執行此腳本。

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




