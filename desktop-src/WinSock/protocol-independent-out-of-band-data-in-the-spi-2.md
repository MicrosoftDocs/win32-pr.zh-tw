---
description: 頻外 (OOB) 資料是與一組連接的串流通訊端相關聯的邏輯獨立傳輸通道。
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: SPI 中的通訊協定 IndependentOut 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e5c7c5c8c8ad7a5985ec101dd157370c5f32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511404"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>SPI 中的通訊協定 IndependentOut 資料

頻外 (OOB) 資料是與一組連接的串流通訊端相關聯的邏輯獨立傳輸通道。 OOB 資料可能會與一般資料分開傳遞給使用者。 此抽象概念會定義 OOB 資料設施一次至少必須支援至少一個 OOB 資料區塊的可靠傳遞。 此資料區塊可能包含至少一個位元組的資料，而且至少有一個 OOB 資料區塊可能會在任何一次都有擱置的傳遞給使用者。 針對支援頻外信號的通訊協定 (也就是 TCP，也就是以一般資料) 順序傳遞緊急資料的情況下，系統通常會從一般資料流程中將 OOB 資料解壓縮，並將其分開儲存 (在一般資料流程) 中留出間距。 這可讓使用者依序接收 OOB 資料並依序接收該資料，而不需要緩衝所有的中間資料。 您可以查看 OOB 資料。

使用者可以使用 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK) 函數，判斷是否有任何的 OOB 資料正在等候讀取。 若為通訊協定，則一般資料流程內 OOB 資料區塊位置的概念會有意義 (也就是 TCP) ，Windows 通訊端服務提供者將會維護概念性標記，指出一般資料流程內 OOB 資料最後一個位元組的位置。 **WSPIoctl** (SIOCATMARK) 功能的執行不需要這項功能，因為 OOB 資料的存在與否都是必要的。

若為通訊協定，則一般資料流程內 OOB 資料區塊位置的概念會有意義，因為這是一般資料流程的一部分，所以應用程式可能偏好以內嵌方式處理頻外資料。 這是藉由設定通訊端選項來達成，因此 \_ OOBINLINE (請參閱 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))) 一節。 對於 OOB 資料區塊真正獨立于一般資料流程的其他通訊協定，嘗試設定 \_ OOBINLINE 會導致錯誤。 應用程式可以使用 SIOCATMARK WSPIoctl 命令，判斷標記前面是否有任何未讀取的 OOB 資料。 例如，它可能會使用這項功能，藉由確保在適當的情況下捨棄資料流程中標示的所有資料，來重新同步處理其對等。

使用 \_ OOBINLINE 停用 (預設為) ：

-   \_如果用戶端已使用 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))註冊通知，Winsock 服務提供者就會通知該用戶端的 fd OOB 事件， \_ 就像是使用 FD READ 來通知存在正常資料的方式一樣。 也就是說， \_ 當 oob 資料到達，而且沒有先前已排入佇列的 oob 資料，而且在使用 MSG OOB 旗標讀取資料時，以及在 \_ 讀取作業傳回之後仍會讀取一些 oob 資料時，就會公佈 FD oob。 FD \_ 讀取訊息不會針對 OOB 資料張貼。
-   如果 OOB 資料在通訊端上排入佇列，Winsock 服務提供者會從 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) 傳回適當的 *exceptfds* 通訊端集。
-   用戶端可以使用訊息 OOB 來呼叫 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ， \_ 以在任何時間讀取緊急資料區塊。 OOB 資料的區塊會跳至佇列。
-   用戶端可以呼叫 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ，而不需要訊息 \_ OOB 來讀取一般資料串流。 OOB 資料區塊將不會出現在具有一般資料的資料流程中。 如果在任何呼叫 **WSPRecv** 之後仍保留 OOB 資料，服務提供者會在 \_ 使用 [**WSPSELECT**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))時，透過 FD OOB 或 *exceptfds* 通知用戶端。
-   針對 OOB 資料在標準資料流程中具有位置的通訊協定，單一 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 作業不會跨越該位置。 其中一個 **WSPRecv** 會傳回標記之前的一般資料，而第二個 **WSPRecv** 則需要在標記之後開始讀取資料。

\_啟用 OOBINLINE 之後：

-   FD 的 oob \_ 訊息不會針對 OOB 資料張貼，因為 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) 和 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 函式的目的是將 oob 資料視為一般資料，並藉由在 *readfds* 中設定通訊端，或分別傳送 FD \_ 讀取訊息來表示。
-   用戶端可能不會呼叫 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ，並將 MSG \_ oob 旗標設為讀取 OOB 資料區塊，而錯誤碼 WSAEINVAL 將會傳回。
-   用戶端可以呼叫未設定 MSG OOB 旗標的 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) \_ 。 任何 OOB 資料都會以正確的順序在正常資料流程中傳遞。 OOB 資料永遠不會與一般資料混合使用，因此必須有三個讀取要求才能取得過去的 OOB 資料。 第一個會傳回 OOB 資料區塊之前的一般資料，第二個會傳回 OOB 資料，而第三個會傳回 oob 資料之後的一般資料。 換句話說，會保留 OOB 資料區塊界限。

[**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))常式特別適合用來處理當 OOBINLINE 為 off 時，有 OOB 資料存在的通知 \_ 。

 

 
