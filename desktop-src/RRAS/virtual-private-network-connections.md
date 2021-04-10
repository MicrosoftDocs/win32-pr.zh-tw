---
title: 虛擬私人網路連接
description: 遠端存取服務 (RAS) 除了使用點對點通訊協定 (PPP)  (PPP) 的傳統遠端存取連接之外，還支援虛擬私人網路 (VPN) 連接。
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f5fc0b80a6eb00e7587e941eea39c056a11d14
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023590"
---
# <a name="virtual-private-network-connections"></a>虛擬私人網路連接

遠端存取服務 (RAS) 除了使用點對點通訊協定 (PPP)  (PPP) 的傳統遠端存取連接之外，還支援虛擬私人網路 (VPN) 連接。 在 VPN 連線中，VPN 封包會封裝在 IP 封包中，並在 IP 網路（例如網際網路）上傳送。 因此，需要存取 IP 網路才能建立 VPN 連線。 如果用戶端電腦有連至 IP 網路的連線（例如連至 IP 區域網路的連線），則用戶端可以使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式的單一呼叫來建立 VPN 連接。

如果用戶端電腦沒有連至 IP 網路的 always on 連線，則需要兩個 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫才能建立 VPN 連接。 第一個呼叫會建立連至 IP 網路的撥號連線;第二個呼叫會建立 VPN 連接。

VPN 連線之 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))結構的 **szLocalPhoneNumber** 成員應該包含目的地 VPN 伺服器的 DNS 名稱或 IP 位址。

每個連接都需要個別的 [電話簿](ras-phone-books.md) 專案。 第一次呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 時，會指定 IP 網路的電話簿專案。 第二個呼叫會指定 VPN 的電話通訊錄專案。

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函式會採用 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的指標做為參數。 此結構指定用於電話簿專案所指定之網路的驗證認證。 存取 IP 網路所需的認證通常與 VPN 的認證不同。 第一次呼叫 **RasDial** 時，應該指定 IP 網路的認證。 第二個呼叫應指定 VPN 的認證。

如果 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式成功，它會傳回連接的控制碼。 在 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 的呼叫中使用此控制碼來終止連接。

在上述案例中，兩個對 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 的呼叫會針對 IP 網路和 VPN 傳回不同的連接控制碼。 使用 VPN 連線的控制碼來呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 會終止 vpn 連線，但不會讓 IP 網路的連線保持不變。

 

 