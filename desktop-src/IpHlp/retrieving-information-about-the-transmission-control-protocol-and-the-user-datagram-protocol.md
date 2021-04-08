---
description: IP 協助程式可讓您存取在本機電腦上使用之網路通訊協定的相關資訊。
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: 正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695871"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊

IP 協助程式可讓您存取在本機電腦上使用之網路通訊協定的相關資訊。 使用下列段落中所述的函式，在本機電腦上取得傳輸控制通訊協定 (TCP) 和使用者資料包協定 (UDP) 的相關資訊。

[**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函數會抓取 TCP 目前的統計資料。 如需涉及 **GetTcpStatistics** 的程式碼範例，請參閱 [使用 GetTcpStatistics 抓取資訊](retrieving-information-using-gettcpstatistics.md)。

[**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics)函式會捕獲 UDP 目前的統計資料。

[**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable)函數會抓取 TCP 連接資料表。 [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable)會捕獲 UDP 接聽程式資料表。

[**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry)函式可讓開發人員將指定 TCP 連接的狀態設定為 MIB \_ tcp \_ 狀態 \_ 刪除 \_ TCB。

 

 



