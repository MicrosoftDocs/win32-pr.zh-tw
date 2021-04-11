---
description: Windows 通訊端的名稱解析和註冊模型 (Winsock) SPI。
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: SPI 的名稱解析模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113033"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="5b5a0-103">SPI 的名稱解析模型</span><span class="sxs-lookup"><span data-stu-id="5b5a0-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="5b5a0-104">在開發與通訊協定無關的用戶端/伺服器應用程式時，有兩個基本的需求存在於名稱解析和註冊方面：</span><span class="sxs-lookup"><span data-stu-id="5b5a0-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="5b5a0-105">伺服器一半的應用程式 (在此稱為服務，) 在 (中註冊其存在，或可) 一個或多個命名空間存取。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="5b5a0-106">用戶端應用程式在命名空間中尋找服務的能力，並取得所需的傳輸通訊協定和定址資訊。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="5b5a0-107">針對習慣開發以 TCP/IP 為基礎的應用程式的人，這可能只需要查閱主機位址，然後使用同意的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="5b5a0-108">不過，其他網路設定可允許服務的位置、用於服務的通訊協定，以及在執行時間探索到的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="5b5a0-109">為了容納現有名稱服務中的功能範圍，Windows 通訊端2介面採用如下所述的模型。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="5b5a0-110">「 *命名空間* 」（namespace）是指將 (與一個或多個人易記名稱的通訊協定) 的最小值相關聯的功能，以及定址網路服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="5b5a0-111">許多命名空間目前可廣泛使用，包括網際網路的網域名稱系統 (DNS) 、NetWare 目錄服務 (NDS) 、X 500 等等。這些命名空間的組織和實行方式有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="5b5a0-112">從 Windows 通訊端名稱解析的觀點來看，某些屬性特別重要。</span><span class="sxs-lookup"><span data-stu-id="5b5a0-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



