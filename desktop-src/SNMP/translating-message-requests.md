---
title: 翻譯訊息要求
description: 本主題說明將 SNMPv1 要求轉譯成 SNMPv2 要求的程式。
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885888"
---
# <a name="translating-message-requests"></a>翻譯訊息要求

本主題說明將 SNMPv1 要求轉譯成 SNMPv2 要求的程式。

如果 WinSNMP 應用程式要求在 SNMP 版本2C 架構下提供的功能 (SNMPv2C) ，但目標實體僅支援 SNMP 第1版架構 (SNMPv1) ，則 Microsoft WinSNMP 執行會嘗試將要求轉譯為 SNMPv1 格式。 若要這樣做，執行會使用 RFC 1908 中定義的程式：「第1版與第2版 Internet-Standard 網路管理架構之間的共存」。 如果無法轉譯， [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式會因為擴充的錯誤碼 SNMPAPI 作業無效而 \_ 失敗 \_ 。

 

 




