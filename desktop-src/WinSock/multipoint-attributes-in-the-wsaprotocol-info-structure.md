---
title: WSAPROTOCOL_INFO 中的 Multipoint 屬性
description: WSAPROTOCOL 資訊結構中的 Multipoint 屬性 \_ 包括 XP1 \_ 支援 \_ multipoint、XP1 \_ MULTIPOINT \_ 控制 \_ 平面和 XP1 \_ MULTIPOINT \_ 資料 \_ 平面。
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1275b6da00258be10b071bc9b2399abaf5dd608583f3d81a0fdb16af493824ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741102"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>WSAPROTOCOL_INFO 中的 Multipoint 屬性

[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中定義了三個屬性參數，以區分用於控制項和資料平面的不同配置：

-   XP1 \_ 支援 \_ multipoint 值為1的 multipoint 表示此通訊協定專案支援 multipoint 通訊，且下列兩個參數有意義。
-   XP1 \_ MULTIPOINT \_ 控制 \_ 平面會指出控制平面的根目錄 (值 = 1) 或 nonrooted (值 = 0) 。
-   XP1 \_ MULTIPOINT \_ 資料 \_ 平面會指出資料平面是否為 root (value = 1) 或 nonrooted (value = 0) 。

如果 multipoint 通訊協定支援 root 和 nonrooted 資料平面（每個都有一個專案），則會出現兩個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案。

 

 
