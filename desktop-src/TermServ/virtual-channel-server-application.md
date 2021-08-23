---
title: 虛擬通道伺服器應用程式
description: 使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。 請注意，您必須提供方法來啟動伺服器應用程式。
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a758f4860a0ab606f18c4a5086d305b1f627475bf7bab588648cea8aabd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423560"
---
# <a name="virtual-channel-server-application"></a>虛擬通道伺服器應用程式

使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。 請注意，您必須提供方法來啟動伺服器應用程式。 您可以透過多種方式達成此目的;例如，您可以使用登入腳本，或是開機檔案夾中的程式或腳本。 使用者也可以啟動應用程式。

您必須在下列位置下新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **終端機伺服器** 的 \\ **載入** 宏

如需子機碼的詳細資訊，請參閱 [監視會話連線和中斷連接](monitoring-session-connections-and-disconnections.md)。

伺服器應用程式可以呼叫 [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) 函數來開啟虛擬通道的控制碼。 然後，應用程式可以使用下列任何一個函式中的控制碼。

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

關閉開啟的虛擬通道控制碼。

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

刪除從用戶端傳送到特定虛擬通道上伺服器的所有已排入佇列的輸入資料。

> [!Note]  
> 遠端桌面服務目前未使用此函數。

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

刪除從伺服器傳送至特定虛擬通道上之用戶端的所有已排入佇列的輸出資料。

> [!Note]  
> 遠端桌面服務目前未使用此函數。

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

傳回指定虛擬通道的相關資訊。

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

從虛擬通道的伺服器端讀取資料。

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

將資料寫入虛擬通道的伺服器端。

</dd> </dl>

 

 




