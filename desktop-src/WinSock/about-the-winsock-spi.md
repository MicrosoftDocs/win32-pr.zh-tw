---
description: Winsock 提供服務提供者介面，用來建立 Winsock 服務，通常稱為 Winsock SPI。
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: 關於 Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113116"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="493a6-103">關於 Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="493a6-103">About the Winsock SPI</span></span>

<span data-ttu-id="493a6-104">Winsock 提供服務提供者介面，用來建立 Winsock 服務，通常稱為 Winsock SPI。</span><span class="sxs-lookup"><span data-stu-id="493a6-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="493a6-105">有兩種類型的服務提供者存在：傳輸提供者和命名空間提供者。</span><span class="sxs-lookup"><span data-stu-id="493a6-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="493a6-106">傳輸提供者的範例包括通訊協定堆疊（例如 TCP/IP 或 IPX/SPX），而命名空間提供者的範例是網際網路網域命名系統 (DNS) 的介面。</span><span class="sxs-lookup"><span data-stu-id="493a6-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="493a6-107">服務提供者介面規格的個別區段適用于每種類型的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="493a6-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="493a6-108">[傳輸](transport-service-providers-2.md) 和 [命名空間](name-space-service-providers-2.md) 服務提供者必須在 \_ 安裝時向 Ws232.dll 註冊。</span><span class="sxs-lookup"><span data-stu-id="493a6-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="493a6-109">此註冊只需要針對每個提供者執行一次，因為必要的資訊會保留在持續性儲存體中。</span><span class="sxs-lookup"><span data-stu-id="493a6-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



