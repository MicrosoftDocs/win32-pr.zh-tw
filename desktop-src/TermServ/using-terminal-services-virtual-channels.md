---
title: 使用遠端桌面服務的虛擬通道
description: 若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f538259134d539104e55706578778931a1180a1901a9891eec7f62f1f40144b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423738"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>使用遠端桌面服務的虛擬通道

若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。 伺服器模組可以是使用者模式應用程式或核心模式驅動程式。 用戶端模組必須是 DLL。

如需這些模組的說明，請參閱下列主題。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[虛擬通道伺服器應用程式](virtual-channel-server-application.md)
</dt> <dd>

使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。 請注意，您必須提供方法來啟動伺服器應用程式。

</dd> <dt>

[虛擬通道用戶端 DLL](virtual-channel-client-dll.md)
</dt> <dd>

虛擬通道應用程式的用戶端是在用戶端電腦上遠端桌面服務初始化期間載入的 DLL。 您必須在用戶端電腦上註冊 DLL。

</dd> <dt>

[虛擬通道用戶端註冊](virtual-channel-client-registration.md)
</dt> <dd>

您必須將用戶端 DLL 的名稱儲存在登錄中。

</dd> <dt>

[遠端控制持續性虛擬通道](remote-control-persistent-virtual-channels.md)
</dt> <dd>

遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。 資料將繼續透過此通道傳送和接收。

</dd> <dt>

[動態虛擬通道](dynamic-virtual-channels.md)
</dt> <dd>

動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。

</dd> </dl>

如果您已在遠端桌面服務部署中啟用虛擬通道的應用程式，您也可以透過遠端桌面 ActiveX 控制項，將應用程式提供給存取 RD 工作階段主機伺服器的用戶端電腦使用。 如需詳細資訊，請參閱[使用遠端桌面 ActiveX 控制項搭配虛擬通道](using-the-remote-desktop-activex-control-with-virtual-channels.md)。

 

 




