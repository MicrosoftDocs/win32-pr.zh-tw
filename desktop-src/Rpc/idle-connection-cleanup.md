---
title: 閒置連接清除
description: 依預設，在整個關聯關閉之前，不會關閉執行緒集區中的連接。
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839507"
---
# <a name="idle-connection-cleanup"></a>閒置連接清除

依預設，在整個關聯關閉之前，不會關閉執行緒集區中的連接。 此原則可讓具有大量執行緒或安全性識別的用戶端以有效率的方式對伺服器進行 RPC 呼叫。 缺點是可能會認可大量的資源，以維護這些連接。 為了管理進程，RPC 提供 [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) 函數。 此函式會啟用閒置連接清除;用戶端會定期掃描連接集區，並關閉最近未使用的連接。 如果關聯已維持內容控制碼，閒置連接清除會關閉所有閒置的連接，但即使連接閒置 (，還是會確定至少有一個連接保持開啟狀態，否則伺服器會取得內容控制碼執行下) 。 如果關聯未維持內容控制碼，閒置連接清除會關閉所有閒置的連接，即使這樣做不會在集區中保留任何連接。

在 Windows XP 上，RPC 執行時間會追蹤關聯中開啟的連接數目，如果任何關聯中的連接數目超過特定臨界值，就會自動開啟閒置的連線清除。

 

 




