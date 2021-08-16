---
description: 資料流程通訊端抽象包括頻外 (OOB) 資料的概念。
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent 頻外資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860828"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent 頻外資料

資料流程通訊端抽象包括頻外 (OOB) 資料的概念。 許多通訊協定允許某些內送資料的部分以某種方式標示為特殊，而這些特殊資料區塊可以傳遞給使用者，而不是正常的順序。 範例包括在 X. 25 和其他 OSI 通訊協定中的快速資料，以及 BSD 中的緊急資料 UNIX 使用 TCP。 下一節會以與通訊協定無關的方式來說明 OOB 資料處理。 使用 TCP 緊急資料實行的 OOB 資料討論，會遵循與通訊協定無關的說明。 在每個討論中，使用 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 也意指 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)和 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)，而 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 的參考也適用于 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)。

## <a name="protocol-independent-oob-data"></a>通訊協定獨立的 OOB 資料

OOB 資料是與每一對連接的串流通訊端相關聯的邏輯獨立傳輸通道。 OOB 資料可能會與一般資料分開傳遞給使用者。 此抽象概念會定義 OOB 資料設施一次至少必須支援至少一個 OOB 資料區塊的可靠傳遞。 此資料區塊可以包含至少一個位元組的資料，而且至少有一個 OOB 資料區塊可以在任何時間都擱置傳遞給使用者。 針對支援頻外信號的通訊協定 (例如 TCP，其中緊急資料是以一般資料) 順序傳遞，系統通常會從一般資料流程中取出 OOB 資料，並將其個別儲存 (在標準資料流程) 中留出間距。 這可讓使用者依序接收 OOB 資料並依序接收該資料，而不需要緩衝所有的中間資料。 您可以查看頻外 (OOB) 資料。

使用者可以使用 [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) 或 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函數搭配 **SIOCATMARK** IOCTL 來判斷是否有任何 OOB 資料正在等候讀取。 若為通訊協定，則一般資料流程內 OOB 資料區塊位置的概念有意義，例如 TCP，Windows 通訊端服務提供者會維護概念性標記，指出一般資料流程內 oob 資料最後一個位元組的位置。 這不是執行支援 **SIOCATMARK** 之 **ioctlsocket** 或 **WSAIoctl** 函數的必要項。 需要的是 OOB 資料的存在或不存在。

針對一般資料流程中 OOB 資料區塊位置的概念有意義的通訊協定，應用程式可能會以內嵌方式處理頻外資料，作為一般資料流程的一部分。 這是藉由設定 socket 選項讓 \_ OOBINLINE 與 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來達成。 對於 OOB 資料區塊真正獨立于一般資料流程的其他通訊協定，嘗試設定 \_ OOBINLINE 會導致錯誤。 應用程式可以使用 [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) 或 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式搭配 **SIOCATMARK** IOCTL，判斷是否有任何未讀取的 OOB 資料在標記前面。 例如，它可以使用這項資訊，藉由確保在適當的情況下捨棄資料流程中標示的所有資料，來重新同步處理其對等。

停用 \_ OOBINLINE 之後 (預設設定) ：

-   Windows\_如果應用程式已向 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)註冊通知，則通訊端會通知應用程式 fd OOB 事件， \_ 就像使用 FD 讀取來通知一般資料存在一樣。 亦即， \_ 當 oob 資料到達時，會在沒有先前排入佇列的 oob 資料的情況下公佈 FD oob。 \_當使用 MSG oob 旗標讀取資料時，也會公佈 FD oob， \_ 而某些 OOB 資料在讀取作業傳回之後仍會排入佇列。 FD \_ 讀取訊息不會針對 OOB 資料張貼。
-   Windows如果 OOB 資料在通訊端上排入佇列，則通訊端會從 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select)傳回，並設定適當的 *exceptfds* 通訊端。
-   應用程式可以在任何時間使用訊息 OOB 呼叫 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) ， \_ 以讀取緊急資料區塊。 OOB 資料的區塊會跳至佇列。
-   應用程式可以在沒有訊息 OOB 的情況下呼叫 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) ， \_ 以讀取正常資料流程。 OOB 資料區塊不會出現在具有一般資料的資料流程中。 如果在任何 **接收** 呼叫之後仍保留 OOB 資料，Windows 通訊端會在 \_ 使用 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select)時，使用 FD OOB 或 with *exceptfds* 來通知應用程式。
-   針對 OOB 資料在標準資料流程中具有位置的通訊協定，單一 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 作業不會跨越該位置。 其中一個 **接收** 會傳回標記之前的一般資料，而第二次 **接收** 則需要在標記之後開始讀取資料。

\_啟用 OOBINLINE 之後：

-   \_未針對 oob 資料張貼 FD oob 訊息。 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select)和 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)函式的用途會將 OOB 資料視為正常，並藉由在 *readfds* 中設定通訊端，或分別傳送 FD \_ 讀取訊息來表示。
-   應用程式無法呼叫[](/windows/desktop/api/winsock/nf-winsock-recv)具有 \_ 設定為讀取 oob 資料區塊之 MSG oob 旗標的接收。 傳回錯誤碼 WSAEINVAL。
-   應用程式可以呼叫未設定 MSG OOB 旗標的 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) \_ 。 任何 OOB 資料在一般資料流程內都會以正確的順序傳遞。 OOB 資料永遠不會與一般資料混合。 必須有三個讀取要求，才能取得過去的 OOB 資料。 第一個會傳回 OOB 資料區塊之前的一般資料，第二個會傳回 OOB 資料，而第三個會傳回 oob 資料之後的一般資料。 換句話說，會保留 OOB 資料區塊界限。

當 OOBINLINE 為 off 時， [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 常式特別適合用來處理頻外資料存在的通知 \_ 。

## <a name="oob-data-in-tcp"></a>TCP 中的 OOB 資料

> [!IMPORTANT]
> 以下討論使用 TCP 緊急資料執行的頻外資料 (OOB) ，會遵循 Berkeley software 散發套件中所使用的模型。 使用者和實施者應該注意：

 

-   [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (有兩個衝突的解釋，) 引進了概念。
-   Berkeley Software 散發 (BSD) 中的 OOB 資料執行不符合 [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt)中指定的主機需求。

    具體而言，BSD 中的 TCP 緊急指標會指向緊急資料位元組之後的位元組，而 RFC 相容的 TCP 緊急指標則會指向緊急資料位元組。 因此，如果應用程式將來自 BSD 相容的執行的緊急資料傳送至與 RFC 1122 相容的執行，則接收者會讀取錯誤的緊急資料位元組 (它會讀取位於資料流程中正確位元組後面的位元組，以作為緊急資料位元組) 。

    為了將互通性問題降到最低，建議應用程式寫入器不要使用 OOB 資料，除非這是與現有服務互通的必要項。 Windows通訊端供應商會呼籲，以記載其產品所實行的 OOB 語義 (BSD 或 RFC 1122) 。

具有 URG (for 緊急) 旗標集合的 TCP 區段抵達，表示 TCP 資料流程內有單一位元組的 OOB 資料存在。 OOB 資料區塊的大小為一個位元組。 緊急指標是 TCP 標頭中目前序號的正數位移，表示 OOB 資料區塊 (不明確的位置，如先前) 所述。 因此，它可能會指向尚未收到的資料。

如果已 \_ 停用 OOBINLINE， (預設) 當 TCP 區段包含緊急指標所指向的位元組時，就會從資料流程中移除 OOB 資料區塊 (一個位元組) ，然後緩衝處理。 如果後續的 TCP 區段以緊急旗標設定 (，並) 新的緊急指標，則目前排入佇列的 OOB 位元組可能會遺失，因為新的 OOB 資料 (區塊會將它取代為 Berkeley 軟體散發) 中發生的情況。 但是，它永遠不會在資料流程中取代。

在 \_ 啟用 OOBINLINE 的情況下，緊急資料仍會保留在資料流程中。 因此，當新的 TCP 區段抵達包含緊急資料時，不會遺失 OOB 資料區塊。 現有的 OOB 資料標記會更新為新的位置。

> [!Note]  
> \_設定好 OOBINLINE 通訊端選項時，SIOCATMARK 的 IOCTL 一律會傳回 **TRUE**，而且 OOB 資料會以一般資料的形式傳回給使用者。

 

 

 



