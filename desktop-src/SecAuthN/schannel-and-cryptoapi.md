---
description: Schannel 針對密碼編譯作業（例如儲存公開/私密金鑰）使用 CryptoAPI。
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel 和 CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386073"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="8dde6-103">Schannel 和 CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="8dde6-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="8dde6-104">Schannel 針對密碼編譯作業（例如儲存 [*公開/私密金鑰*](../secgloss/p-gly.md)）使用 [CryptoAPI](../seccrypto/cryptography-essentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="8dde6-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="8dde6-105">下列主題提供有關 Schannel 如何利用 CryptoAPI 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8dde6-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="8dde6-106">主題</span><span class="sxs-lookup"><span data-stu-id="8dde6-106">Topic</span></span>                                                                   | <span data-ttu-id="8dde6-107">描述</span><span class="sxs-lookup"><span data-stu-id="8dde6-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dde6-108">憑證存放區</span><span class="sxs-lookup"><span data-stu-id="8dde6-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="8dde6-109">用戶端和伺服器憑證都必須儲存在憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="8dde6-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="8dde6-110">CryptoAPI 2.0 私密金鑰</span><span class="sxs-lookup"><span data-stu-id="8dde6-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="8dde6-111">Schannel 認證會在內部表示為憑證 [**\_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) 結構。</span><span class="sxs-lookup"><span data-stu-id="8dde6-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 
