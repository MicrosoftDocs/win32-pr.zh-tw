---
description: 系統會提供具有某些預設設定的 PGM 傳送者，這些設定會影響資料傳輸的效能，以及資料緩衝處理的時間長度，以考慮封包遺失以及相關聯的 PGM 用戶端重新傳輸要求。
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: PGM 寄件者選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973266"
---
# <a name="pgm-sender-options"></a>PGM 寄件者選項

系統會提供具有某些預設設定的 PGM 傳送者，這些設定會影響資料傳輸的效能，以及資料緩衝處理的時間長度，以考慮封包遺失以及相關聯的 PGM 用戶端重新傳輸要求。 下列段落描述這些預設設定。

## <a name="window-size-and-transmission-rate"></a>視窗大小和傳輸速率

設定視窗大小和傳輸速率的功能，可讓應用程式控制傳輸緩衝區重新傳輸的資料量，以及傳輸位元組資料流程的速率。

重新傳輸資料會儲存在檔案中，因此最大視窗大小會受到傳輸可用磁碟空間的限制。 預設視窗大小為10MB。 雖然傳送或訊息大小可能會超過視窗或緩衝區大小，但資料串流仍不會中斷;傳送會暫止，直到所有資料都已送出為止。

> [!Note]  
> 緩衝區空間上限會受限於在任何指定時間（等於 2 ^ 31-1）可以保留在視窗中的封包數上限。

 

傳輸速率是原始資料封包的資料流程 (ODATA) 、重新傳輸的資料封包 (.RDATA) 和傳輸特定的簿記封包 (SPMs) （以碼錶示）。 如果速率限制預設為每秒 56 kb。 預設視窗大小為 10 mb，預設速率為每秒 56 kb。 由於 [**RM \_ 傳送 \_ 視窗**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) 結構的三個成員之間的關聯性，因此預設的視窗大小為1428秒。 如需詳細資訊，請參閱 **RM \_ 傳送 \_ 視窗** 。

## <a name="window-advance-rate"></a>視窗提前速率

視窗提前速率是由 RM 傳送者 [ \_ \_ 視窗 \_ 進階 \_ 率](socket-options.md) 通訊端選項設定。 此選項可讓應用程式指定 PGM 傳送者視窗的遞增量（以非零百分比值的視窗大小表示）。 預設值為15%，最大速率為50%。 如果 PGM 傳送者有擱置中的修復資料落在遞增視窗的空間中，則會在視窗中的每個修復封包送出時，將視窗部分設定為 advanced。

## <a name="forward-error-correction-fec"></a>轉寄錯誤更正 (FEC) 

轉寄錯誤更正是透過使用 RM \_ use \_ FEC socket 選項來設定。 此通訊端選項可讓 PGM 傳送者將修復封包當作同位封包傳送，而不是一般的資料封包。 這樣做可將傳送的修復封包數目降至最低，以修復由相同資料群組內的多個接收者所遺失的不同序列。 啟用 FEC 只會在 PGM 寄件者上設定。 PGM 接收器會自動遵循寄件者所設定的原則。 如需 FEC 的詳細討論，請參閱位於 [IETF](https://www.ietf.org/) 網站的 PGM RFC。

 

 



