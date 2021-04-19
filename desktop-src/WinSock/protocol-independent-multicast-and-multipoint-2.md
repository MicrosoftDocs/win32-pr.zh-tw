---
description: Windows 通訊端2提供使用傳輸的 multipoint 和多播功能的一般方法。
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent 多播和 Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974601"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent 多播和 Multipoint

Windows 通訊端2提供使用傳輸的 multipoint 和多播功能的一般方法。 這個泛型方法會實作為這些功能，因為它可讓您存取多個傳輸通訊協定的基本資料傳輸功能。 Multipoint 的詞彙是用來參考多播和 multipoint 通訊。

目前的 multipoint 執行 (例如，IP 多播、聖 II、T. 120 和 ATM 單向) 差異很大。 節點如何聯結 multipoint 會話、特定節點是否指定為中央或根節點，以及是否要在所有節點之間交換資料，或只在根節點與不同分葉節點之間交換資料，兩者之間的不同。 Windows 通訊端2的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構是用來宣告通訊協定的各種 multipoint 屬性。 藉由檢查這些屬性，程式設計人員就知道要遵循適用的 Windows 通訊端2函式來設定、使用和卸載 multipoint 會話的慣例。

以下摘要說明支援 multipoint 的 Winsock 功能：

-   [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中的兩個屬性位。
-   針對 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函數的 *dwFlags* 參數定義的四個旗標。
-   一個函式（ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)），用於將分葉節點新增至 multipoint 會話
-   用於控制 multipoint 回送和建立多播傳輸範圍的兩個 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 命令代碼。  (後者對應至 IP 多播的存留時間或 TTL 參數。 ) 

> [!Note]  
> 在 Windows 通訊端2中包含這些 multipoint 功能，並不會妨礙應用程式使用現有的通訊協定相依介面，例如 IP 多播的 Deering 通訊端選項。

 

如需有關各種 Multipoint 配置的特性，以及如何運用 Windows 通訊端2適用功能的詳細資訊，請參閱 [Multipoint 和多播語義](multipoint-and-multicast-semantics-2.md) 。

 

 
