---
description: 應用程式會使用 WSAEnumProtocols 函數來判斷存在哪些傳輸通訊協定和通訊協定鏈，以及取得相關聯 WSAPROTOCOL 資訊結構中所包含之每個的相關資訊 \_ 。
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: 使用多個通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112996"
---
# <a name="using-multiple-protocols"></a>使用多個通訊協定

應用程式會使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 函數來判斷存在哪些傳輸通訊協定和通訊協定鏈，以及取得相關聯 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中所包含之每個的相關資訊。

在大部分的情況下，每個通訊協定或通訊協定鏈都有一個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。 不過，某些通訊協定會展示多個行為。 例如，SPX 通訊協定是訊息導向的 (也就是說，傳送者的訊息界限會由網路) 保留，但是接收的通訊端可以忽略這些訊息界限，並將其視為位元組串流。 因此，每個行為都有兩個不同的 **WSAPROTOCOL \_ 資訊** 結構專案。

在 Windows 通訊端2中，會出現數個新的位址系列、通訊端類型和通訊協定值。 Windows 通訊端1.1 支援單一位址系列 (AF \_ INET) 適用于 IPv4，其中由少數知名的通訊端類型和通訊協定識別碼組成。 由於相容性的緣故，Windows 通訊端2會保留現有的位址系列、通訊端類型和通訊協定識別碼，但它也支援新的傳輸通訊協定新的位址系列值給新的媒體類型。

新的唯一識別碼不一定是知名的，但這應該不會造成問題。 建議需要與通訊協定無關的應用程式，根據其適用性（而不是指派給其 *通訊端 \_ 類型* 或 *通訊協定* 參數的值）選取通訊協定。 通訊協定適用性是由通訊屬性工作表示，例如訊息與位元組資料流程，以及包含在通訊協定 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中可靠且不可靠的通訊屬性。 以適用性為基礎選取通訊協定，而不是已知的通訊協定名稱和通訊端類型，可讓與通訊協定無關的應用程式利用新的傳輸通訊協定與其相關聯的媒體類型（因為它們變成可用）。

伺服器一半的用戶端/伺服器應用程式會藉由在所有適合的傳輸通訊協定上建立接聽通訊端來獲益。 然後，用戶端可以使用任何適當的通訊協定來建立其連接。 例如，這會讓用戶端應用程式不受修改，不論它是在透過區域網路連線的桌面系統上執行，還是在使用無線網路的膝上型電腦上執行。

 

 
