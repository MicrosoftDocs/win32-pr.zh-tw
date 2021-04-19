---
description: 傳輸層安全性 (TLS) 記錄通訊協定會使用在交握期間建立的金鑰來保護應用程式資料。
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: TLS 記錄通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984229"
---
# <a name="tls-record-protocol"></a><span data-ttu-id="95690-103">TLS 記錄通訊協定</span><span class="sxs-lookup"><span data-stu-id="95690-103">TLS Record Protocol</span></span>

<span data-ttu-id="95690-104">[*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 記錄通訊協定會使用在 [交握](tls-handshake-protocol.md)期間建立的金鑰來保護應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="95690-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="95690-105">記錄通訊協定負責保護應用程式資料，並驗證其 [*完整性*](../secgloss/i-gly.md) 和來源。</span><span class="sxs-lookup"><span data-stu-id="95690-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="95690-106">它會管理下列各項：</span><span class="sxs-lookup"><span data-stu-id="95690-106">It manages the following:</span></span>

-   <span data-ttu-id="95690-107">將外寄訊息分割成可管理的區塊，並目的地重組傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="95690-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="95690-108">壓縮外寄區塊和解壓縮連入區塊 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="95690-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="95690-109">將 [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 套用至外寄訊息，以及使用 MAC 來驗證傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="95690-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="95690-110">加密外寄訊息和解密傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="95690-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="95690-111">當記錄通訊協定完成時，傳出的加密資料會向下傳遞至傳輸控制通訊協定 (TCP) 層以進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="95690-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
