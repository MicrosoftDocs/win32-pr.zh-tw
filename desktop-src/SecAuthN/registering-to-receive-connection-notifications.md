---
description: 建立要接收連線通知的 DLL 之後，您必須向系統註冊。
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: 註冊以接收連接通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3a25e26e290700b8f343d3d543af4fbd7b709ff8b099522e4cd4b02b3d587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919471"
---
# <a name="registering-to-receive-connection-notifications"></a>註冊以接收連接通知

建立要接收連線通知的 DLL 之後，您必須向系統註冊。 若要這麼做，請在下列情況下新增 **REG \_ EXPAND \_ SZ** 值

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **Notifyees**

金鑰。 這個值會指定執行 [連接通知 API](connection-notification-api.md)之 DLL 的路徑。

值可以有任何名稱。 **Notifyees** 索引鍵下的所有值都會被視為連接事件通知之 dll 的路徑。 建議您使用可識別 DLL 的名稱。 這樣就能減少與其他連接通知應用程式發生名稱衝突的機率。

如需有關如何建立可接收連線通知的應用程式的詳細資訊，請參閱 [接收連接](receiving-connection-notifications.md)通知。

 

 



