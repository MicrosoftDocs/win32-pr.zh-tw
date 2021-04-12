---
description: 與通訊協定無關的名稱解析和 Windows 通訊端 (Winsock) 。
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Protocol-Independent 名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318367"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="89b82-103">Protocol-Independent 名稱解析</span><span class="sxs-lookup"><span data-stu-id="89b82-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="89b82-104">在開發與通訊協定無關的用戶端/伺服器應用程式時，有兩個基本的需求存在於名稱解析和註冊方面：</span><span class="sxs-lookup"><span data-stu-id="89b82-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="89b82-105">伺服器一半的應用程式 ( 服務) 在 (內登錄其存在，或可) 一或多個命名空間存取。</span><span class="sxs-lookup"><span data-stu-id="89b82-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="89b82-106">用戶端應用程式在命名空間中尋找服務的能力，並取得所需的傳輸通訊協定和定址資訊。</span><span class="sxs-lookup"><span data-stu-id="89b82-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="89b82-107">針對習慣開發以 TCP/IP 為基礎的應用程式的人，這似乎只需要查閱主機位址，然後使用同意的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="89b82-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="89b82-108">不過，其他網路設定則允許服務的位置、用於服務的通訊協定，以及在執行時間探索到的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="89b82-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="89b82-109">為了配合現有名稱服務中的廣泛多樣性功能，Windows 通訊端2介面採用本節中的主題所述的模型。</span><span class="sxs-lookup"><span data-stu-id="89b82-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="89b82-110">本節說明 Winsock 開發人員可用的通訊協定獨立名稱解析功能。</span><span class="sxs-lookup"><span data-stu-id="89b82-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="89b82-111">下列清單說明本節中的主題：</span><span class="sxs-lookup"><span data-stu-id="89b82-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="89b82-112">名稱解析模型</span><span class="sxs-lookup"><span data-stu-id="89b82-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="89b82-113">名稱解析函數的摘要</span><span class="sxs-lookup"><span data-stu-id="89b82-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="89b82-114">名稱解析資料結構</span><span class="sxs-lookup"><span data-stu-id="89b82-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="89b82-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="89b82-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89b82-116">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="89b82-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



