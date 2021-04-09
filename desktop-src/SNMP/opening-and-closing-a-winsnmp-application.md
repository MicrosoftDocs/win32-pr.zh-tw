---
title: 開啟和關閉 WinSNMP 應用程式
description: 在呼叫任何其他的 WinSNMP 函數之前，必須先成功呼叫 SnmpStartup 函式。
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021774"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="93f22-103">開啟和關閉 WinSNMP 應用程式</span><span class="sxs-lookup"><span data-stu-id="93f22-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="93f22-104">在呼叫任何其他的 WinSNMP 函數之前，必須先成功呼叫 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式。</span><span class="sxs-lookup"><span data-stu-id="93f22-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="93f22-105">**SnmpStartup** 函式可讓 Microsoft WinSNMP 實行執行初始化程式。</span><span class="sxs-lookup"><span data-stu-id="93f22-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="93f22-106">函式也會將執行所支援的 WinSNMP API 版本、支援的 SNMP 通訊層級，以及執行的預設轉譯和重新傳輸模式，傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="93f22-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="93f22-107">當應用程式不再需要執行程式的服務時，必須呼叫 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 函式。</span><span class="sxs-lookup"><span data-stu-id="93f22-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="93f22-108">即使 **SnmpCleanup** 可讓實施解除配置配置給應用程式的所有資源，建議應用程式先針對每個開啟的 WinSNMP 會話呼叫 [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) 函式一次，以將執行效能最大化。</span><span class="sxs-lookup"><span data-stu-id="93f22-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="93f22-109">在終止應用程式之前，必須先呼叫 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 作為最後的 WinSNMP 函數。</span><span class="sxs-lookup"><span data-stu-id="93f22-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




