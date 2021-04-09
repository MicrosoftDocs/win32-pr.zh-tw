---
description: 原始通訊端是允許存取基礎傳輸提供者的通訊端類型。 不建議將應用程式移植到 Winsock 時使用原始通訊端的原因有好幾種。
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: 原始通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114908"
---
# <a name="raw-sockets"></a>原始通訊端

原始通訊端是允許存取基礎傳輸提供者的通訊端類型。 不建議將應用程式移植到 Winsock 時使用原始通訊端的原因有好幾種。

Windows 通訊端規格不會要求 Winsock 服務提供者支援原始通訊端，也就是 **SOCK \_ 原始** 類型的通訊端。 不過，建議服務提供者提供原始通訊端支援。 想要使用原始通訊端的 Windows 通訊端相容應用程式應該嘗試使用 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 呼叫來開啟通訊端，如果它失敗，請嘗試使用另一個通訊端類型或指出使用者失敗。

在 Windows 7、Windows Server 2008 R2、Windows Vista 和 Windows XP （含 Service Pack 2）上 (SP2) ，透過原始通訊端傳送流量的能力已受到數種限制。 如需詳細資訊，請參閱 [Tcp/ip 原始通訊端](tcp-ip-raw-sockets-2.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**插座**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[TCP/IP 原始通訊端](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 



