---
description: 泛型 Winsock multipoint 函數支援 IP 多播。
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: 多點傳送
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113044"
---
# <a name="multicast"></a><span data-ttu-id="8d9f2-103">多點傳送</span><span class="sxs-lookup"><span data-stu-id="8d9f2-103">Multicast</span></span>

<span data-ttu-id="8d9f2-104">泛型 Winsock multipoint 函數支援 IP 多播。</span><span class="sxs-lookup"><span data-stu-id="8d9f2-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="8d9f2-105">不過，支援多播的 TCP/IP 傳輸提供者也必須提供 Berkeley 軟體散發 (BSD) 樣式–支援對應的多播選項來支援多播。</span><span class="sxs-lookup"><span data-stu-id="8d9f2-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="8d9f2-106">這可簡化將現有多播應用程式移植到 Windows 通訊端2的程式。</span><span class="sxs-lookup"><span data-stu-id="8d9f2-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



