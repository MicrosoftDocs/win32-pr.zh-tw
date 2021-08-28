---
title: 連接狀態
description: 在連接到遠端伺服器的過程中，遠端存取連線管理員和遠端電腦上的 RAS 伺服器會執行幾個步驟來建立連線。
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e52e1e4ea4a071f6606681aa2dc2fc15e88df659f8fd16746abf2d84727d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074218"
---
# <a name="connection-states"></a>連接狀態

在連接到遠端伺服器的過程中，遠端存取連線管理員和遠端電腦上的 RAS 伺服器會執行幾個步驟來建立連線。 每個步驟都是由連接狀態所識別。 [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))列舉是對應至這些連接狀態的一組值。 連接狀態可以分成下列三個群組：

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>正在執行狀態
</dt> <dd>

「執行中」狀態是 RAS 自動處理的連接作業部分，例如連接到必要的裝置、驗證使用者，以及等待遠端伺服器的回呼。 除非發生錯誤，否則 RAS 用戶端不需要採取任何動作，就能將通知傳遞給使用者。

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>暫停狀態
</dt> <dd>

當遠端伺服器暫停連接作業來取得使用者的其他輸入時，就會發生 [暫停狀態](paused-states.md) 。 在暫停狀態期間，使用者可以輸入 [回呼](callback-connections.md) 號碼、在使用者驗證失敗時輸入不同的使用者名稱和密碼，或在舊密碼過期時輸入新的密碼。

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>終端州
</dt> <dd>

當成功建立連線、連接作業失敗，或 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 呼叫中斷連接時，就會發生終端機狀態。

</dd> </dl>

有幾個機制可供 RAS 用戶端用來判斷連接操作的目前狀態。 當 RAS 用戶端以非同步方式執行 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式時，遠端存取連線管理員會在連接狀態變更時，將進度通知傳送至用戶端的 [通知處理常式](notification-handlers.md) 。 此外，用戶端可以使用 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函式來取得任何 RAS 連接作業的目前狀態。

 

 