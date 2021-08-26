---
title: 裝置主機安全性考慮
description: 使用裝置主機會產生安全性問題。
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008088"
---
# <a name="device-host-security-considerations"></a>裝置主機安全性考慮

使用裝置主機會因為下列原因而產生安全性問題：

-   在執行 Windows XP 的電腦上主控的裝置會在所有網路上傳送公告。
-   在執行 Windows XP 的電腦上裝載的裝置，可讓您控制所有網路中的裝置。

這會增加家用取用者的風險，因為在執行 Windows XP 的電腦上所裝載的裝置（例如媒體播放機或橋接光源或 HVAC 系統）會顯示出來，而且可以從家裡以外的控制點控制。

當您建立託管裝置時，您必須考慮一些安全性問題。

-   為了減少探索和攻擊 UPnP 型裝置的範圍，所有 SSDP 訊息的 TTL 都是1。 這表示已註冊的裝置只會由相同網路上的控制點來探索。 您可以在登錄中設定較高的 TTL。
-   註冊非執行中的裝置需要預先向 COM 註冊裝置 .dll，這需要系統管理員許可權。
-   註冊正在執行的裝置需要系統管理員、本機服務或本機系統許可權。
-   當裝置主機啟動時，它會以 [LocalService](/windows/desktop/Services/localservice-account)的形式執行。 這讓裝置能夠產生審核和讀取 **HKEY \_ 本機 \_ 電腦** 登錄機碼。 裝置可以存取 **HKEY \_ 目前的 \_ 使用者**。 LocalService 帳戶可以使用已授與 LocalService 存取權的資源，以及授與存取權給 AuthenticatedUser 的資源。 裝置具有受限的檔案系統存取權。
-   必須更新檔案系統 Acl，以允許 [LocalService](/windows/desktop/Services/localservice-account) 存取資原始目錄。
-   如果您的裝置必須有更多的安全性存取權，您可以為裝置建立自己的進程，並使用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)來註冊它。

 

 