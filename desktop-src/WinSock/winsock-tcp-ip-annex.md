---
description: 本節說明傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 函數、資料結構和控制項。
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191729"
---
# <a name="winsock-tcpip-annex"></a>Winsock TCP/IP 附錄

本節說明傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 函數、資料結構和控制項。



| 元素          | 描述                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 通訊協定名稱 (s)  | TCP、UDP                                                                                                                                    |
| Description      | 透過 IP 網路層提供傳輸服務： UDP 適用于不可靠的資料包、TCP （適用于可靠的連接導向位元組串流）。 |
| 位址系列   | **AF \_INET**， **AF \_ INET6**                                                                                                                 |
| 標頭檔      | *Ws2tcpip。h*                                                                                                                                |



 

提供兩種基本類型的傳輸服務：不可靠的資料包 (UDP) ，以及可靠的連接導向-位元組串流 (的 TCP) 。 此外，也可以選擇性地支援原始通訊端。 原始通訊端可讓應用程式透過 TCP 和 UDP （例如 ICMP）以外的通訊協定進行通訊。 **Af \_ INET** 和 **af \_ INET6** 位址系列支援原始通訊端，但有一些限制。

本節涵蓋 TCP/IP 通訊協定專用的 Winsock 延伸模組。 它也會描述需要特殊考慮的基底 Winsock 函式，或使用 TCP/IP 時可能出現的獨特行為的層面。

 

 



