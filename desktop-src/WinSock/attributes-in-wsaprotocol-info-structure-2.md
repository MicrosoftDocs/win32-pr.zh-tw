---
description: XP1 \_ 支援 \_ \_ \_ \_ Winsock WSAPROTOCOL 資訊結構中的 multipoint、XP1 multipoint 控制項平面和 XP1 \_ multipoint \_ 資料 \_ 平面屬性參數 \_ 。
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: WSAPROTOCOL_INFO 結構中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb502c0f29f09604f80e5437774f2b481cef238aaf34f566e78886127dae1027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898548"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>WSAPROTOCOL 資訊結構中的屬性 \_

為了支援上述分類法， [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中的三個屬性參數可分別用來區分控制項和資料平面中使用的配置：

-   XP1 \_ 支援 \_ multipoint 值為1的 multipoint 表示此通訊協定專案支援 multipoint 通訊，且下列兩個參數有意義。
-   XP1 \_ MULTIPOINT \_ 控制 \_ 平面會指出控制平面的根目錄 (值 = 1) 或 nonrooted (值 = 0) 。
-   XP1 \_ MULTIPOINT \_ 資料 \_ 平面會指出資料平面是否為 root (value = 1) 或 nonrooted (value = 0) 。

請注意，如果 multipoint 通訊協定支援 root 和 nonrooted 資料平面（每個都有一個專案），就會出現兩個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案。

應用程式可以使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 來探索指定的通訊協定是否支援 multipoint 通訊，如果是，則分別支援控制和資料平面的方式。

 

 
