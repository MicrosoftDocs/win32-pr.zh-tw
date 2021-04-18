---
title: 翻譯訊息要求
description: 本主題說明將 SNMPv1 要求轉譯成 SNMPv2 要求的程式。
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507109"
---
# <a name="translating-message-requests"></a><span data-ttu-id="ea456-103">翻譯訊息要求</span><span class="sxs-lookup"><span data-stu-id="ea456-103">Translating Message Requests</span></span>

<span data-ttu-id="ea456-104">本主題說明將 SNMPv1 要求轉譯成 SNMPv2 要求的程式。</span><span class="sxs-lookup"><span data-stu-id="ea456-104">This topic describes the process of translating SNMPv1 requests into SNMPv2 requests.</span></span>

<span data-ttu-id="ea456-105">如果 WinSNMP 應用程式要求在 SNMP 版本2C 架構下提供的功能 (SNMPv2C) ，但目標實體僅支援 SNMP 第1版架構 (SNMPv1) ，則 Microsoft WinSNMP 執行會嘗試將要求轉譯為 SNMPv1 格式。</span><span class="sxs-lookup"><span data-stu-id="ea456-105">If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity supports only the SNMP version 1 framework (SNMPv1), the Microsoft WinSNMP implementation attempts to translate the request to the SNMPv1 format.</span></span> <span data-ttu-id="ea456-106">若要這樣做，執行會使用 RFC 1908 中定義的程式：「第1版與第2版 Internet-Standard 網路管理架構之間的共存」。</span><span class="sxs-lookup"><span data-stu-id="ea456-106">To do this, the implementation uses the procedures defined in RFC 1908, "Coexistence Between Version 1 and Version 2 of the Internet-Standard Network Management Framework."</span></span> <span data-ttu-id="ea456-107">如果無法轉譯， [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式會因為擴充的錯誤碼 SNMPAPI 作業無效而 \_ 失敗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ea456-107">If translation is not possible, the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function fails with the extended error code SNMPAPI\_OPERATION\_INVALID.</span></span>

 

 




