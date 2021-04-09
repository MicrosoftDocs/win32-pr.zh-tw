---
description: 每一部伺服器都可以在登錄中設定 MachineID 登錄機碼值，此值會設定為會話識別碼的固定部分。
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: 使用 Schannel 的負載平衡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849612"
---
# <a name="load-balancing-using-schannel"></a>使用 Schannel 的負載平衡

每一部伺服器都可以在登錄中設定 MachineID 登錄機碼值，此值會設定為會話識別碼的固定部分。 MachineID 登錄機碼是 **REG \_ DWORD** 值型別。 負載平衡器可以使用會話識別碼的這個部分，判斷哪一部伺服器已產生 SSL 會話，並可維護該伺服器的對應。 會話識別碼是透過網路傳送的 SSL/TLS 信號交換的一部分。 繼續或重新連線至用戶端時，負載平衡器程式碼應該使用會話識別碼中的第二個 **DWORD** 。 Schannel 伺服器所產生之隨機會話識別碼的第二個 **dword** 會由登錄中儲存的 **DWORD** 取代。 **DWORD** 的登錄值不可為0xffffffff。

登錄機碼值如下所示。

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 



