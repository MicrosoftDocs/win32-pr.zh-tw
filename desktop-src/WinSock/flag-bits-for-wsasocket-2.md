---
description: 在聯結至 multipoint 會話的某些實例中，從點對點通訊端的行為可能有所差異。
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: WSASocket 的旗標位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971398"
---
# <a name="flag-bits-for-wsasocket"></a>WSASocket 的旗標位

在聯結至 multipoint 會話的某些實例中，從點對點通訊端的行為可能有所差異。 例如， \_ 根資料平面配置中的 d 分葉通訊端只能將資訊傳送給 d \_ 根參與者。 這會讓應用程式必須能夠指出通訊端的預期使用方式與其建立方式一致。 這是透過可在 *dwFlags* 參數中設定為 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的四個旗標位來完成：

-   WSA \_ 旗標 \_ MULTIPOINT \_ C \_ root，用於建立作為 C 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根控制項平面時才允許。
-   WSA \_ 旗 \_ \_ 標 MULTIPOINT C 分 \_ 葉，用於建立作為 C 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。
-   WSA \_ 旗標 \_ MULTIPOINT \_ D \_ root，用於建立做為 D 根的通訊端 \_ ，而且只有在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出根資料平面時才允許。
-   WSA \_ 旗標 \_ MULTIPOINT \_ D 分 \_ 葉，用於建立做為 D 分葉的通訊端 \_ ，而且只有 \_ \_ 在對應的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案中指出 XP1 支援 MULTIPOINT 時才允許。

請注意，建立 multipoint 通訊端時，正好是兩個控制平面旗標的其中一個，而且必須在 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的 *dwFlags* 參數中設定兩個數據平面旗標的其中一個。 因此，建立 multipoint 通訊端的四種可能性如下：

-   "c \_ root/d \_ root"
-   "c \_ 根/d 分 \_ 葉"
-   "c 分 \_ 葉/d \_ 根"
-   "c 分 \_ 葉/d 分 \_ 葉"

 

 
