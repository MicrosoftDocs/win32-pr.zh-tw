---
title: Teredo 位址
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 深入瞭解： Teredo 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354134"
---
# <a name="teredo-addresses"></a>Teredo 位址

Teredo 位址包含下列各項：

-   **Teredo 首碼**

    前32位是針對 Teredo 首碼，這對所有 Teredo 位址都相同。 WindowsXP 和 Windows Server 2003 一開始使用3FFE：831F：：/32 Teredo 前置詞。 在 RFC 4380 中為 teredo 定義的前置詞是2001::/32，而是 Windows Vista 和 Windows Server 2008 中的 teredo 所使用的前置詞。 以 Microsoft 資訊安全公告 MS06-064 更新時，執行 Windows XP 和 Windows Server 2003 的電腦將使用 2001::/32 Teredo 首碼。

-   **Teredo 伺服器 IPv4 位址**

    下一個32位包含協助設定此 Teredo 位址之 Teredo 伺服器的 IPv4 公用位址。 如需詳細資訊，請參閱本文中的「Teredo 用戶端的初始設定」。

-   **旗標**

    接下來的16個位是保留給 Teredo 旗標。 針對 Windows XP 型 Teredo 用戶端，唯一定義的旗標是高序位位，稱為錐形旗標。 當 Teredo 用戶端位於錐形 NAT 後方時，會設定錐形旗標。 在 Teredo 用戶端的初始設定期間，判斷連接到網際網路的 NAT 是否為錐形 NAT。 如需詳細資訊，請參閱本文中的「Teredo 用戶端的初始設定」。

    針對 Windows Vista 和 Windows Server 2008 型 Teredo 用戶端，[旗標] 欄位中未使用的位，可提供惡意使用者的位址掃描保護層級。 Windows Vista 和 Windows Server 2008 型 Teredo 用戶端的 [旗標] 欄位中的16個位包含下列各項： CRAAAAUG AAAAAAAA。 C 位適用于錐形旗標。 R 位是保留供日後使用。 U 位適用于通用/本機旗標 (設定為 0) 。 G 位是個別/群組旗標 (設定為 0) 。 A 位會設為12位隨機產生的數位。 藉由使用亂數字來表示在 Teredo 用戶端與 Teredo 伺服器之間，藉由捕捉封包的初始設定交換來判斷 Teredo 位址的其餘部分，將必須嘗試最多 4096 (212) 不同的位址，以在位址掃描期間判斷 Teredo 用戶端的位址。

-   **遮蔽外部埠**

    接下來的16個位會儲存與此 Teredo 用戶端之所有 Teredo 流量對應的外部 UDP 埠遮蔽版本。 當 Teredo 用戶端傳送其初始封包到 Teredo 伺服器時，封包的來源 UDP 埠會被 NAT 對應到不同的外部 UDP 埠。 Teredo 用戶端會維護此埠對應，使其保留在 NAT 的轉譯表中。 因此，主機的所有 Teredo 流量都使用相同的外部對應 UDP 埠。 外部 UDP 埠是由 teredo 伺服器從 Teredo 用戶端傳送之傳入初始封包的來源 UDP 埠所決定，並傳送回 Teredo 用戶端。

    外部埠會以0xFFFF 由外部埠來遮蔽。 例如，以十六進位格式表示的外部埠5000遮蔽版本是 EC77 (5000 = 0x1388，0x1388 XOR 0xFFFF = 0xEC77) 。 遮蔽外部埠可避免 Nat 在轉送的封包承載內轉譯外部埠。

-   **遮蔽外部地址**

    最後一個32位會儲存與此 Teredo 用戶端之所有 Teredo 流量對應之外部 IPv4 位址的遮蔽版本。 就像外部埠，當 Teredo 用戶端傳送其初始封包到 Teredo 伺服器時，封包的來源 IP 位址會被 NAT 對應到不同的外部 (公用) 位址。 Teredo 用戶端會維護此位址對應，使其保留在 NAT 的轉譯表中。 因此，主機的所有 Teredo 流量都使用相同的外部、對應的公用 IPv4 位址。 從 Teredo 用戶端傳送之傳入初始封包的來源 IPv4 位址，以及傳送回 Teredo 用戶端之傳入初始封包的來源 IPv4 位址，會決定外部 IPv4 位址。

    使用0xFFFFFFFF 由外部地址來遮蔽外部地址。 例如，以冒號十六進位格式131.107.0.1 的公用 IPv4 位址的遮蔽版本是7C94： FFFE (131.107.0.1 = 0x836B0001，0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE) 。 遮蔽外部地址可避免 Nat 在轉送的封包承載內轉譯外部地址。

 

 




