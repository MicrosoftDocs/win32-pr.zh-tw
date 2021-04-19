---
description: Windows 通訊端 2 (適用于 multipoint 和多播的 Winsock) 介面元素。
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: 適用于 Multipoint 和多播的 Windows 通訊端2介面元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977196"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="a3074-103">適用于 Multipoint 和多播的 Windows 通訊端2介面元素</span><span class="sxs-lookup"><span data-stu-id="a3074-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="a3074-104">已併入 Windows 通訊端2以利用 multipoint 功能的機制可摘要如下：</span><span class="sxs-lookup"><span data-stu-id="a3074-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="a3074-105">[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中有三個屬性位。</span><span class="sxs-lookup"><span data-stu-id="a3074-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="a3074-106">針對 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)的 *dwFlags* 參數定義的四個旗標。</span><span class="sxs-lookup"><span data-stu-id="a3074-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="a3074-107">一個函式 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)，用於將分葉節點新增至 multipoint 會話。</span><span class="sxs-lookup"><span data-stu-id="a3074-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="a3074-108">用於控制 multipoint 回送的兩個 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 命令代碼，以及多播傳輸的範圍。</span><span class="sxs-lookup"><span data-stu-id="a3074-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="a3074-109">下列各節將更詳細地說明這些介面元素：</span><span class="sxs-lookup"><span data-stu-id="a3074-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="a3074-110">聯結 Multipoint 離開的語義</span><span class="sxs-lookup"><span data-stu-id="a3074-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="a3074-111">現有 Multipoint 通訊協定如何支援這些擴充功能</span><span class="sxs-lookup"><span data-stu-id="a3074-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
