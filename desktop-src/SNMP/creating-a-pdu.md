---
title: 建立 PDU
description: 若要建立及初始化 PDU，則會呼叫 SnmpCreatePdu 函式的 WinSNMP 應用程式。
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840071"
---
# <a name="creating-a-pdu"></a><span data-ttu-id="2a8d2-103">建立 PDU</span><span class="sxs-lookup"><span data-stu-id="2a8d2-103">Creating a PDU</span></span>

<span data-ttu-id="2a8d2-104">若要建立及初始化 PDU，則會呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式的 WinSNMP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="2a8d2-104">To create and initialize a PDU a WinSNMP application calls the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="2a8d2-105">應用程式必須先呼叫 **SnmpCreatePdu** ，然後再呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，以要求 MICROSOFT WinSNMP 執行傳輸 PDU。</span><span class="sxs-lookup"><span data-stu-id="2a8d2-105">The application must call **SnmpCreatePdu** before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit a PDU.</span></span> <span data-ttu-id="2a8d2-106">應用程式也必須先呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ，然後再呼叫 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式來要求 SNMP 訊息的編碼。</span><span class="sxs-lookup"><span data-stu-id="2a8d2-106">The application must also call [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) before it calls the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function to request encoding of an SNMP message.</span></span>

<span data-ttu-id="2a8d2-107">應用程式必須呼叫 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) 函式，以釋放 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式為新的 pdu 配置的資源。</span><span class="sxs-lookup"><span data-stu-id="2a8d2-107">The application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function to release the resources that the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function allocates for new PDUs.</span></span>

 

 




