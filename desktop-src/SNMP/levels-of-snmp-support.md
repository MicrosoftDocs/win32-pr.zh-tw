---
title: SNMP 支援層級
description: Microsoft WinSNMP 實行提供等級2的 SNMP 通訊支援。
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009456"
---
# <a name="levels-of-snmp-support"></a>SNMP 支援層級

Microsoft WinSNMP 實行提供等級2的 SNMP 通訊支援。 層級2支援網際網路工程任務推動小組 (IETF) 標準的 SNMPv2 通訊協定，如 Rfc 1902-1908 中所定義。 它也支援在 RFC 1901 中定義的以社區為基礎的訊息包裝函式 (SNMPv2C) 。

層級2通訊支援包括訊息編碼和解碼服務，先前在 WinSNMP 1.1 版中稱為層級0通訊支援。 層級2也支援所有 SNMPv1 通訊協定作業，先前在 WinSNMP 1.1 版中稱為層級1通訊支援。

此實值會傳回它所支援的最大 SNMP 通訊層級，以回應透過 WinSNMP 應用程式對 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式的呼叫。

如果 WinSNMP 應用程式使用的是 SNMP 訊息編碼和解碼的執行，則應用程式必須執行執行時所需的轉換。 這包括將呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函數所傳回的 SNMPv1 陷阱轉譯為 SNMPv2C 陷阱。 它也包括根據 RFC 1908，將 SNMPv1 定義的 PDU 類型轉譯為 SNMPv2C 定義的相關 PDU 類型。

 

 




