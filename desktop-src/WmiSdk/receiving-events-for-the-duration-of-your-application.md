---
description: 接收事件的其中一個最常見的方法是透過執行中的應用程式，例如，可收集並向使用者顯示事件的管理應用程式。
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: 在您的應用程式期間接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554216"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>在您的應用程式期間接收事件

接收事件的其中一個最常見的方法是透過執行中的應用程式，例如，可收集並向使用者顯示事件的管理應用程式。 這類應用程式稱為「暫時性」，因為暫時性取用者不會在關閉時收到事件通知。

暫時性取用者會呼叫腳本中的 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ，或在 c + + 中 [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ，以訂閱命名空間中的事件。 與此訂用帳戶相關聯的身分識別是呼叫者。

暫存事件取用者可以在腳本和 c + + 中非同步或半同步方式接收通知。

> [!Note]  
> 基於安全性理由，請務必注意，不建議使用非同步事件通知。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。 事件取用者具有特殊的安全性考慮。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。

 

如需接收非同步事件和同步事件通知的詳細資訊，請參閱 [接收非同步事件通知](receiving-asynchronous-event-notifications.md) 和 [接收半同步事件通知](receiving-synchronous-and-semisynchronous-event-notifications.md)。

 

 



