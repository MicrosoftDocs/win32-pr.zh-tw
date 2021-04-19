---
description: 連接到特定的智慧卡並與其通訊。
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: 智慧卡與讀者存取功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980596"
---
# <a name="smart-card-and-reader-access-functions"></a>智慧卡與讀者存取功能

下列函式會連接到特定的 [*智慧卡*](../secgloss/s-gly.md)，並與之通訊。 卡片的 i/o 作業會使用緩衝區來傳送或接收資料，並使用包含通訊協定控制資訊的結構。 通訊協定控制資訊結構的開頭一律為 [**捨棄 \_ IO \_ 要求**](scard-io-request.md) 結構。



| 主題                                                  | 描述                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | 連接到卡片。                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | 重新建立連接。                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | 終止連接。                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | 啟動 [*交易*](../secgloss/t-gly.md)，封鎖其他應用程式存取卡片。                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | 結束交易，讓其他應用程式存取卡片。                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | 提供讀取器的目前狀態。                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | 使用 [*t = 0*](../secgloss/t-gly.md)、 [*T = 1*](../secgloss/t-gly.md)和未經處理的通訊協定，要求服務並從卡片收到資料。 |



 

 

 
