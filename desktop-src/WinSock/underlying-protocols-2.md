---
description: 您的應用程式相依于特定服務的一些通訊協定（例如遠端程序呼叫 (RPC) ）可能會有需要您根據其使用方式修改應用程式的 IP 版本相依功能和結構。
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: IPv6 Winsock 應用程式的基礎通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191329"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a><span data-ttu-id="ab019-103">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="ab019-103">Underlying Protocols for IPv6 Winsock Applications</span></span>

<span data-ttu-id="ab019-104">您的應用程式相依于特定服務的一些通訊協定（例如遠端程序呼叫 (RPC) ）可能會有需要您根據其使用方式修改應用程式的 IP 版本相依功能和結構。</span><span class="sxs-lookup"><span data-stu-id="ab019-104">Some protocols that your application depends on for certain services, such as Remote Procedure Call (RPC), may have IP-version dependent functions and structures that require you to modify your application in terms of their usage.</span></span>

<span data-ttu-id="ab019-105">修改程式碼以支援 IPv6 的程式中，有部分應包括判斷基礎通訊協定的使用是否 (從堆疊的角度來看，這些通訊協定是否視為較高層級的通訊協定) 需要修改才能正確地使用 IPv6。</span><span class="sxs-lookup"><span data-stu-id="ab019-105">Part of the process to modify your code to support IPv6 should include determining whether the use of the underlying protocols (from the perspective of the stack, these protocols are considered higher-layer protocols) require modification in order to properly make use of IPv6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab019-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab019-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab019-107">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="ab019-107">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ab019-108">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="ab019-108">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="ab019-109">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="ab019-109">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="ab019-110">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="ab019-110">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="ab019-111">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="ab019-111">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="ab019-112">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="ab019-112">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> </dl>

 

 



