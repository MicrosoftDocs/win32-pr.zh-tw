---
description: 本主題中的資訊適用于 Windows Server 2003 和 Windows XP。
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: 安全通訊端層通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944130"
---
# <a name="secure-sockets-layer-protocol"></a>安全通訊端層通訊協定

本主題中的資訊適用于 Windows Server 2003 和 Windows XP。 如需 Windows Server 2008 和 Windows Vista 的加密套件，請參閱 [Schannel 中的加密套件](cipher-suites-in-schannel.md)。

Schannel 支援 [*安全通訊端層 (SSL) 通訊協定*](../secgloss/s-gly.md)的版本2.0 和3.0。

> [!Note]  
> 從 Windows 10 開始，1607和 Windows Server 2016 版，SSL 2.0 已經移除，不再受到支援。

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3.0 是 [傳輸層安全性通訊協定](transport-layer-security-protocol.md)的前身。

Schannel 支援 SSL 3.0 的 [TLS 加密套件](tls-cipher-suites.md) 底下所列的加密套件。 SSL 3.0 支援 TLS 加密套件下所列的所有加密套件，以及 \_ \_ \_ 具有 \_ FORTEZZA \_ CBC \_ SHA 的 ssl FORTEZZA KEA。

## <a name="ssl-20"></a>SSL 2.0

SSL 2.0 已被 TLS 取代，不應該用於新的開發。

Schannel 支援 SSL 2.0 的下列加密套件。 套件會依最安全到最不安全的順序列出。

-   \_ \_ \_ 使用 MD5 的 SSL RC4 128 \_
-   \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL DES 192 EDE3 CBC
-   \_ \_ \_ \_ \_ 使用 \_ MD5 的 SSL RC2 cbc 128 CBC
-   \_ \_ \_ \_ 使用 MD5 的 SSL DES 64 CBC \_
-   \_ \_ \_ \_ 使用 MD5 的 SSL RC4 128 EXPORT40 \_

 

 
