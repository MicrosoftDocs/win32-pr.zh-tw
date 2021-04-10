---
description: 以下是保護 Windows 通訊端程式設計的指南。
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: 安全 Winsock 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692215"
---
# <a name="secure-winsock-programming"></a>安全 Winsock 程式設計

以下是保護 Windows 通訊端程式設計的指南。 它的設計目的是要讓您瞭解 Winsock 安全性以及安全網路應用程式開發人員可用的選項。

-   [使用 \_ REUSEADDR 等 \_ EXCLUSIVEADDRUSE](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Winsock 安全通訊端擴充功能](winsock-secure-socket-extensions.md)

使用通訊端的通訊也可以使用安全通道的 SSL/TLS 標準（也稱為 Schannel 技術）進行加密。 Schannel 是安全性支援提供者 (SSP) ，其中包含一組安全性通訊協定，可透過加密提供身分識別驗證和安全的私人通訊。 Schannel 主要用於需要安全超文字傳輸通訊協定 (HTTP) 通訊的網際網路應用程式。 如需詳細資訊，請參閱 [安全通道](../secauthn/secure-channel.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安全通道](../secauthn/secure-channel.md) \(英文\)
</dt> </dl>

 

 
