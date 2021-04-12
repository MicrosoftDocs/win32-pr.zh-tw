---
description: WSAIoctl 函式可讓服務提供者提供提供者特有的功能延伸模組。
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific 擴充機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58a8bba3c83e7dbf973ff8fe5b7d91c1065cfc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113013"
---
# <a name="provider-specific-extension-mechanism"></a><span data-ttu-id="41597-103">Provider-Specific 擴充機制</span><span class="sxs-lookup"><span data-stu-id="41597-103">Provider-Specific Extension Mechanism</span></span>

<span data-ttu-id="41597-104">[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式可讓服務提供者提供提供者特有的功能延伸模組。</span><span class="sxs-lookup"><span data-stu-id="41597-104">The [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function enables service providers to offer provider-specific feature extensions.</span></span> <span data-ttu-id="41597-105">當然，這個機制假設應用程式知道特定的擴充功能，並同時瞭解所涉及的語法和語法。</span><span class="sxs-lookup"><span data-stu-id="41597-105">This mechanism assumes, of course, that an application is aware of a particular extension and understands both the semantics and syntax involved.</span></span> <span data-ttu-id="41597-106">服務提供者廠商通常會提供這類資訊。</span><span class="sxs-lookup"><span data-stu-id="41597-106">Such information would typically be supplied by the service provider vendor.</span></span>

<span data-ttu-id="41597-107">若要叫用擴充功能，應用程式必須先要求所需函式的指標。</span><span class="sxs-lookup"><span data-stu-id="41597-107">To invoke an extension function, the application must first ask for a pointer to the desired function.</span></span> <span data-ttu-id="41597-108">這是透過 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式使用 SIO 取得延伸模組函式 \_ \_ \_ \_ 指標命令程式碼來完成。</span><span class="sxs-lookup"><span data-stu-id="41597-108">This is done through the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using the SIO\_GET\_EXTENSION\_FUNCTION\_POINTER command code.</span></span> <span data-ttu-id="41597-109">要 **WSAIoctl** 的輸入緩衝區包含所需擴充功能函式的識別碼，而輸出緩衝區包含函式指標本身。</span><span class="sxs-lookup"><span data-stu-id="41597-109">The input buffer to **WSAIoctl** contains an identifier for the desired extension function while the output buffer contains the function pointer itself.</span></span> <span data-ttu-id="41597-110">然後，應用程式就可以直接叫用擴充功能，而不需透過 Ws2 \_32.dll。</span><span class="sxs-lookup"><span data-stu-id="41597-110">The application can then invoke the extension function directly without passing through the Ws2\_32.dll.</span></span>

<span data-ttu-id="41597-111">指派給延伸模組函式的識別碼是由服務提供者廠商所配置 (Guid) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="41597-111">The identifiers assigned to extension functions are globally unique identifiers (GUIDs) that are allocated by service provider vendors.</span></span> <span data-ttu-id="41597-112">建立延伸模組函式的廠商呼籲，以發佈函式的完整詳細資料，包括函數原型的語法。</span><span class="sxs-lookup"><span data-stu-id="41597-112">Vendors who create extension functions are urged to publish full details about the function including the syntax of the function prototype.</span></span> <span data-ttu-id="41597-113">這可讓多個服務提供者廠商提供常見且熱門的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="41597-113">This makes it possible for common and popular extension functions to be offered by more than one service provider vendor.</span></span> <span data-ttu-id="41597-114">應用程式可以取得函式指標並使用函式，而不需要知道任何有關執行函數的特定服務提供者。</span><span class="sxs-lookup"><span data-stu-id="41597-114">An application can obtain the function pointer and use the function without needing to know anything about the particular service provider that implements the function.</span></span>

<span data-ttu-id="41597-115">在 Windows Vista 和更新版本中，新的 Winsock 系統延伸模組會直接從 Winsock DLL 匯出，因此不需要 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式就能載入這些擴充功能。</span><span class="sxs-lookup"><span data-stu-id="41597-115">On Windows Vista and later, new Winsock system extensions are exported directly from the Winsock DLL, so the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function is not needed to load these extensions.</span></span> <span data-ttu-id="41597-116">Windows Vista 和更新版本上提供的新擴充功能，包括從 *Ws2 \_32.dll* 匯出的 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)和 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)函數。</span><span class="sxs-lookup"><span data-stu-id="41597-116">The new extension functions available on Windows Vista and later include the [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) functions that are exported from *Ws2\_32.dll*.</span></span>

 

 
