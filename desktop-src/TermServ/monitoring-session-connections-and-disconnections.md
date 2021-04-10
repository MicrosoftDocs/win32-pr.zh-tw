---
title: 監視會話連線和中斷連接
description: 若要向遠端桌面服務註冊應用程式，請新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中。
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023580"
---
# <a name="monitoring-session-connections-and-disconnections"></a>監視會話連線和中斷連接

針對服務應用程式（例如虛擬通道伺服器應用程式），若要監視會話連線和中斷連接，您必須向遠端桌面服務註冊。 若要向遠端桌面服務註冊應用程式，請在下列位置下新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **TerminalServer** \\ **載入** 宏

子機碼可以有任何名稱。 它必須有一個包含應用程式符號名稱的 **REG \_ SZ** 值 **name**。

``` syntax
Name = AddinName
```

子機碼和 **Name** 值的最大長度為99個字元。

子機碼也必須有指示伺服器應用程式類型的 **REG \_ DWORD** 值。

``` syntax
Type = AddinType
```

*AddinType* 必須是下列值。



| 值 | 意義                               |
|-------|---------------------------------------|
| 3     | 使用者模式應用程式、會話空間。 |



 

服務應用程式的註冊只會在執行註冊之後建立的會話中生效。

針對每個已註冊的服務應用程式，遠端桌面服務會在用戶端連接或中斷會話的連線時，發出一組事件物件的信號。 每個虛擬通道外掛程式都必須註冊自己，並藉由呼叫 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)來建立通知事件。 這些事件物件的名稱會遵循下列格式。

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName* 是在註冊伺服器應用程式所用之登錄子機碼的 **名稱** 值中所指定的字串。 在會話下建立這些事件，會在特定的每個會話事件目錄中建立這些事件。 事件目錄可以防止其他會話中的應用程式修改這些事件的狀態，以提供額外的安全性。

若要控制是否要在伺服器上收到重新連接和中斷連接事件，您可以在登錄中將 **RemoteControlPersistent** 旗標放在下列機碼底下：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **TerminalServer** \\ **載入** 宏 \\ *addinname*

旗標可啟用或停用在用戶端會話啟動或停止時發出的重新連接和中斷線上活動。 **REG \_ DWORD** 值的語法如下所示。

``` syntax
RemoteControlPersistent = flag
```

*旗* 標的值可以是一或零。 預設值為零。 如果設定為1，當用戶端會話啟動或停止時，服務應用程式將不會收到通知。 如果設定為零，當用戶端會話啟動時，重新連接事件就會收到信號，並在用戶端會話停止時發出中斷線上活動。

在 Windows Server 2008 中仍支援先前的事件物件名稱格式，以提供回溯相容性。 建議您使用較新的 Windows Server 2008 格式，因為它比較安全。

先前的事件格式如下所示。

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName* 是在註冊伺服器應用程式所用之登錄子機碼的 **名稱** 值中所指定的字串。 *SessionId* 是用戶端會話的會話識別碼。

 

 