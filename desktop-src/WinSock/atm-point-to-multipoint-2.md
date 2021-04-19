---
description: ATM 落在根資料和根控制項平面的類別中。
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM 指向 Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973064"
---
# <a name="atm-point-to-multipoint"></a>ATM 指向 Multipoint

ATM 落在根資料和根控制項平面的類別中。 作為根的應用程式會建立 c \_ 根通訊端，而分葉節點上執行的對應項會使用 c 分 \_ 葉通訊端。 根應用程式會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來加入新的分葉節點。 分葉節點上的對應應用程式，會將它們的 c \_ 分葉通訊端設定為接聽模式。 具有指定之 c \_ 根通訊端的 WSAJoinLeaf 會對應至 2931 ADDPARTY 訊息。 在 ATM 的3.1 中不支援分葉起始的聯結，但在 ATM 單向4.0 中支援。 因此 ，使用指定的 c 分 \_ 葉通訊端 WSAJoinLeaf 會對應到適當的 ATM 單向4.0 訊息。

針對 ATM 點對 multipoint，還有其他考慮要謹記：

-   將新的點新增至 ATM 點對 multipoint 會話只會以邀請為基礎。 根邀請會藉由呼叫 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)函式來離開（已有 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept)函式呼叫）。
-   在 ATM 點對 multipoint 會話中的資料流程程，只是從根目錄到離開;「離開」無法使用相同的會話將資訊傳送至根目錄。
-   每個 ATM 介面卡只允許一個分葉。

 

 



