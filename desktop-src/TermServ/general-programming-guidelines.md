---
title: 一般程式設計指導方針
description: 在遠端桌面服務環境中開發應用程式的指導方針。
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b0e83daa98f59390408fa43f5c5f83ff547e3d0cad665d29922f4244913361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353879"
---
# <a name="general-programming-guidelines"></a>一般程式設計指導方針

下列各節提供在遠端桌面服務環境中開發應用程式的一般方針。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[應用程式相容性層](application-compatibility-layer.md)
</dt> <dd>

若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。

</dd> <dt>

[用戶端/伺服器應用程式指導方針](client-server-application-guidelines.md)
</dt> <dd>

用戶端/伺服器應用程式不能假設單一電腦連接相當於單一使用者會話。

</dd> <dt>

[監視會話連線和中斷連接](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

若要向遠端桌面服務註冊應用程式，請新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中。

</dd> <dt>

[週邊硬體指導方針](peripheral-hardware-guidelines.md)
</dt> <dd>

如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。

</dd> <dt>

[執行時間連結至 Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

您的應用程式可以使用遠端桌面服務 API，在執行時間動態連結到 Wtsapi32.dll。 若要這樣做，您的應用程式應該呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Wtsapi32.dll。

</dd> </dl>

 

 