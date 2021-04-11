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
# <a name="secure-winsock-programming"></a><span data-ttu-id="2b79b-103">安全 Winsock 程式設計</span><span class="sxs-lookup"><span data-stu-id="2b79b-103">Secure Winsock Programming</span></span>

<span data-ttu-id="2b79b-104">以下是保護 Windows 通訊端程式設計的指南。</span><span class="sxs-lookup"><span data-stu-id="2b79b-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="2b79b-105">它的設計目的是要讓您瞭解 Winsock 安全性以及安全網路應用程式開發人員可用的選項。</span><span class="sxs-lookup"><span data-stu-id="2b79b-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="2b79b-106">使用 \_ REUSEADDR 等 \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="2b79b-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="2b79b-107">Winsock 安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="2b79b-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="2b79b-108">使用通訊端的通訊也可以使用安全通道的 SSL/TLS 標準（也稱為 Schannel 技術）進行加密。</span><span class="sxs-lookup"><span data-stu-id="2b79b-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="2b79b-109">Schannel 是安全性支援提供者 (SSP) ，其中包含一組安全性通訊協定，可透過加密提供身分識別驗證和安全的私人通訊。</span><span class="sxs-lookup"><span data-stu-id="2b79b-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="2b79b-110">Schannel 主要用於需要安全超文字傳輸通訊協定 (HTTP) 通訊的網際網路應用程式。</span><span class="sxs-lookup"><span data-stu-id="2b79b-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="2b79b-111">如需詳細資訊，請參閱 [安全通道](../secauthn/secure-channel.md)。</span><span class="sxs-lookup"><span data-stu-id="2b79b-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b79b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b79b-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2b79b-113">[安全通道](../secauthn/secure-channel.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="2b79b-113">[Secure Channel](../secauthn/secure-channel.md)</span></span>
</dt> </dl>

 

 
