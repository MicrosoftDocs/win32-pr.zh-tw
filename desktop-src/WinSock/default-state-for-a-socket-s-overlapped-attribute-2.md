---
description: 在第一個 Wsock32.dll （32位版本的 Windows 通訊端1.1）中，通訊端函式會以預設設定的重迭屬性來建立通訊端。
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: 通訊端之重迭屬性的預設狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113088"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="f2225-103">通訊端之重迭屬性的預設狀態</span><span class="sxs-lookup"><span data-stu-id="f2225-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="f2225-104">在第一個 Wsock32.dll （32位版本的 Windows 通訊端1.1）中， [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式會以預設設定的重迭屬性來建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="f2225-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="f2225-105">為了確保與目前部署 Wsock32.dll 的相容性，這也會持續適用于 Windows 通訊端2。</span><span class="sxs-lookup"><span data-stu-id="f2225-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="f2225-106">也就是說，使用 **socket** 函式建立的 Windows 通訊端2通訊端將會有重迭的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2225-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="f2225-107">不過，為了與 Windows API 的其餘部分相容，使用 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 建立的通訊端不會有重迭的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2225-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="f2225-108">只有在設定 WSA 旗標重迭位時，才會套用此屬性 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f2225-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



