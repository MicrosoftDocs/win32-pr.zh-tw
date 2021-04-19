---
description: 大部分 UNIX 執行所提供的 SIOCGIFCONF 命令都支援使用命令 SIO \_ GET INTERFACE LIST 形式的 WSAIoctl 和 WSPIoctl 函數 \_ \_ 。 此命令會傳回已設定之介面及其參數的清單。
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: 在 Winsock 中使用 UNIX Ioctls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991872"
---
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="e00fc-104">在 Winsock 中使用 UNIX Ioctls</span><span class="sxs-lookup"><span data-stu-id="e00fc-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="e00fc-105">大部分 UNIX 執行所提供的 **SIOCGIFCONF** 命令都支援使用命令 **SIO \_ GET \_ INTERFACE \_ LIST** 形式的 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))函數。</span><span class="sxs-lookup"><span data-stu-id="e00fc-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="e00fc-106">此命令會傳回已設定之介面及其參數的清單。</span><span class="sxs-lookup"><span data-stu-id="e00fc-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="e00fc-107">對 Windows 通訊端2相容的 TCP/IP 服務提供者，此命令的支援是必要的。</span><span class="sxs-lookup"><span data-stu-id="e00fc-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="e00fc-108">參數 *lpvOutBuffer* 會指向緩衝區，而 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 會在其中儲存介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e00fc-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="e00fc-109">您可以根據 *lpcbBytesReturned* 中傳回的輸出緩衝區實際長度，判斷 *lpvOutBuffer*) 中所傳回之結構的介面數目 (。</span><span class="sxs-lookup"><span data-stu-id="e00fc-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 
