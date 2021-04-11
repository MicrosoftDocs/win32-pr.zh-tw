---
description: 訊息驗證碼 (MAC) 用來偵測訊息篡改和偽造。
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Schannel 中的訊息驗證碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194068"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="b1f23-103">Schannel 中的訊息驗證碼</span><span class="sxs-lookup"><span data-stu-id="b1f23-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="b1f23-104">[*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 用來偵測訊息篡改和偽造。</span><span class="sxs-lookup"><span data-stu-id="b1f23-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="b1f23-105">訊息的傳送者會使用傳送者和收件者所共用的 [*工作階段金鑰*](../secgloss/s-gly.md)，加密訊息內文的單向 [*雜湊*](../secgloss/h-gly.md)來建立 MAC。</span><span class="sxs-lookup"><span data-stu-id="b1f23-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="b1f23-106">MAC 會附加至傳送給收件者的訊息。</span><span class="sxs-lookup"><span data-stu-id="b1f23-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="b1f23-107">訊息收件者會使用共用工作階段金鑰和訊息內文再次產生 MAC，並將產生的 MAC 與接收自傳送者的 MAC 進行比較。</span><span class="sxs-lookup"><span data-stu-id="b1f23-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="b1f23-108">如果兩者相同，則寄件者必須有共用工作階段金鑰，而且訊息在傳輸時尚未改變。</span><span class="sxs-lookup"><span data-stu-id="b1f23-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="b1f23-109">在安全通道通訊協定中，用來產生 MAC 的演算法是由傳送者和收件者所使用的 [加密套件](cipher-suites-in-schannel.md) 所決定。</span><span class="sxs-lookup"><span data-stu-id="b1f23-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
