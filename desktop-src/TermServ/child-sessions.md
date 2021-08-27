---
title: 子會話
description: 從 Windows Server 2012 和 Windows 8 開始，遠端桌面支援子會話的概念，也就是系結至使用者現有會話的特殊回送遠端桌面會話。
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d79fa6e18cece69c672b60a65e679441ce986a6cd8a0ad46524440738c3844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010418"
---
# <a name="child-sessions"></a>子會話

從 Windows Server 2012 和 Windows 8 開始，遠端桌面支援 *子會話* 的概念，也就是系結至使用者現有會話的特殊回送遠端桌面會話。

下列作業系統不支援子會話：

<dl> Windows RT  
Windows Server 2012Server Core 安裝選項  
Microsoft Hyper-V Server 2012  
</dl>

在任何指定時間，系統一次只能有一個作用中且已連線的子會話。

您可以直接登出子會話，或在父會話終止時將其終止。

您必須藉由呼叫 [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) 函式來啟用子會話功能，才可以在系統上使用子會話。 您也可以使用 [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) 函式來判斷子會話是否已啟用。

只有在連接之前，您可以使用 [遠端桌面 ActiveX 控制項](remote-desktop-activex-control.md)，並使用 [**IMsRdpExtendedSettings**](imsrdpextendedsettings-property.md)設定 "ConnectToChildSession" 屬性，以在現有使用者的會話內建立子會話。 呼叫 [**連線 IMsTscAx**](imstscax-connect.md)方法時，除非使用者使用智慧卡登入父會話，否則遠端桌面 ActiveX 控制項會自動登入子會話，而不會提示輸入認證。 不同于一般的遠端桌面會話，使用者不需要遠端互動式許可權即可登入子會話，因為這是回送會話。

子會話無法鎖定。 它不會有螢幕保護裝置和登入畫面。 此外，與一般會話不同的是，如果設定 WinLogon 登入文字原則，登入文字將不會顯示在此子會話中。 此外，如果已設定這些原則，子會話的遠端桌面連線 Timeout 群組原則就不會有任何影響。

下列 Api 會與子會話搭配使用：

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   IMsRdpExtendedSettings 中的 "ConnectToChildSession" 屬性 [ **。屬性**](imsrdpextendedsettings-property.md)

 

 




