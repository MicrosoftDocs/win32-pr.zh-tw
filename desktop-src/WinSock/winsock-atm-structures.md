---
description: 下列清單提供每個 Winsock ATM 結構的精確描述。 如需任何結構的詳細資訊，請按一下結構名稱。
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Winsock ATM 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612798"
---
# <a name="winsock-atm-structures"></a>Winsock ATM 結構

下列清單提供每個 Winsock ATM 結構的精確描述。 如需任何結構的詳細資訊，請按一下結構名稱。



| ATM 結構                           | 描述                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**ATM \_ 位址**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | 將 ATM 位址資料儲存在 ATM 型通訊端中。             |
| [**ATM \_ BHLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | 識別相關聯的 ATM 通訊端的 B-HLI 資訊。 |
| [**ATM \_ BLLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | 識別相關聯之 ATM 通訊端的 B LLI 資訊。 |
| [**sockaddr \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | 儲存 ATM 通訊端的通訊端位址資訊。         |



 

若為原生 ATM 服務，請針對 \_ 位址家族使用 AF atm，並使用 [**sockaddr 的 \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) 通訊端位址結構。 若要開啟原生的 ATM 通訊端，請分別將 AF \_ 的 atm、SOCK \_ RAW 和 ATMPROTO \_ AAL5 或 ATMPROTO \_ AALUSER 傳遞至 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數。

 

 



