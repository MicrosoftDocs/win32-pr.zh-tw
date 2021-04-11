---
title: 取消重新傳輸
description: 如果對目的地實體指定的超時時間內沒有對通訊要求的回應，而且如果指定了對實體的重新傳輸，Microsoft 的 WinSNMP 執行會重新傳輸要求。
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021442"
---
# <a name="canceling-retransmission"></a>取消重新傳輸

如果對目的地實體指定的超時時間內沒有對通訊要求的回應，而且如果指定了對實體的重新傳輸，Microsoft 的 WinSNMP 執行會重新傳輸要求。 [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)函式的呼叫可以取消此重新傳輸週期，並釋放與訊息要求相關聯的內部資料結構。

請注意，目的地實體可能會接收 [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) 函式的呼叫已取消的 SNMP 訊息。 目的地實體也可能會回應已取消的 SNMP 訊息。 這是因為交易佇列發生在多個層級。 不過，一旦呼叫 [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)取消訊息，Microsoft 的 WinSNMP 執行就不會重新傳輸訊息、提交回應 PDU，或傳送超時通知給該訊息的應用程式。

 

 




