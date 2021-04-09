---
title: SNMP 支援層級
description: Microsoft WinSNMP 實行提供等級2的 SNMP 通訊支援。
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092230"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="47790-103">SNMP 支援層級</span><span class="sxs-lookup"><span data-stu-id="47790-103">Levels of SNMP Support</span></span>

<span data-ttu-id="47790-104">Microsoft WinSNMP 實行提供等級2的 SNMP 通訊支援。</span><span class="sxs-lookup"><span data-stu-id="47790-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="47790-105">層級2支援網際網路工程任務推動小組 (IETF) 標準的 SNMPv2 通訊協定，如 Rfc 1902-1908 中所定義。</span><span class="sxs-lookup"><span data-stu-id="47790-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="47790-106">它也支援在 RFC 1901 中定義的以社區為基礎的訊息包裝函式 (SNMPv2C) 。</span><span class="sxs-lookup"><span data-stu-id="47790-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="47790-107">層級2通訊支援包括訊息編碼和解碼服務，先前在 WinSNMP 1.1 版中稱為層級0通訊支援。</span><span class="sxs-lookup"><span data-stu-id="47790-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="47790-108">層級2也支援所有 SNMPv1 通訊協定作業，先前在 WinSNMP 1.1 版中稱為層級1通訊支援。</span><span class="sxs-lookup"><span data-stu-id="47790-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="47790-109">此實值會傳回它所支援的最大 SNMP 通訊層級，以回應透過 WinSNMP 應用程式對 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="47790-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="47790-110">如果 WinSNMP 應用程式使用的是 SNMP 訊息編碼和解碼的執行，則應用程式必須執行執行時所需的轉換。</span><span class="sxs-lookup"><span data-stu-id="47790-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="47790-111">這包括將呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函數所傳回的 SNMPv1 陷阱轉譯為 SNMPv2C 陷阱。</span><span class="sxs-lookup"><span data-stu-id="47790-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="47790-112">它也包括根據 RFC 1908，將 SNMPv1 定義的 PDU 類型轉譯為 SNMPv2C 定義的相關 PDU 類型。</span><span class="sxs-lookup"><span data-stu-id="47790-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




