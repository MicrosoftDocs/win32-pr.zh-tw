---
title: Teredo 元件
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 深入瞭解： Teredo 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997076"
---
# <a name="teredo-components"></a>Teredo 元件

[Teredo](about-teredo.md)基礎結構包含下列元件：

## <a name="teredo-clients"></a>Teredo 用戶端

Teredo 用戶端是一個支援 Teredo 通道介面的 IPv6/IPv4 節點，透過 Teredo 通道介面，封包會透過 Teredo 轉送) 傳送至 IPv6 網際網路上的其他 Teredo 用戶端或節點 (。 Teredo 用戶端會與 Teredo 伺服器通訊，以取得設定或使用以 Teredo 為基礎的 IPv6 位址所使用的位址首碼，以促進 IPv6 網際網路上其他 Teredo 用戶端或主機的通訊。

Windows XP Service Pack 1 (SP1) 搭配 Advanced 網路套件、Windows XP Service Pack 2 (SP2) 、Windows Server 2003 （含 Service pack 1） (SP1) 、Windows Server 2003 Service pack 2 (SP2) 、Windows Vista 和 Windows Server 2008 全都包含 Teredo 用戶端。

## <a name="teredo-servers"></a>Teredo 伺服器

Teredo 伺服器是一個同時連線至 IPv4 網際網路和 IPv6 網際網路的 IPv6/IPv4 節點，可支援接收封包的 Teredo 通道介面。 Teredo 伺服器的一般角色是協助 Teredo 用戶端的位址設定，並協助 Teredo 用戶端與其他 Teredo 用戶端之間的初始通訊，或 Teredo 用戶端與 IPv6 專用主機之間的初始通訊。 Teredo 伺服器會接聽 UDP 埠3544的 Teredo 流量。

與用戶端不同的是，Teredo 伺服器不包含在 Microsoft 作業系統中。 為了方便 Windows 型 Teredo 用戶端電腦之間的通訊，Microsoft 已將 Teredo 伺服器部署在 IPv4 網際網路上。

## <a name="teredo-relays"></a>Teredo 轉送

Teredo 轉送是一種 IPv6/IPv4 路由器，可以在 IPv4 網際網路上的 Teredo 用戶端之間轉送封包 (使用 Teredo 通道介面) 和 IPv6 專用主機。 在某些情況下，Teredo 轉送會與 Teredo 伺服器互動，以促進 Teredo 用戶端與 IPv6 專用主機之間的初始通訊。 Teredo 轉送會接聽 UDP 埠3544的 Teredo 流量。

如同 Teredo 伺服器，Microsoft 作業系統不包含 Teredo 轉送功能。 Microsoft 目前不打算在 IPv4 網際網路上部署 Teredo 轉送。 Teredo 轉送不需要與 Teredo 主機特定轉送通訊。

## <a name="teredo-host-specific-relays"></a>Teredo Host-Specific 轉送

Teredo 用戶端與使用全域位址設定的 IPv6 主機之間的通訊必須經過 Teredo 轉送。 連線到 IPv6 網際網路的 IPv6 專用主機需要這項功能。 但是，當 IPv6 主機具備 IPv6 和 IPv4 功能，並同時連線到 IPv4 網際網路和 IPv6 網際網路時，就應該透過 IPv4 網際網路在 Teredo 用戶端與 IPv6 主機之間進行通訊，而不需要跨越 IPv6 網際網路並經過 Teredo 轉送。

Teredo 主機特定轉送是一種 IPv6/IPv4 節點，其具有 IPv4 網際網路和 IPv6 網際網路的介面和連線能力，且可以透過 IPv4 網際網路直接與 Teredo 用戶端通訊，而不需要中繼 Teredo 轉送。 IPv4 網際網路的連線可以透過公用 IPv4 位址，或透過私人 IPv4 位址和連續的 NAT 來進行。 IPv6 網際網路的連線能力可透過直接連線到 IPv6 網際網路，或透過 IPv6 轉換技術（例如6to4）進行，其中 IPv6 封包會在 IPv4 網際網路上進行通道處理。 Teredo 主機特定轉送會接聽 UDP 埠3544的 Teredo 流量。

具有 Advanced 網路功能套件的 windows XP （含 SP1）、Windows XP 加裝 SP2、Windows Server 2003 （含 SP1）、Windows Server 2003 SP2、Windows Vista 及 Windows Server 2008 包含 Teredo 主機特定轉送功能，如果電腦有指派的全域位址，則會自動啟用此功能。 系統會從原生 IPv6 路由器、ISATAP 路由器或6to4 路由器，在接收的路由器通告訊息中指派全域位址。 如果電腦沒有全域位址，便會啟用 Teredo 用戶端功能。

Teredo 主機特定轉送可讓 Teredo 用戶端有效率地與6to4 主機、使用非6to4 全域首碼的 IPv6 主機，或在其位址使用全域首碼的組織內的 ISATAP 或6over4 主機進行通訊，前提是這兩個主機都使用支援 Teredo 的 Windows 版本。

 

 




