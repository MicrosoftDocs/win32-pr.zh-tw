---
title: 安全性和延伸錯誤資訊
description: 擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675235"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="ba3ea-103">安全性和延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="ba3ea-103">Security and Extended Error Information</span></span>

<span data-ttu-id="ba3ea-104">擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="ba3ea-105">考慮到這類安全性問題，預設會關閉擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="ba3ea-106">當停用擴充的錯誤資訊時，仍會產生擴充的錯誤資訊，但絕對不會在進程或電腦界限之間傳輸資訊。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="ba3ea-107">這種方法可讓有權存取進程位址空間的工具（例如偵錯工具）使用錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="ba3ea-108">開啟時，會產生擴充的錯誤資訊，並且可以跨進程和電腦界限傳送這些資訊。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="ba3ea-109">目前，擴充的錯誤資訊用於連接導向的通訊協定序列和本機 RPC (LRPC) 。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="ba3ea-110">它會針對資料包部分實行。</span><span class="sxs-lookup"><span data-stu-id="ba3ea-110">It is partially implemented for datagrams.</span></span>

 

 




