---
title: 關於重新傳輸
description: WinSNMP 應用程式可以透過各種方式進行 SNMP 作業要求。
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300436"
---
# <a name="about-retransmission"></a><span data-ttu-id="a716e-103">關於重新傳輸</span><span class="sxs-lookup"><span data-stu-id="a716e-103">About Retransmission</span></span>

<span data-ttu-id="a716e-104">WinSNMP 應用程式可以透過各種方式進行 SNMP 作業要求。</span><span class="sxs-lookup"><span data-stu-id="a716e-104">A WinSNMP application can make SNMP operation requests in various ways.</span></span> <span data-ttu-id="a716e-105">應用程式可以在不等候回應的情況下，對 SNMP 代理程式發出數個要求，也可以發出單一要求並等候回應。</span><span class="sxs-lookup"><span data-stu-id="a716e-105">The application can issue several requests to an SNMP agent, without waiting for a response, or it can issue a single request and wait for the response.</span></span> <span data-ttu-id="a716e-106">由於 SNMP 可以在多個傳輸通訊協定上執行，因此傳遞機制和可靠性特性可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="a716e-106">Since SNMP can be implemented on multiple transport protocols, delivery mechanisms and reliability characteristics can vary.</span></span>

<span data-ttu-id="a716e-107">當您撰寫「WinSNMP」應用程式的程式碼時，您必須根據應用程式發出作業要求的方式，判斷通訊作業需要的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="a716e-107">When you code the WinSNMP application you must determine the level of reliability you need for communications operations, based on the way the application issues operation requests.</span></span> <span data-ttu-id="a716e-108">然後，您必須選取重新傳輸策略，並執行重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="a716e-108">Then you must select a retransmission strategy and implement a retransmission policy.</span></span>

<span data-ttu-id="a716e-109">重新傳輸原則包含超時時間和重試計數。</span><span class="sxs-lookup"><span data-stu-id="a716e-109">A retransmission policy includes a time-out period and a retry count.</span></span> <span data-ttu-id="a716e-110">超時期間是指應用程式在 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 要求的發行和收到的對應訊息之間，所經過的時間（百分之一秒）。</span><span class="sxs-lookup"><span data-stu-id="a716e-110">A time-out period is the elapsed time, in hundredths of a second, between an application's issuance of an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request and its receipt of the corresponding message.</span></span> <span data-ttu-id="a716e-111">應用程式會在呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式時收到訊息。</span><span class="sxs-lookup"><span data-stu-id="a716e-111">The application receives the message as a result of a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function.</span></span> <span data-ttu-id="a716e-112">超時值是 Microsoft 的 WinSNMP 執行等候實體回應通訊要求的一段時間。</span><span class="sxs-lookup"><span data-stu-id="a716e-112">The time-out value is the period of time the Microsoft WinSNMP implementation waits for an entity to respond to a communication request.</span></span> <span data-ttu-id="a716e-113">如果在超時期間內沒有任何回應，則會在 [重試計數] 值指定重新傳輸嘗試，或無法呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)時，將要求重新傳輸。</span><span class="sxs-lookup"><span data-stu-id="a716e-113">If there is no response within the time-out period, the implementation either retransmits the request if the retry count value specifies retransmission attempts, or it fails the call to [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span> <span data-ttu-id="a716e-114">重試計數是當 SNMP 傳輸要求失敗時，執行所進行的重新傳輸嘗試次數上限。</span><span class="sxs-lookup"><span data-stu-id="a716e-114">A retry count is the maximum number of retransmission attempts the implementation makes if an SNMP transmission request fails.</span></span>

<span data-ttu-id="a716e-115">此實值會在應用程式的資料庫中儲存超時值和重試計數。</span><span class="sxs-lookup"><span data-stu-id="a716e-115">The implementation stores time-out values and retry counts in its database for the application.</span></span> <span data-ttu-id="a716e-116">此實值會儲存每個目的地實體的個別值。</span><span class="sxs-lookup"><span data-stu-id="a716e-116">The implementation stores individual values for each destination entity.</span></span>

<span data-ttu-id="a716e-117">應用程式必須建立自己的輪詢頻率，且必須管理計時器變數。</span><span class="sxs-lookup"><span data-stu-id="a716e-117">Applications must establish their own polling frequencies and they must manage timer variables.</span></span> <span data-ttu-id="a716e-118">如需詳細資訊，請參閱 [管理重新傳輸原則](managing-the-retransmission-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="a716e-118">For more information, see [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




