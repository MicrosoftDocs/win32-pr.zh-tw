---
title: RPC-Message 佇列應用程式的系統需求
description: 若要在 RPC 用戶端/伺服器應用程式中使用訊息佇列傳輸，伺服器和用戶端電腦必須安裝適當的作業系統平臺和訊息佇列軟體。
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382490"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="1c81a-103">RPC-Message 佇列應用程式的系統需求</span><span class="sxs-lookup"><span data-stu-id="1c81a-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="1c81a-104">若要在 RPC 用戶端/伺服器應用程式中使用訊息佇列傳輸，伺服器和用戶端電腦必須安裝適當的作業系統平臺和訊息佇列軟體。</span><span class="sxs-lookup"><span data-stu-id="1c81a-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="1c81a-105">伺服器電腦的需求如下：</span><span class="sxs-lookup"><span data-stu-id="1c81a-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="1c81a-106">Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1c81a-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="1c81a-107">SQL Server 6.5 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1c81a-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="1c81a-108">訊息佇列主要企業控制器或主要網站控制器。</span><span class="sxs-lookup"><span data-stu-id="1c81a-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="1c81a-109">RPC 伺服器端傳輸 DLL (RpcMqSvr.dll) 。</span><span class="sxs-lookup"><span data-stu-id="1c81a-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="1c81a-110">用戶端電腦的需求如下：</span><span class="sxs-lookup"><span data-stu-id="1c81a-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="1c81a-111">Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1c81a-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="1c81a-112">Microsoft Message Queuing 用戶端。</span><span class="sxs-lookup"><span data-stu-id="1c81a-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="1c81a-113">RPC 用戶端傳輸 DLL (RpcMqCl.dll) 。</span><span class="sxs-lookup"><span data-stu-id="1c81a-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="1c81a-114">當 MSMQ 元件安裝在用戶端和伺服器電腦上時，系統登錄會自動設定為包含遠端程序呼叫的 [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) 訊息佇列傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1c81a-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="1c81a-115">若要建立您的 RPC MSMQ 應用程式，您需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="1c81a-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="1c81a-116">Microsoft Windows Server 2003、Windows XP 或 Windows 2000 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1c81a-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="1c81a-117">MIDL 版本3.1.76 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1c81a-117">MIDL version 3.1.76 or later.</span></span>

 

 