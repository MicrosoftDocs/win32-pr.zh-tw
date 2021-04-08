---
title: 使用者驗證
description: 驗證通訊協定本身可以透過受保護的 EAP (PEAP) 來驗證使用者。
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679247"
---
# <a name="user-authentication"></a><span data-ttu-id="19f13-103">使用者驗證</span><span class="sxs-lookup"><span data-stu-id="19f13-103">User Authentication</span></span>

<span data-ttu-id="19f13-104">驗證通訊協定本身可以透過受保護的 EAP (PEAP) 來驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="19f13-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="19f13-105">作業系統中內建的驗證提供者有兩種： Windows 網域驗證 (透過目錄服務存取，) 和遠端存取撥入使用者服務 (RADIUS) 。</span><span class="sxs-lookup"><span data-stu-id="19f13-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="19f13-106">在 RADIUS 為驗證提供者的情況下，EAP 外掛程式會安裝在 RADIUS 伺服器上，而不是安裝在 (AP) server （例如 RAS 伺服器）的無線存取點上。</span><span class="sxs-lookup"><span data-stu-id="19f13-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="19f13-107">AP 伺服器會直接從用戶端將 EAP 封包傳遞給 RADIUS 伺服器上的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="19f13-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="19f13-108">AP 伺服器不會處理 EAP 封包中的任何資訊，但它必須接受伺服器端、完整強度 (256 位) PEAP 產生的加密金鑰，才能建立安全的連接。</span><span class="sxs-lookup"><span data-stu-id="19f13-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




