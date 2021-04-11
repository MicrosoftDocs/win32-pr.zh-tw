---
title: 開啟和關閉 WinSNMP 會話
description: 若要開啟會話，應用程式會呼叫 SnmpCreateSession 函數。
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021772"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="ca24e-103">開啟和關閉 WinSNMP 會話</span><span class="sxs-lookup"><span data-stu-id="ca24e-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="ca24e-104">若要開啟會話，應用程式會呼叫 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) 函數。</span><span class="sxs-lookup"><span data-stu-id="ca24e-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="ca24e-105">如果函式順利完成，Microsoft WinSNMP 執行會開啟會話，而此函式會以 **HSNMP \_ 會話** 控制碼的形式傳回會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca24e-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="ca24e-106">所有傳回控制碼變數的 WinSNMP 函數都會包含會話識別碼作為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ca24e-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="ca24e-107">這可讓實作為使用控制碼，有效率地管理工作階段層級的資源。</span><span class="sxs-lookup"><span data-stu-id="ca24e-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="ca24e-108">應用程式一次可以有多個會話開啟。</span><span class="sxs-lookup"><span data-stu-id="ca24e-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="ca24e-109">應用程式內的多個會話可以共用控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="ca24e-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="ca24e-110">如果由於資源限制而無法開啟會話，則 \_ 當應用程式呼叫 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)時，它會傳回 SNMPAPI 失敗。</span><span class="sxs-lookup"><span data-stu-id="ca24e-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="ca24e-111">如果應用程式接著呼叫 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 函數，它會傳回 SNMPAPI \_ 配置 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca24e-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="ca24e-112">[**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)函式的呼叫可讓實作為釋放任何剩餘的資源，並關閉會話。</span><span class="sxs-lookup"><span data-stu-id="ca24e-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="ca24e-113">如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md) 和 [WinSNMP 會話](winsnmp-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="ca24e-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




