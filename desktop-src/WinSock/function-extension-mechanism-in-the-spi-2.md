---
description: 由於 Winsock DLL 本身不再由每個個別堆疊廠商提供，因此堆疊廠商無法藉由將進入點新增至 Winsock DLL 來提供擴充功能。
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: SPI 中的函數延伸機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cfa6c9dfaf3afcec8e6861a9a0d3545a7ed0c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972036"
---
# <a name="function-extension-mechanism-in-the-spi"></a><span data-ttu-id="38345-103">SPI 中的函數延伸機制</span><span class="sxs-lookup"><span data-stu-id="38345-103">Function Extension Mechanism in the SPI</span></span>

<span data-ttu-id="38345-104">由於 Winsock DLL 本身不再由每個個別堆疊廠商提供，因此堆疊廠商無法藉由將進入點新增至 Winsock DLL 來提供擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38345-104">Because the Winsock DLL itself is no longer supplied by each individual stack vendor, it is not possible for a stack vendor to offer extended functionality by adding entry points to the Winsock DLL.</span></span> <span data-ttu-id="38345-105">為了克服這項限制，Winsock 利用新的 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式來容納希望提供提供者專屬功能延伸模組的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="38345-105">To overcome this limitation, Winsock takes advantage of the new [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function to accommodate service providers who wish to offer provider-specific functionality extensions.</span></span> <span data-ttu-id="38345-106">這項機制會 presupposes 應用程式知道特定的擴充功能，並瞭解相關的語法和語法。</span><span class="sxs-lookup"><span data-stu-id="38345-106">This mechanism presupposes that an application is aware of a particular extension and understands both the semantics and syntax involved.</span></span> <span data-ttu-id="38345-107">服務提供者廠商通常會提供這類資訊。</span><span class="sxs-lookup"><span data-stu-id="38345-107">Such information would typically be supplied by the service provider vendor.</span></span>

<span data-ttu-id="38345-108">若要叫用擴充功能，應用程式必須先要求所需函式的指標。</span><span class="sxs-lookup"><span data-stu-id="38345-108">To invoke an extension function, the application must first ask for a pointer to the desired function.</span></span> <span data-ttu-id="38345-109">這是透過 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式使用 SIO 取得延伸模組函式 \_ \_ \_ \_ 指標命令程式碼來完成。</span><span class="sxs-lookup"><span data-stu-id="38345-109">This is done through the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using the SIO\_GET\_EXTENSION\_FUNCTION\_POINTER command code.</span></span> <span data-ttu-id="38345-110">**WSAIoctl** 函式的輸入緩衝區包含所需擴充功能函式的識別碼，而且輸出緩衝區將包含函式指標本身。</span><span class="sxs-lookup"><span data-stu-id="38345-110">The input buffer to the **WSAIoctl** function contains an identifier for the desired extension function and the output buffer will contain the function pointer itself.</span></span> <span data-ttu-id="38345-111">然後，應用程式就可以直接叫用擴充功能，而不需透過 Ws2 \_32.dll。</span><span class="sxs-lookup"><span data-stu-id="38345-111">The application can then invoke the extension function directly without passing through the Ws2\_32.dll.</span></span>

<span data-ttu-id="38345-112">指派給延伸模組函式的識別碼是由服務提供者廠商所配置 (Guid) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="38345-112">The identifiers assigned to extension functions are globally unique identifiers (GUIDs) that are allocated by service provider vendors.</span></span> <span data-ttu-id="38345-113">建立延伸模組函式的廠商呼籲，以發佈函式的完整詳細資料，包括函數原型的語法。</span><span class="sxs-lookup"><span data-stu-id="38345-113">Vendors who create extension functions are urged to publish full details about the function including the syntax of the function prototype.</span></span> <span data-ttu-id="38345-114">這可促進多個服務提供者提供的一般及/或熱門擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38345-114">This facilitates common and/or popular extension functions to be offered by multiple service providers.</span></span> <span data-ttu-id="38345-115">應用程式可以取得函式指標並使用函式，而不需要知道任何有關執行函數的特定服務提供者。</span><span class="sxs-lookup"><span data-stu-id="38345-115">An application can obtain the function pointer and use the function without needing to know anything about the particular service provider that implements the function.</span></span>

 

 



